# Ansible Role: PHP PEAR packages

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Installs PHP PEAR packages on servers with PHP and `php-pear` already installed.

## Requirements

PHP and `php-pear` (or the equivalent) must already be installed on the server, so the `pear` command can be run.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_pear_channels:
      - pear.phing.info

(Defaults to empty list (`[]`).) The PEAR channels that should be discovered so pear libraries can be installed. By default, PEAR is not configured to autodiscover channels for libraries you would like installed, so you need to explicitly list all the libraries' channels here.

    php_pear_libraries:
      - phing

(Defaults to empty list (`[]`).) The libraries/extensions you would like installed via PEAR.

## Dependencies

  - nholuong.php

## Example Playbook

```yaml
---
- hosts: webservers

  vars_files:
    - vars/main.yml

  roles:
    - nholuong.php-pear
```

*Inside `vars/main.yml`*:

```yaml
php_pear_channels:
  - pear.phpunit.de

php_pear_libraries:
  - phpunit/PHPUnit
```

## TODO

  - Continue refining the `changed`/`failed` conditions for PEAR. Yuck.

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
