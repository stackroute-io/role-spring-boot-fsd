sagarpatke.role_spring_boot_fsd
=========

A role to install necessary tools for Spring Boot Full Stack Development.

Installs the following:
- OpenJDK 8 and 12
- Maven
- MongoDB
- MySQL and MySQL Workbench
- Spring Tool Suite 4
- NodeJS 10
- Sublime Text 3
- Atom
- Microsoft Visual Studio Code
- Google Chrome
- Mozilla Firefox
- Slack
- Docker and docker-compose
- git
- vim
- curl
- wget

Requirements
------------

User `ubuntu` must be present before running this script.

Role Variables
--------------

```
slack_version: "4.0.0"
```
Specifies the version of slack to install

Dependencies
------------
```
- role: geerlingguy.nodejs
  nodejs_install_npm_user: ubuntu
- role: chaosmail.sublime-text
  sublime_package_control: false
- andrewrothstein.atom
- ngetchell.vscode
- cmprescott.chrome
- arknoll.firefox
- role: geerlingguy.docker
  docker_users:
    - ubuntu
```

Example Playbook
----------------

```
- hosts: all
  become: true
  roles:
    - role: sagarpatke.role_spring_boot_fsd
```


License
-------

MIT

Author Information
------------------

- [Sagar Patke](https://github.com/sagarpatkeatl)
