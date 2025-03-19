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

<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>category_normal='<font style="font-family: NotoSans Nerd Font;"></font> '
category_removed='<font style="font-family: NotoSans Nerd Font;"></font> '
category_git='<font style="font-family: NotoSans Nerd Font;"></font> '
package_status_init='<font style="font-family: NotoSans Nerd Font;"></font> '
package_status_normal='<font style="font-family: NotoSans Nerd Font;"></font> '</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="category_normal=' '
category_removed=' '
category_git=' '
package_status_init=' '
package_status_normal=' '" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>

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

This is the result of running `vimpacks list` with default configuration.

This is the result of running `vimpacks list` with the icons set to the font glyph of `nerd-fonts`.

## Example

Below is an image of the configuration screen capture when `nerd-fonts` is installed.

<p style="background-color: #300A24;"><img src="images/ex01.png?raw=true" width="423" /></p>

<p style="background-color: #300A24;"><img src="images/ex02.png?raw=true" width="423" /></p>

<p style="background-color: #300A24;"><img src="images/ex03.png?raw=true" width="423" /></p>

<p style="background-color: #300A24;"><img src="images/ex04.png?raw=true" width="423" /></p>
