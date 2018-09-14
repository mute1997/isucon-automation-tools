# isucon-automation-tools
## 準備
- ansible_ssh_userを設定する
- hostsを編集する

```
$ ansible-playbook -i hosts --ask-pass --ask-become-pass backup.yml
$ ansible-playbook -i hosts --ask-pass --ask-become-pass site.yml
$ ansible-playbook -i hosts --ask-pass --ask-become-pass deploy.yml
```
