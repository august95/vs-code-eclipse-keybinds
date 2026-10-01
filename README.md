# Adding the Eclipse-style C/C++ keybindings

This repo is the **source of truth** for the keybindings. It's mirrored (copies
kept in sync, not symlinked) into:

- `trunk/.vscode/keybindings.json` and `trunk/.vscode/extensions.json` — shareable
  reference copies for anyone working in that repo.
- `%APPDATA%\Code\User\keybindings.json` on the Windows client — the **actual
  live file** VS Code reads. See "Why a plain copy into `.vscode/` doesn't work"
  below for why this copy has to exist separately.

`keybindings.json` was built from a full export of the user's real Eclipse C/C++
keymap (`eclipse-key-export.csv`, 336 entries). `COVERAGE.md` has a row-by-row
accounting of every entry in that export — what's mapped here, what's covered by
the Eclipse Keymap extension, what's already a stock VS Code default, and what has
no VS Code/cpptools equivalent (with the reason why).

## Steps

1. Open the Command Palette → **"Preferences: Open Keyboard Shortcuts (JSON)"**.
   This always opens the keybindings.json that your *current window* actually
   reads, so it's the simplest way to apply changes and avoids path-guessing.
2. Copy the contents of this repo's `keybindings.json` into that file (merge
   with any existing entries, don't just overwrite).
3. Save, then reload the window (Command Palette → **"Developer: Reload
   Window"**) if the shortcuts don't respond immediately.

## Why a plain copy into `.vscode/` doesn't work

VS Code only loads `keybindings.json` from the **user profile**, never from a
workspace's `.vscode/` folder (unlike `settings.json`, which is
workspace-scoped). So a repo-local `keybindings.json` is just a reference/share
mechanism — it must always be copied into the real profile file to take effect.

## The Remote-WSL / Remote-SSH gotcha

Keybindings are handled entirely by the **client** (the machine running the
VS Code UI), never by the remote host. If you're connected via Remote-WSL or
Remote-SSH, writing to the remote side's user data dir
(e.g. `~/.vscode-server/data/User/keybindings.json` inside WSL) has **no
effect** — that's backend-only state.

The file that actually matters is the client-side one:

- Windows client: `%APPDATA%\Code\User\keybindings.json`
  (i.e. `C:\Users\<you>\AppData\Roaming\Code\User\keybindings.json`)
- From inside WSL this is reachable at:
  `/mnt/c/Users/<you>/AppData/Roaming/Code/User/keybindings.json`

If you use multiple VS Code **profiles**, check which profile your workspace
is bound to (`globalStorage/storage.json` → `profileAssociations`) — a non-default
profile may have its own `profiles/<name>/keybindings.json` instead of the
plain `User/keybindings.json`, unless it inherits keybindings from Default.

Using step 1 above (the Command Palette command) sidesteps all of this,
since it opens the correct file for whatever client/profile you're
currently in — use the manual path only if you need to debug why shortcuts
aren't applying.

## `extensions.json` needs no copy-in step

Unlike `keybindings.json`, a workspace's `.vscode/extensions.json` *is*
workspace-scoped — VS Code reads it directly from the repo and prompts to
install anything listed under `recommendations` the first time you open the
folder (or when the list changes). Nothing to document there beyond the one
recommended extension, **"Eclipse Keymap"** (`alphabotsec.vscode-eclipse-keybindings`),
which covers the rest of Eclipse's general shortcuts (debug F5-F8, window/view
navigation, etc.) that `keybindings.json` here doesn't touch. If you install it,
be aware it ships its own large set of keybinding overrides — ours take priority
for the C/C++-specific entries only because user `keybindings.json` entries
always beat extension-contributed ones, not because of any ordering between the
two files. This repo's own `extensions.json` is just a copy for reference; it has
no effect sitting here, only when it's the workspace's `.vscode/extensions.json`.

## Updating from a new Eclipse export

If you re-export your Eclipse keymap (Eclipse: **Window → Preferences → General →
Keys → Export CSV**) and want to refresh this mapping:

1. Drop the new CSV in this repo and diff it against `eclipse-key-export.csv` to
   see what actually changed — most rows are noise (Eclipse re-exports everything,
   not just customizations).
2. For each new/changed row, classify by its **Eclipse command ID** (the last CSV
   column), not by the label — labels are ambiguous (e.g. multiple rows named
   "Format" or "Open Declaration" map to different IDs depending on editor context),
   but the ID tells you unambiguously what it does and whether it's a duplicate of
   a row you've already handled in another editor context (XML/Java/etc. editors
   using the exact same gesture).
3. Before adding any new VS Code command ID to `keybindings.json`, verify it's
   real — don't guess from memory. Check it against:
   - The actual installed extension's `package.json` (e.g. cpptools' contributed
     commands), not assumed naming conventions.
   - VS Code core source (`microsoft/vscode` on GitHub) for built-in commands.
   - The bundled `references-view` extension's `package.json` for hierarchy/reference
     commands — `editor.showTypeHierarchy`/`editor.showCallHierarchy` look plausible
     but don't exist; the real IDs are `references-view.showTypeHierarchy` /
     `references-view.showCallHierarchy`. This exact mistake shipped once already.
4. Update `COVERAGE.md` for any newly classified rows so the accounting stays
   complete (it should always sum to the CSV's total row count).
5. Mirror the updated `keybindings.json` to `trunk/.vscode/keybindings.json` and
   to the live `%APPDATA%\Code\User\keybindings.json`, then reload the window.
   
