# Vimpacks
VIM 8 버전부터 VIM에 내장된 native-pack으로 package들을 관리할 수 있다. 

VIM의 설정들을 GIT의 Repository에서 모아 관리하면서, native-pack의 Package들까지 Sub module로 통합 관리하고 있다면, 새로 환경이 구축되더라도, VIM 설정을 리모트 GIT의 Repository로부터 복제만 해오면 거의 모든 설정이 완성되는 장점이 있다. 그러나 GIT 명령어에 익숙하지 못하면 오히려 더 어렵게 느낄 수 있고, GIT 명령어도 다소 길어서 사용하기 힘들다. 그리고 항상 .vim 디렉토리에서 GIT 명령어를 사용해야 한다.

Vimpacks는 작업 위치와 상관없이 어디에서나 리모트 GIT으로 관리되는 VIM의 설정들을 간단한 명령어로 처리할 수 있게 해주는 래핑 툴이다.

## 설치
```
$ cd /usr/local/bin
$ sudo wget https://github.com/gurumdari/vimpacks/releases/latest/download/vimpacks
$ chmod +x vimpacks
```

## 설정
Vimpacks의 환경설정은 `~/.vim/vimpacks.cfg` 파일에 할 수 있다.
```
branch='master'
default_category='plugins/start'
category_normal='📂'
category_removed='🗑 '
package_status_init='㊀'
package_status_normal='◯ '
package_status_weight=9333
package_status_indent='   '
package_status_space=' '
```

위는 Vimpacks의 기본 환경설정으로써, 기본값과 다른 부분만 `~/.vim/vimpacks.cfg` 파일에 설정하면 된다. 아래의 설정들은 `nerd-fonts`가 설치되어 있어야 아이콘들이 제대로 보인다.

```
category_normal=' '
category_removed=' '
package_status_init=' '
package_status_normal=' '
package_status_weight=127215
```

### package_status_weight
Letter Status Icon | package_status_weight
-- | --
`A` &nbsp; (65)<br>`D` &nbsp; (68)<br>`M` &nbsp; (77) | `0` &nbsp; (65 - 65)
`a` &nbsp; (97)<br>`d` &nbsp; (100)<br>`m` &nbsp; (109) | `32` &nbsp; (97 - 65)
`Ⓐ` &nbsp; (9398)<br>`Ⓓ` &nbsp; (9401)<br>`Ⓜ` &nbsp; (9410) | `9333` &nbsp; (9398 - 65)
`🄰` &nbsp; (127280)<br>`🄳` &nbsp; (127283)<br>`🄼` &nbsp; (127292) | `127215` &nbsp; (127280 - 65)
`𝒜` &nbsp; (119964)<br>`𝒟` &nbsp; (119967)<br>`𝒨` &nbsp; (119976) | `119899` &nbsp; (119964 - 65)
`𝓪` &nbsp; (120042)<br>`𝓭` &nbsp; (120045)<br>`𝓶` &nbsp; (120054) | `119977` &nbsp; (120042 - 65)

## 사용예