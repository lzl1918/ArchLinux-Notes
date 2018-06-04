# Powershell

## Installation
Currently, there are no microsoft release for archlinux. However, the public release for ubuntu 17.04 can be used.

Before installation, make sure you have [dotnet core sdk](https://www.archlinux.org/packages/community/any/dotnet-sdk/) installed in your machine.

1. Download the deb file for ubuntu 17.04 from the [github page](https://github.com/PowerShell/PowerShell/releases).

2. Unzip the deb file

    `bsdtar xf <file>`

    If the operation throws an error of `Failed to set default locale`, export the `LANG` first.
    
    `export LANG=en_US.UTF-8`

    After the operation, you will get `data.tar.gz` in the output directory.
3. Unzip `data.tar.gz`
    
    `bsdtar xf data.tar.gz`

    copy and combine the unzipped directories `opt` and `usr` to `/opt` and `/usr` respectively.

4. Test if `pwsh` works.
    
    Change the current directory to `/opt/microsoft/powershell/<version>/`, and run `dotnet pwsh.dll` to see if `pwsh` works correctly.

5. Make a symbol link

    `ln -s /opt/microsoft/powershell/<version>/pwsh /usr/bin/pwsh`
