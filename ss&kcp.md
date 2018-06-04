# SS & Kcptun

## SS

### Installation
Due to regulations, **A WORD** is replaced with **XXX** in the following contents.

`pacman -S` [**XXX**](https://www.archlinux.org/packages/?name=shadowsocks-libev)

### Configuration
Go to `/etc/XXX`, create configuration files.

### Start and stop
`systemctl start XXX@cfg`, the `cfg` refers to the configuration file name without extension.

`systemctl stop XXX@cfg`

## Kcptun
### Installation
The package can be found [here](https://www.archlinux.org/packages/community/x86_64/kcptun/).

### Configuration
This is similar to set up configurations for **XXX**.
Go to `/etc/kcptun`, create your configurations.

### Start and stop
This is also similar to start and stop **XXX**.
```shell
systemctl start kcptun@cfg
systemctl stop kcptun@cfg
``` 