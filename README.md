# Fresh Nix Language Pack
This is a language pack for the [Fresh](https://getfresh.dev/) ([github](https://github.com/sinelaw/fresh)) tui text editor.
It has syntax highlighting, formatting and LSP.
## Features
* **Syntax Highlighting:** Credits: [wmertens](https://github.com/wmertens)/[sublime-nix](https://github.com/wmertens/sublime-nix), which I converted to sublime-syntax from tmLanguage
* **Language Server Integration:** Using (https://github.com/oxalica)/[nil](https://github.com/oxalica/nil)
* **Auto-Formatting:** Using [NixOS](https://github.com/NixOS)/[nixfmt](https://github.com/NixOS/nixfmt)
---
## Prerequisites
To get the **full** experience (LSP and Formatting), you need to have the following tools installed on your system. If you are on NixOS, add these to your `environment.systemPackages` or `home.packages`:
- **[nil](https://github.com/oxalica/nil)**: The Nix Language Server. This provides the completions and so on..
- **[nixfmt](https://github.com/nix-community/nixfmt)**: The standard Nix code formatter.
### NixOS Setup:
```nix
environment.systemPackages = with pkgs; [
  nil
  nixfmt
];
```
### Home Manager Setup:
```nix
home.packages = with pkgs; [
  nil
  nixfmt
];
```
## Grammar Attribution
The syntax grammar is derived from [original-package]([https://github.com/user/repo](https://github.com/wmertens/sublime-nix))
by [wmertens](https://github.com/wmertens), licensed under MIT. See `grammars/LICENSE` for details.
