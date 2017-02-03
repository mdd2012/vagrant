# ubuntu16.04LTSのBOXを取得して、gnomeデスクトップを上げる
## 前提
- 以下のバージョンで稼働確認しました。
  - Windows10
    - vagrant  1.8.1
    - VirtualBox 5.0.12

## 手順
### Ubuntu 16.04 LTSのサーバーイメージのBOXを取得する  
  - ubuntu_box_get.bat(Windows)やubuntu_box_get.sh(Linux、Mac)でBOXイメージ取得
```
# Windowsの場合
ubuntu_box_get_16_04.bat
# LinuxやMacの場合
ubuntu_box_get_16_04.sh
```
  - 取得できたかどうかは、以下のコマンドで確認
```
$ vagrant box list
ubuntu16_04_64 (virtualbox, 0)
```
### カレントディレクトリにVagrantfile、localhost、site.ymlを置いた状態でvagrant up!!  
```
$ vagrant up
```
### 仮想マシンが立ち上がったら、ローカルでsshログインして UbuntuLinux上で ansible-playbookコマンドでプロビジョニング実施  
```
$ vagrant ssh

vagrant@vagrant-ubuntu-xxxx-64:~$ cd provision
vagrant@vagrant-ubuntu-xxxx-64:~$ ./provision.sh
vagrant@vagrant-ubuntu-xxxx-64:~$ exit
```
### 仮想マシンのリロード  
```
$ vagrant reload
```
これで、VirtualBOXの画面側にUbuntuLinuxのデスクトップが表示されるはず。
![画面イメージ](img/ubuntu_desktop.PNG "イメージ")

## 参考URL
- [Qiita:VagrantでGUIを有効にする - Qiita](http://qiita.com/WizowozY/items/3f3e5d4065c548db3e54)
- [Qiita:AnsibleをUbuntuのローカルで使う](http://qiita.com/itiut@github/items/e8b95ac9b9ea2a6ea701)
