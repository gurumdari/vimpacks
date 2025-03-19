# Vimpacks
<p align="center"><img src="images/logo.png?raw=true" width="728" /></p>

From VIM 8 version, packages can be managed with native-pack built into VIM.

If VIM settings are managed in the GIT repository, and native-pack packages are integrated and managed as sub modules, even if a new environment is built, almost all settings are completed by simply cloning the VIM settings from the remote GIT repository. Despite these advantages, if you are not familiar with GIT commands, you may find it more difficult, and the GIT commands are rather long, making them difficult to use. And you should always use GIT commands in the `.vim` directory.

Vimpacks is a wrapping tool that allows you to process VIM settings managed by remote GIT anywhere with simple commands, regardless of the working location.

## Installation
```
$ cd /usr/local/bin
$ sudo wget https://github.com/gurumdari/vimpacks/releases/latest/download/vimpacks
$ chmod +x vimpacks
```

## Configuration
Vimpacks configuration can be done in the `~/.vim/vimpacks.cfg` file.

```
branch='master'
default_category='plugins/start'
category_normal='📂'
category_removed='🗑️'
category_git='🔀'
package_status_init=' '
package_status_normal='📦'
package_status_weight=127215
package_status_indent='   '
package_status_space=' '
```

The above is the basic configuration of vimpacks, and only the parts different from the default value can be set in the `~/.vim/vimpacks.cfg` file.

> <code>category_normal='<font style="font-family: NotoSans Nerd Font;"></font> '<br>category_removed='<font style="font-family: NotoSans Nerd Font;"></font> '<br>category_git='<font style="font-family: NotoSans Nerd Font;"></font> '<br>package_status_init='<font style="font-family: NotoSans Nerd Font;"></font> '<br>package_status_normal='<font style="font-family: NotoSans Nerd Font;"></font> '</code>

You need to install `nerd-fonts` to properly see the icons in the above settings.

### **package_status_weight**
Letter Status Icon | package_status_weight
-- | --
`A` &nbsp; (65)<br>`D` &nbsp; (68)<br>`M` &nbsp; (77) | `0` &nbsp; (65 - 65)
`a` &nbsp; (97)<br>`d` &nbsp; (100)<br>`m` &nbsp; (109) | `32` &nbsp; (97 - 65)
`Ⓐ` &nbsp; (9398)<br>`Ⓓ` &nbsp; (9401)<br>`Ⓜ` &nbsp; (9410) | `9333` &nbsp; (9398 - 65)
`🄰` &nbsp; (127280)<br>`🄳` &nbsp; (127283)<br>`🄼` &nbsp; (127292) | `127215` &nbsp; (127280 - 65)
`𝒜` &nbsp; (119964)<br>`𝒟` &nbsp; (119967)<br>`𝒨` &nbsp; (119976) | `119899` &nbsp; (119964 - 65)
`𝓪` &nbsp; (120042)<br>`𝓭` &nbsp; (120045)<br>`𝓶` &nbsp; (120054) | `119977` &nbsp; (120042 - 65)

## Example

Below is an image of the configuration screen capture when `nerd-fonts` is installed.

<p style="background-color: #300A24;"><img src="images/ex01.png?raw=true" width="423" /></p>

<p style="background-color: #300A24;"><img src="images/ex02.png?raw=true" width="423" /></p>

<p style="background-color: #300A24;"><img src="images/ex03.png?raw=true" width="423" /></p>

<p style="background-color: #300A24;"><img src="images/ex04.png?raw=true" width="423" /></p>
