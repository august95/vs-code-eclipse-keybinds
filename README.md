# Adding the Eclipse-style C/C++ keybindings

Reference file: `trunk/.vscode/keybindings.json` (source of truth, kept here for
sharing — VS Code does not load it automatically, see below).

## Steps

1. Open the Command Palette → **"Preferences: Open Keyboard Shortcuts (JSON)"**.
   This always opens the keybindings.json that your *current window* actually
   reads, so it's the simplest way to apply changes and avoids path-guessing.
2. Copy the contents of `trunk/.vscode/keybindings.json` into that file (merge
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

Unlike `keybindings.json`, `trunk/.vscode/extensions.json` *is* workspace-scoped
— VS Code reads it directly from the repo and prompts to install anything
listed under `recommendations` the first time you open the folder (or when the
list changes). Nothing to document there beyond the one recommended extension,
**"Eclipse Keymap"** (`alphabotsec.vscode-eclipse-keybindings`), which covers
the rest of Eclipse's general shortcuts (debug F5-F8, perspectives, etc.) that
`keybindings.json` here doesn't touch. If you install it, be aware it ships
its own large set of keybinding overrides — ours take priority for the
C/C++-specific entries only because user `keybindings.json` entries always
beat extension-contributed ones, not because of any ordering between the two
files.
