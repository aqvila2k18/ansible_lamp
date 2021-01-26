# ansible_lamp
Ansible LAMP

Файл hosts.txt - фал инвентаризации, переменные ansible_host нужно заменить или прописать ip в /etc/hosts
linux-1 ansible_host=linux-1
linux-2 ansible_host=linux-2

Файлы переменных:
group_vars/db-server
  sudo пользователь:                       ansible_user:  ubuntu
  путь к ssh ключу:                        ansible_ssh_private_key_file:  /home/ubuntu/.ssh/ansible.pem
  пароль от рут mysql:                     mysql_root_password:  "root_password"
  пароль от ползователя BD для wordpress:  mysql_password:  "password"
  ip хоста с wordpress:                    http_host:  172.31.47.188
  
group_vars/http-server
  sudo пользователь:                      ansible_user : ubuntu
  путь к ssh ключу:                       ansible_ssh_private_key_file : /home/ubuntu/.ssh/ansible.pem
  имя сайта:                              http_host: mysite
  конфиг сайта:                           http_conf: mysite.conf
  порт подключения:                       http_port: 80
  пароль от ползователя BD для wordpress: mysql_password: "password"
  ip хоста с BD:                          db_host: 172.31.35.27
  
Переменная mysql_password должна иметь одинаковое значение
