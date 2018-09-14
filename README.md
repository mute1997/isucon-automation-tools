# isucon-automation-tools
## 準備
- ansible_ssh_userを設定する
- hostsを編集する

```
$ ssh {ユーザー名}@{DBホスト名} mysqldump --single-transaction -u DBユーザ名 -p DB名 > init.sql
$ scp -r {ユーザー名}@{DBホスト名}:init.sql ~/init.sql
$ scp {ユーザー名}@{DBホスト名}:/etc/my.cnf ~/my.cnf.0
$ scp {ユーザー名}@{DBホスト名}:/etc/mysql/my.cnf ~/my.cnf.1
$ scp -r {ユーザー名}@{APPホスト名}:/etc/nginx/ ~/nginx
$ scp {ユーザー名}@{APPホスト名}:{アプリのパス} ~/app
$ ansible-playbook -i hosts --ask-pass --ask-become-pass site.yml
$ ansible-playbook -i hosts --ask-pass --ask-become-pass deploy.yml
```
