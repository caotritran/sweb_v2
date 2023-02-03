LEMP compile with Nginx fastcgi caching + php-fpm + mariadb + wordpress + another module third Nginx:
- Nginx nginx-1.23.3
- PHP php-8.1.15
- Mariadb 10.5
- Wordpress latest

`Usage:`

`install:` **ansible-playbook main.yml -i hosts --skip-tags "template-2, template-phpfpm"**

`create new vhost seconds:`
edit file group_vars/all with variables as:
- user_domain 
- server_name
- group_domain
- mysql_database
- mysql_user

`run playbook:` **ansible-playbook main.yml -i hosts --tags "vhost, mariadb, template-2, template-phpfpm, wp"**

`Note:`

File hosts just example, You can edit match with information your Server/VPS
