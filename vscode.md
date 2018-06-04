# Visual studio code

## Installation
There are no microsoft release version for archlinux.
However, several [aur packages](https://aur.archlinux.org/packages/?O=0&K=visual+studio+code) are available.

The [visual-studio-code-bin](https://aur.archlinux.org/packages/visual-studio-code-bin/) is used in this installation.

To install packages from aur, you have to follow the instructions from [archwiki](https://wiki.archlinux.org/index.php/Arch_User_Repository#Installing_packages).

A valid git installation is recommended.

If the command `makepkg -si` exits with exceptions, go check if the current user belongs to [sudoers](https://wiki.archlinux.org/index.php/Sudo#View_current_settings).


## Font modification
The default installation of visual studio code uses a fixed-width font over the whole ui, which looks really ugly. 

You can modify the default font of the main editor as well as terminals via configuration files. But other ui components like notification windows are not configurable by the same way.

You have to modify the css file of vscode.

Warning: such a modification will cause a integrity issue of visual studio code, which turns visual studio code into an `unsupported` version. However, the modification will do no harm to your system, neither to your vscode.

To continue, make sure you logged in as root or the current user belongs to sudoers. 

The file locates in `/opt/visual-studio-code/resources/app/out/vs/workbench` named as `workbench.main.css`. Launch a editor with root privilege to modify the file, e.g. `sudo vim workbench.main.css`. 

1. Add a font configuration at the first line:
```css
html { font-family: 'your font name'; }
```

2. Remove font configuration for `.monaco-shell`:
    1. Search `.monaco-shell{`
    2. Just before the nearest `}`, you can see a configuration for `font-family` like this: `font-family:-apple-system...`, remove it.

3. Save and exit. Start visual studio code.

