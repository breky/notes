## Ubuntun 18.04 LTS 设置

### 单击已打开应用的状态栏图标

Ubuntu 18.04 LTS 默认不能单击已打开应用的图标以最小化，用以下命令启用。

```shell
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```
