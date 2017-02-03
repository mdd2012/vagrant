# ansible管理用のLinuxをつくる
## できること
- ansibleで他環境を管理するためのLinuxイメージを作成
- vagrantでubuntu boxをもってきて、Ansible2.0を入れる
- Playbookなどの編集はviとかでいいかなと

## 作り方
0. 前提
  - vagrantとVirtualBoxを入れておくこと
  
1. ubuntu 16.04のboxをもってくる。
  - ubuntu_box_get_16_04.bat(Windows)やubuntu_box_get_16_04.sh(Linux)でBOXを取得

2. vagrant upすると、ansibleの最新版を自動インストールしたubuntuが上がる
