<p align="center"><img src="images/rebranded75.png?raw=true" width="570" /></p>

> <span style="color: #FF0000">⚠  <span style="text-decoration: line-through; text-decoration-color: #808080">vimpacks</span> has been rebranded as **_vimmy_**.</span>

> 🌐 **_vimmy_**: [https://github.com/gurumdari/vimmy](https://github.com/gurumdari/vimmy)

**_vimmy_** is the tool to integrate vim configuration via git, highly configurable and easy to use experience.

From vim 8 version, packages can be managed with native-pack built into vim.

If vim configuration are managed in the git repository, and native-pack packages are integrated and managed as sub modules, even if a new environment is built, almost all settings are completed by simply cloning the vim configuration from the remote git repository. Despite these advantages, if you are not familiar with git commands, you may find it more difficult, and the git commands are rather long, making them difficult to use. And you should always use git commands in the `.vim` directory.

**_vimmy_** is a wrapping tool that allows you to process vim configuration managed by remote git repository, anywhere with simple commands, regardless of the working location.

## Installation
```
$ cd /usr/local/bin
$ sudo wget https://github.com/gurumdari/vimpacks/releases/latest/download/vimpacks
$ sudo chmod +x vimpacks
```

## Configuration
**_vimpacks_** configuration can be done in the `~/.vim/vimpacks.cfg` file.
```
branch='main'
default_category='plugins/start'
category_normal='📂'
category_removed='🗑️'
category_git='🔀'
package_status_init='㊀'
package_status_normal='📦'
package_status_weight=127215
package_status_indent='   '
package_status_space=' '
```

The above is the basic configuration of **_vimpacks_**, and only the parts different from the default value can be set in the `~/.vim/vimpacks.cfg` file.

```
category_normal=' '
category_removed=' '
category_git=' '
package_status_init=' '
package_status_normal=' '
```

You need to install Nerd Fonts to properly see the icons in the above settings.

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

Below is an image of the configuration screen capture when Nerd Fonts is installed.

<p>
	<div><img src="images/ex01.png?raw=true" width="690" /></div>
	<div><img src="images/ex02.png?raw=true" width="690" /></div>
</p>
<p><img src="images/ex03.png?raw=true" width="690" /></p>
<p><img src="images/ex04.png?raw=true" width="690" /></p>