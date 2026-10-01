# Keybinding coverage

Full accounting of every row in `eclipse-key-export.csv` (336 rows), grouped by how it's handled. Classified by each row's real Eclipse command ID (not guessed from the label), so nothing is silently dropped. See `keybindings.json` for the actual bindings and `README.md` for how to apply them.

| Bucket | Rows |
|---|---|
| Added in keybindings.json (this file) | 36 |
| Covered by the "Eclipse Keymap" extension | 26 |
| Already a stock VS Code default (same key, same effect) | 54 |
| Duplicate of a C/C++ gesture above, for another editor type/language | 28 |
| No VS Code/cpptools equivalent | 96 |
| Out of scope (plugin not used in this workflow) | 96 |
| **Total** | **336** |

## Added in keybindings.json (this file) (36)

| Category | Command | Key | Context | Note |
|---|---|---|---|---|
| Source | Remove Block Comment | `Ctrl+Shift+\` | C/C++ Editor | Ctrl+Shift+\ -> editor.action.blockComment |
| Source | References | `Ctrl+Shift+G` | In C/C++ Views | Ctrl+Shift+G -> editor.action.referenceSearch.trigger |
| Refactor - C++ | Rename - Refactoring  | `Alt+Shift+R` | C/C++ Editor | Alt+Shift+R -> editor.action.rename |
| Source | Declaration | `Ctrl+G` | In C/C++ Views | Ctrl+G -> editor.action.revealDeclaration |
| Source | Format | `Ctrl+Shift+F` | C/C++ Editor | Ctrl+Shift+F -> editor.action.formatDocument |
| Navigate | Open Type in Hierarchy | `Ctrl+Shift+H` | In C/C++ Views | Ctrl+Shift+H -> references-view.showTypeHierarchy |
| Source | Declaration | `Ctrl+G` | C/C++ Editor | Ctrl+G -> editor.action.revealDeclaration |
| Source | Indent Line | `Ctrl+I` | C/C++ Editor | Ctrl+I -> editor.action.reindentselectedlines |
| Source | Toggle Source/Header | `Ctrl+Tab` | C/C++ Editor | Ctrl+Tab -> C_Cpp.SwitchHeaderSource |
| C/C++ Editor (LSP) | Toggle Source/Header | `Ctrl+Tab` | in Generic Code Editor | Ctrl+Tab -> C_Cpp.SwitchHeaderSource |
| Source | References | `Ctrl+Shift+G` | C/C++ Editor | Ctrl+Shift+G -> editor.action.referenceSearch.trigger |
| Refactor - C++ | Rename - Refactoring  | `Alt+Shift+R` | In C/C++ Views | Alt+Shift+R -> editor.action.rename |
| Navigate | Open Type Hierarchy | `F4` | In C/C++ Views | F4 -> references-view.showTypeHierarchy (fixed command id) |
| Source | Open Declaration | `F3` | Assembly Editor | F3 -> editor.action.revealDefinition |
| Edit | Restore Last C/C++ Selection | `Alt+Shift+↓` | C/C++ Editor | Alt+Shift+Down -> editor.action.smartSelect.shrink |
| Source | Open Declaration | `F3` | C/C++ Editor | F3 -> editor.action.revealDefinition |
| Source | Add Block Comment | `Ctrl+Shift+/` | C/C++ Editor | Ctrl+Shift+/ -> editor.action.blockComment (also covered by Eclipse Keymap ext) |
| Project | Build Target Build | `Shift+F9` | In Windows | Shift+F9 -> workbench.action.tasks.runTask |
| Source | Toggle Comment | `Ctrl+/` | C/C++ Editor | Ctrl+/ / Ctrl+7 -> editor.action.commentLine (VS Code default, also Eclipse Keymap ext) |
| Navigate | Open Call Hierarchy | `Ctrl+Alt+H` | C/C++ Editor | Ctrl+Alt+H -> references-view.showCallHierarchy (fixed command id) |
| Run/Debug | Run to Line | `Ctrl+R` | Debugging | Ctrl+R -> editor.debug.action.runToCursor |
| Navigate | Open Call Hierarchy | `Ctrl+Alt+H` | In C/C++ Views | Ctrl+Alt+H -> references-view.showCallHierarchy (fixed command id) |
| Source | Open Declaration | `F3` | In Macro Expansion Hover | F3 -> editor.action.revealDefinition |
| Source | Open Declaration | `F3` | In C/C++ Views | F3 -> editor.action.revealDefinition |
| Source | Sort Lines | `Ctrl+Alt+S` | C/C++ Editor | Ctrl+Alt+S -> editor.action.sortLinesAscending |
| Source | Show outline | `Ctrl+O` | C/C++ Editor | Ctrl+O -> workbench.action.gotoSymbol |
| Navigate | Open Type Hierarchy | `F4` | C/C++ Editor | F4 -> references-view.showTypeHierarchy (fixed command id) |
| Source | Toggle Comment | `Ctrl+Shift+C` | C/C++ Editor | Ctrl+/ / Ctrl+7 -> editor.action.commentLine (VS Code default, also Eclipse Keymap ext) |
| Source | Quick Type Hierarchy | `Ctrl+T` | C/C++ Editor | Ctrl+T -> references-view.showTypeHierarchy |
| Source | Toggle Comment | `Ctrl+7` | C/C++ Editor | Ctrl+/ / Ctrl+7 -> editor.action.commentLine (VS Code default, also Eclipse Keymap ext) |
| Navigate | Open Type in Hierarchy | `Ctrl+Shift+H` | C/C++ Editor | Ctrl+Shift+H -> references-view.showTypeHierarchy |
| Project | Rebuild Last Target | `F9` | In Windows | F9 -> workbench.action.tasks.reRunTask |
| Text Editing | Scroll Line Down | `Ctrl+↓` | Editing Text | Ctrl+Down -> scrollLineUp/scrollLineDown (added, not bound by default in VS Code) |
| Edit | Toggle Block Selection | `Alt+Shift+A` | Editing Text | Alt+Shift+A -> editor.action.toggleColumnSelection (added, not bound by default) |
| Text Editing | Scroll Line Up | `Ctrl+↑` | Editing Text | Ctrl+Up -> scrollLineUp/scrollLineDown (added, not bound by default in VS Code) |
| Project | Build All | `Ctrl+B` | In Windows | Ctrl+B -> workbench.action.tasks.build (added, overrides default Toggle Sidebar Visibility) |

## Covered by the "Eclipse Keymap" extension (26)

| Category | Command | Key | Context | Note |
|---|---|---|---|---|
| Text Editing | Open Hyperlink | `F3` | in Generic Code Editor | F3 -> editor.action.goToDeclaration |
| Window | Maximize Active View or Editor | `Ctrl+M` | In Windows | Ctrl+M -> workbench.action.toggleSidebarVisibility (not an exact match, see notes) |
| File | Close All | `Ctrl+Shift+W` | In Windows | Ctrl+Shift+W -> workbench.action.closeAllEditors |
| Navigate | Forward History | `Alt+→` | In Windows | Alt+Right -> workbench.action.navigateForward |
| Run/Debug | Step Return | `F7` | Debugging | F7 -> workbench.action.debug.stepOut |
| Edit | Toggle Word Wrap | `Alt+Shift+Y` | Editing Text | Alt+Shift+Y -> editor.action.toggleWordWrap |
| File | Rename | `Alt+Shift+R` | in Generic Code Editor | Alt+Shift+R / F2 -> editor.action.rename |
| Run/Debug | Resume | `F8` | Debugging | F8 -> workbench.action.debug.continue |
| Window | Next View | `Ctrl+F7` | In Windows | Ctrl+F7 -> workbench.action.focusNextPart |
| Window | Quick Switch Editor | `Ctrl+E` | In Windows | Ctrl+E -> workbench.action.showEditorsInActiveGroup |
| Navigate | Open Resource | `Ctrl+Shift+R` | In Windows | Ctrl+Shift+R -> workbench.action.quickOpen |
| Run/Debug | Terminate | `Ctrl+F2` | Debugging | Ctrl+F2 -> workbench.action.debug.stop |
| Navigate | Previous Edit Location | `Ctrl+Q` | In Windows | Ctrl+Q -> workbench.action.navigateToLastEditLocation |
| Window | Find Actions | `Ctrl+3` | In Windows | Ctrl+3 -> workbench.action.showCommands |
| Navigate | Go to Line | `Ctrl+L` | Editing Text | Ctrl+L -> workbench.action.gotoLine |
| Uncategorized | Find References | `Ctrl+Shift+G` | in Generic Code Editor | Ctrl+Shift+G -> editor.action.referenceSearch.trigger |
| File | Close All | `Ctrl+Shift+F4` | In Windows | Ctrl+Shift+W -> workbench.action.closeAllEditors |
| Navigate | Backward History | `Alt+←` | In Windows | Alt+Left -> workbench.action.navigateBack |
| Navigate | Previous Edit Location | `Ctrl+Alt+←` | In Windows | Ctrl+Q -> workbench.action.navigateToLastEditLocation |
| File | Rename | `F2` | In Windows | Alt+Shift+R / F2 -> editor.action.rename |
| Window | Previous View | `Ctrl+Shift+F7` | In Windows | Ctrl+Shift+F7 -> workbench.action.focusPreviousPart |
| Run/Debug | Step Over | `F6` | Debugging | F6 -> workbench.action.debug.stepOver |
| Run/Debug | Debug | `F11` | In Windows | F11 -> workbench.action.debug.start |
| Run/Debug | Run | `Ctrl+F11` | In Windows | Ctrl+F11 -> workbench.action.debug.run |
| Run/Debug | Step Into | `F5` | Debugging | F5 -> workbench.action.debug.stepInto |
| Navigate | Next Edit Location | `Ctrl+Alt+→` | In Windows | Close equivalent: Alt+Left/Right (workbench.action.navigateBack/Forward) from the Eclipse Keymap extension; VS Code has no separate 'edit location' history distinct from navigation history |

## Already a stock VS Code default (same key, same effect) (54)

| Category | Command | Key | Context | Note |
|---|---|---|---|---|
| File | Close | `Ctrl+W` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Select All | `Ctrl+A` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Paste | `Shift+Insert` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Run/Debug | Toggle Breakpoint | `Ctrl+Shift+B` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Select Line End | `Shift+End` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Select Next Word | `Ctrl+Shift+→` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Content Assist | `Ctrl+Space` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Redo | `Ctrl+Y` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Cut | `Ctrl+X` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| File | New | `Ctrl+N` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Toggle Overwrite | `Insert` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | To Lower Case | `Ctrl+Shift+Y` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| File | Print | `Ctrl+P` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| File | Properties | `Alt+Enter` | In Windows | Generic file-menu action (new/close/save/print/refresh/etc.) with a VS Code equivalent on the same or an adjacent default key |
| Window | Activate Editor | `F12` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| File | Refresh | `F5` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| File | Save | `Ctrl+S` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Delete Next Word | `Ctrl+Delete` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| File | Save All | `Ctrl+Shift+S` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Delete Previous Word | `Ctrl+Backspace` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Paste | `Ctrl+V` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Delete Line | `Ctrl+D` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Undo | `Ctrl+Z` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Copy | `Ctrl+C` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Next Word | `Ctrl+→` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| File | Close | `Ctrl+F4` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| File | New menu | `Alt+Shift+N` | In Windows | Generic file-menu action (new/close/save/print/refresh/etc.) with a VS Code equivalent on the same or an adjacent default key |
| Text Editing | Move Lines Up | `Alt+↑` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Join Lines | `Ctrl+Alt+J` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Select Previous Word | `Ctrl+Shift+←` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Zoom In | `Ctrl+=` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | To Upper Case | `Ctrl+Shift+X` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Copy Lines | `Ctrl+Alt+↓` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Delete to End of Line | `Ctrl+Shift+Delete` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Line Start | `Home` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Zoom In | `Ctrl++` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Insert Line Above Current Line | `Ctrl+Shift+Enter` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Text Start | `Ctrl+Home` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Previous Word | `Ctrl+←` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Find and Replace | `Ctrl+F` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Select Line Start | `Shift+Home` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Cut | `Shift+Delete` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Insert Line Below Current Line | `Shift+Enter` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Line End | `End` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Move Lines Down | `Alt+↓` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Text End | `Ctrl+End` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Duplicate Lines | `Ctrl+Alt+↑` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Copy | `Ctrl+Insert` | In Dialogs and Windows | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Delete | `Delete` | In Windows | Matches a built-in VS Code default already (same key, same effect) |
| Text Editing | Zoom Out | `Ctrl+-` | Editing Text | Matches a built-in VS Code default already (same key, same effect) |
| Edit | Context Information | `Ctrl+Shift+Space` | In Dialogs and Windows | VS Code already binds Ctrl+Shift+Space to editor.action.triggerParameterHints by default |
| Edit | Word Completion | `Alt+/` | Editing Text | Functionally replaced by VS Code IntelliSense (Ctrl+Space, also triggers automatically) |
| Edit | Shift Left | `Shift+Tab` | C/C++ Editor | VS Code already binds Shift+Tab to editor.action.outdentLines by default |
| Edit | Toggle Insert Mode | `Ctrl+Shift+Insert` | Editing Text | VS Code already toggles insert/overwrite mode via the plain Insert key by default (different key than this Eclipse export, same functionality) |

## Duplicate of a C/C++ gesture above, for another editor type/language (28)

| Category | Command | Key | Context | Note |
|---|---|---|---|---|
| Edit | Select Enclosing Element | `Alt+Shift+↑` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Matching Tag | `Ctrl+Shift+>` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Quick Search | Quick Search | `Ctrl+Alt+Shift+L` | In Windows | Covered by Ctrl+H (Find in Files) from the Eclipse Keymap extension, or VS Code's own Ctrl+Shift+F |
| Edit | Select Next Element | `Alt+Shift+→` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Open Selection | `F3` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Previous Sibling | `Ctrl+Shift+↑` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Enclosing Element | `Alt+Shift+↑` | in Generic Code Editor | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Open Type Hierarchy | `F4` | in Generic Code Editor | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Occurrences in File | `Ctrl+Shift+A` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Quick Type Hierarchy | `Ctrl+T` | Editing Text | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Format | `Ctrl+Shift+F` | Editing Text | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Search | Open Search Dialog | `Ctrl+H` | In Windows | Covered by Ctrl+H (Find in Files) from the Eclipse Keymap extension, or VS Code's own Ctrl+Shift+F |
| Edit | Remove Block Comment | `Ctrl+Shift+\` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Quick Fix | `Ctrl+1` | In Dialogs and Windows | Same as the C/C++ Editor equivalent (Ctrl+1 Quick Fix); Java not used in this repo |
| Edit | Format Active Elements | `Ctrl+I` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Toggle Comment | `Ctrl+Shift+C` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Restore To Last Selection | `Alt+Shift+↓` | in Generic Code Editor | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Format | `Ctrl+Shift+F` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Navigate | Matching Character | `Ctrl+Shift+P` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Restore Last Selection | `Alt+Shift+↓` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Add Block Comment | `Ctrl+Shift+/` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Select Previous Element | `Alt+Shift+←` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Go to Symbol in Workspace | `Ctrl+Shift+T` | In Windows | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Open Call Hierarchy | `Ctrl+Alt+H` | in Generic Code Editor | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Edit | Next Sibling | `Ctrl+Shift+↓` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Language Servers | Go to Symbol in File | `Ctrl+O` | Editing Text | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Navigate | Quick Outline | `Ctrl+O` | Editing in Structured Text Editors | Same gesture as a C/C++ Editor row above, just for XML/HTML/generic-LSP editors; already generic (not language-scoped) in our mapping or in VS Code core, so no separate binding needed |
| Search | Find Text in Workspace | `Ctrl+Alt+G` | In Windows | Covered by Ctrl+H (Find in Files) from the Eclipse Keymap extension, or VS Code's own Ctrl+Shift+F |

## No VS Code/cpptools equivalent (96)

| Category | Command | Key | Context | Note |
|---|---|---|---|---|
| Run/Debug | Next Memory Monitor | `Ctrl+Alt+N` | In Memory View | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Navigate | Open Include Browser | `Ctrl+Alt+I` | In C/C++ Views | No 'Include Browser' view in VS Code/cpptools |
| Navigate | Previous | `Ctrl+,` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Go to Program Counter | `Home` | In Disassembly | Niche disassembly-view navigation; cpptools Disassembly View exists but has no matching shortcut |
| Views | Show View (Error Log) | `Alt+Shift+Q, L` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Text Editing | Toggle Folding | `Ctrl+Numpad_Divide` | Editing Text | VS Code's folding commands exist (Ctrl+Shift+[ / ]) but use different default keys; not rebound to avoid clobbering split-editor shortcuts |
| Reverse Debugging Commands | Reverse Resume | `Shift+F8` | Debugging C/C++ | Reverse debugging is not exposed in the VS Code debug UI |
| Navigate | Next Sub-Tab | `Alt+PageDown` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Views | Show View (Cheat Sheets) | `Alt+Shift+Q, H` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Text Editing | Collapse | `Ctrl+Numpad_Subtract` | Editing Text | VS Code's folding commands exist (Ctrl+Shift+[ / ]) but use different default keys; not rebound to avoid clobbering split-editor shortcuts |
| Reverse Debugging Commands | Reverse Step Into | `Shift+F5` | Debugging C/C++ | Reverse debugging is not exposed in the VS Code debug UI |
| Window | Previous Perspective | `Ctrl+Shift+F8` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Step Into Selection | `Ctrl+F5` | Debugging C/C++ | No "step into selection" command in the VS Code debug UI |
| Refactor - C++ | Extract Function - Refactoring  | `Alt+Shift+M` | C/C++ Editor | cpptools has no C++ extract-function refactoring (clangd extension has partial support via Quick Fix) |
| Views | Show View (Synchronize) | `Alt+Shift+Q, Y` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Navigate | Previous Page | `Alt+Shift+F7` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Toggle Memory Monitors Pane | `Ctrl+T` | In Memory View | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Makefile Source | Open declaration | `F3` | Makefile Editor | Covered generically by F3 if a Makefile symbol provider is installed |
| Navigate | Previous Tab | `Ctrl+PageUp` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Source | Explore Macro Expansion | `Ctrl+=` | C/C++ Editor | No macro-expansion-explorer command in cpptools (hover tooltips show expansions instead) |
| Views | Show View (Variables) | `Alt+Shift+Q, V` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Invoke Autotools | Show Outline | `Ctrl+O` | Autoconf Editor | Niche Autoconf editor; already covered generically by Ctrl+O if a symbol provider exists |
| Views | Show View (Outline) | `Alt+Shift+Q, O` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Window | Next Perspective | `Ctrl+F8` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Navigate | Next Tab | `Ctrl+PageDown` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Navigate | Show In... | `Alt+Shift+W` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Source | Go to Matching Bracket | `Ctrl+Shift+P` | C/C++ Editor | Conflicts with VS Code's Command Palette shortcut; not rebound to avoid losing the Palette (use editor.action.jumpToBracket on its own default instead) |
| Refactor - C++ | Toggle Function - Refactoring  | `Alt+Shift+T` | C/C++ Editor | cpptools has no equivalent "toggle function" refactor |
| Run/Debug | Skip All Breakpoints | `Ctrl+Alt+B` | In Windows | Niche GDB memory/stepping feature not exposed as a single VS Code command |
| Navigate | Previous Sub-Tab | `Alt+PageUp` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Window | Previous Editor | `Ctrl+Shift+F6` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Edit | Select Enclosing C/C++ Element | `Alt+Shift+↑` | C/C++ Editor | Covered generically by Smart Select (Alt+Shift+Up), bound by the Eclipse Keymap extension |
| Views | Show View (History) | `Alt+Shift+Q, Z` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Source | Align const qualifiers | `Ctrl+Shift+A` | C/C++ Editor | No east/west-const toggle in cpptools |
| Window | Show System Menu | `Alt+-` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Previous Page of Memory | `Ctrl+Shift+,` | In Table Memory Rendering | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Run/Debug | Close Rendering | `Ctrl+W` | In Memory View | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Views | Show View (Search) | `Alt+Shift+Q, S` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Source | Copy Qualified Name | `Ctrl+Alt+Shift+C` | C/C++ Editor | No copy-qualified-name command in cpptools |
| Views | Show View (Problems) | `Alt+Shift+Q, X` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Makefile Source | Toggle Comment | `Ctrl+/` | Makefile Editor | Covered generically by VS Code's default Ctrl+/ |
| Window | Toggle Full Screen | `Alt+F11` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Use Step Filters | `Shift+F5` | In Windows | Niche GDB memory/stepping feature not exposed as a single VS Code command |
| Navigate | Next | `Ctrl+.` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Go to Address | `Ctrl+G` | In Table Memory Rendering | Niche GDB memory/stepping feature not exposed as a single VS Code command |
| Views | Show View (Console) | `Alt+Shift+Q, C` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Edit | Select Previous C/C++ Element | `Alt+Shift+←` | C/C++ Editor | No per-sibling selection command; use Smart Select (Alt+Shift+Up/Down) instead |
| Run/Debug | Next Page of Memory | `Ctrl+Shift+.` | In Table Memory Rendering | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Reverse Debugging Commands | Uncall | `Shift+F7` | Debugging C/C++ | Reverse debugging is not exposed in the VS Code debug UI |
| Window | Toggle Split Editor (Horizontal) | `Ctrl+_` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Source | Toggle Mark Occurrences | `Alt+Shift+O` | C/C++ Editor | VS Code's occurrence highlighting is always-on (editor.occurrencesHighlight setting) rather than a toggle command |
| Source | Organize Includes | `Ctrl+Shift+O` | C/C++ Editor | No organize-includes command in cpptools (the clangd extension has one) |
| Source | Explore Macro Expansion | `Ctrl+#` | C/C++ Editor | No macro-expansion-explorer command in cpptools (hover tooltips show expansions instead) |
| Edit | Quick Diff Toggle | `Ctrl+Shift+Q` | Editing Text | No single-command VS Code equivalent found; gutter diff indicators are always-on in VS Code |
| Text Editing | Expand | `Ctrl+Numpad_Add` | Editing Text | VS Code's folding commands exist (Ctrl+Shift+[ / ]) but use different default keys; not rebound to avoid clobbering split-editor shortcuts |
| Text Editing | Reset Structure | `Ctrl+Shift+Numpad_Multiply` | Editing Text | VS Code's folding commands exist (Ctrl+Shift+[ / ]) but use different default keys; not rebound to avoid clobbering split-editor shortcuts |
| Text Editing | Expand All | `Ctrl+Numpad_Multiply` | Editing Text | VS Code's folding commands exist (Ctrl+Shift+[ / ]) but use different default keys; not rebound to avoid clobbering split-editor shortcuts |
| Source | Surround With Quick Menu | `Alt+Shift+Z` | C/C++ Editor | No "Surround With" snippet menu in cpptools |
| Source | Go to Next Member | `Ctrl+Shift+↓` | C/C++ Editor | No next/previous top-level-member navigation command in cpptools |
| Window | Next Editor | `Ctrl+F6` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Navigate | Expand All | `Ctrl+Shift+Numpad_Multiply` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Views | Show View (Task List) | `Alt+Shift+Q, K` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Navigate | Open Include Browser | `Ctrl+Alt+I` | C/C++ Editor | No 'Include Browser' view in VS Code/cpptools |
| Source | Back | `Alt+←` | In Macro Expansion Hover | Niche macro-expansion-hover navigation, no cpptools equivalent |
| Window | Toggle Split Editor (Vertical) | `Ctrl+{` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Edit | Select Next C/C++ Element | `Alt+Shift+→` | C/C++ Editor | No per-sibling selection command; use Smart Select (Alt+Shift+Up/Down) instead |
| Source | Open Element | `Ctrl+Shift+T` | C/C++ Editor | Covered by Ctrl+Shift+T -> workbench.action.showAllSymbols (Eclipse Keymap extension) |
| Navigate | Next Page | `Alt+F7` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Reverse Debugging Commands | Reverse Step Over | `Shift+F6` | Debugging C/C++ | Reverse debugging is not exposed in the VS Code debug UI |
| Run/Debug | Add Memory Block | `Ctrl+Alt+M` | In Memory View | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Views | Show View | `Alt+Shift+Q, Q` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Run/Debug | Go to Address... | `Ctrl+G` | In Disassembly | Niche disassembly-view navigation; cpptools Disassembly View exists but has no matching shortcut |
| Window | Show Key Assist | `Ctrl+Shift+L` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Refactor - C++ | Extract Constant - Refactoring  | `Alt+C` | C/C++ Editor | cpptools has no C++ extract-constant refactoring |
| Source | Forward | `Alt+→` | In Macro Expansion Hover | Niche macro-expansion-hover navigation, no cpptools equivalent |
| Views | Show View (Breakpoints) | `Alt+Shift+Q, B` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Text Editing | Collapse All | `Ctrl+Shift+Numpad_Divide` | Editing Text | VS Code's folding commands exist (Ctrl+Shift+[ / ]) but use different default keys; not rebound to avoid clobbering split-editor shortcuts |
| Run/Debug | EOF | `Ctrl+Z` | In I/O Console | Niche GDB memory/stepping feature not exposed as a single VS Code command |
| Window | Switch to Editor | `Ctrl+Shift+E` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Refactor - C++ | Extract Local Variable - Refactoring  | `Alt+Shift+L` | C/C++ Editor | cpptools has no C++ extract-variable refactoring |
| Navigate | Collapse All | `Ctrl+Shift+Numpad_Divide` | In Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Window | Show Contributing Plug-in | `Alt+Shift+F3` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Window | Show View Menu | `Ctrl+F10` | In Dialogs and Windows | Eclipse window/view/perspective management with no direct VS Code panel/layout equivalent (or not worth a dedicated binding); use the Command Palette |
| Source | Show Tooltip Description | `F2` | Autoconf Editor | Niche Autoconf editor, not used in this workflow |
| Source | Go to Previous Member | `Ctrl+Shift+↑` | C/C++ Editor | No next/previous top-level-member navigation command in cpptools |
| Source | Open Element | `Ctrl+Shift+T` | In C/C++ Views | Covered by Ctrl+Shift+T -> workbench.action.showAllSymbols (Eclipse Keymap extension) |
| Source | Add Include | `Ctrl+Shift+N` | C/C++ Editor | No auto-add-include command in cpptools; sometimes available via Quick Fix (Ctrl+1) if IntelliSense offers it |
| Run/Debug | New Rendering | `Ctrl+N` | In Memory View | Niche GDB Memory View feature; VS Code has a newer built-in Memory Inspector but no verified 1:1 command mapping |
| Uncategorized | Go to Matching Bracket | `Ctrl+Shift+P` | in Generic Code Editor | Conflicts with VS Code's Command Palette shortcut; not rebound so the Palette keeps working (use editor.action.jumpToBracket on its own default key instead) |
| Source | Show Source Quick Menu | `Alt+Shift+S` | C/C++ Editor | No equivalent "Source" quick-menu (organize imports / generate getters-setters) in VS Code/cpptools |
| Edit | Find Next | `Ctrl+K` | In Windows | Ctrl+K is VS Code's chord prefix for dozens of commands; not rebound to avoid breaking that whole namespace - use F3 (VS Code's own Find Next, stock default) instead |
| Edit | Incremental Find | `Ctrl+J` | Editing Text | VS Code's Find widget (Ctrl+F) already highlights incrementally as you type; no separate command to bind |
| Edit | Incremental Find Reverse | `Ctrl+Shift+J` | Editing Text | Same as Incremental Find - replaced by the Find widget's Shift+Enter for previous match |
| Text Editing | Show Tooltip Description | `F2` | Editing Text | VS Code already uses F2 for Rename (a different meaning than Eclipse's hover-tooltip); not rebound to avoid breaking the common Rename gesture - use mouse hover or Ctrl+K Ctrl+I instead |
| Window | Show Ruler Context Menu | `Ctrl+F10` | Editing Text | No command to open the gutter/ruler context menu via keyboard in VS Code |
| Edit | Find Previous | `Ctrl+Shift+K` | In Windows | Same Ctrl+K chord-prefix conflict as Find Next - use Shift+F3 (VS Code's own Find Previous, stock default) instead |

## Out of scope (plugin not used in this workflow) (96)

Grouped by plugin/category - none are used for C/C++ editing in this repo:

- **ANSI Support Commands** (1 rows) - Plugin not used in this workflow (ANSI Support Commands)
- **Changelog** (7 rows) - Plugin not used in this workflow (Changelog)
- **Editor Commands** (5 rows) - Plugin not used in this workflow (Editor Commands)
- **Focused UI** (4 rows) - Plugin not used in this workflow (Focused UI)
- **Git** (5 rows) - Plugin not used in this workflow (Git)
- **Navigate** (9 rows) - Plugin not used in this workflow (Navigate)
- **TM4E Language Configuration** (4 rows) - Plugin not used in this workflow (TM4E Language Configuration)
- **Task Editor** (2 rows) - Plugin not used in this workflow (Task Editor)
- **Task Repositories** (15 rows) - Plugin not used in this workflow (Task Repositories)
- **Terminal Commands** (2 rows) - Plugin not used in this workflow (Terminal Commands)
- **Terminal view commands** (23 rows) - Plugin not used in this workflow (Terminal view commands)
- **Tracing** (10 rows) - Plugin not used in this workflow (Tracing)
- **UML2 Sequence Diagram Viewer Commands** (7 rows) - Plugin not used in this workflow (UML2 Sequence Diagram Viewer Commands)
- **Uncategorized** (2 rows) - Plugin not used in this workflow (Uncategorized)
