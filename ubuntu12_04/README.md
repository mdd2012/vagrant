# ubuntu12.04LTS��BOX���擾���āAgnome�f�X�N�g�b�v���グ��
## �O��
- �ȉ��̃o�[�W�����ŉғ��m�F���܂����B
  - Windows
    - Vagrant 1.7.4
    - Oracle VirtualBOX for Win 4.3.12
    - msysGit 2.0.0

## �菇
1. Ubuntu 12.04 LTS�̃T�[�o�[�C���[�W��BOX���擾����
- ubuntu_box_get.bat(Windows)��ubuntu_box_get.sh(Linux�AMac)��BOX�C���[�W�擾
- �擾�ł������ǂ����́A�ȉ��̃R�}���h�Ŋm�F
```
$ vagrant box list
ubuntu64 (virtualbox, 0)
```
	
2. �J�����g�f�B���N�g����Vagrantfile�Alocalhost�Asite.yml��u������Ԃ�vagrant up!!
```
vagrant up
```

3. ���z�}�V���������オ������A���[�J����ssh���O�C������ UbuntuLinux��� ansible-playbook�R�}���h�Ńv���r�W���j���O���{
```
$ vagrant ssh

vagrant@vagrant-ubuntu-precise-64:~$ cd provision
vagrant@vagrant-ubuntu-precise-64:~$ ansible-playbook site.yml -i localhost
```
4. ���z�}�V���̃����[�h
```
$ vagrant reload
```


## �Q�lURL
- [Qiita:Vagrant��GUI��L���ɂ��� - Qiita](http://qiita.com/WizowozY/items/3f3e5d4065c548db3e54)
- [Qiita:Ansible��Ubuntu�̃��[�J���Ŏg��](http://qiita.com/itiut@github/items/e8b95ac9b9ea2a6ea701)
