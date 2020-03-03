# ansible管理用のLinuxをつくる
## できること
- ansibleで他環境を管理するためのLinuxイメージを作成
- vagrantでubuntu boxをもってきて、Ansibleを入れる
- Playbookなどの編集はviとかでいいかなと

## 作り方
0. 前提
  - ローカル環境へvagrantとVirtualBoxを入れておくこと
  
1. ubuntuのboxをもってくる。
  - ubuntu_box_get_xx_04.bat(Windows)やubuntu_box_get_xx_04.sh(Linux)でBOXを取得

2. vagrant upすると、ansibleの最新版を自動インストールしたubuntuが上がる
