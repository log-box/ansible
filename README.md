# ansible
Здание
======================================================
1. Развернуть виртуальную машину на centos 8

hostname: c8.local

2. Развернуть виртуальную машину на ubuntu 21.04

hostname: u21.local

3. Написать ansible playbook для c8.local и u21.local

c8.local должен быть в группе frontend

u21.local должен быть в группе backend

    - для ОС centos playbook должен применять следующие изменения

    * selinux: disable

    * firewalld: disable

    - для группы frontend playbook должен установить и сконфигурировать nginx

    - конфигурация nginx должна делать проксирование с порта 80 на порт 19999 в группу backend

    - для группы backend playbook должен установить из официальных репозиториев приложение netdata и запустить его на порту 19999

4. Оформить на git репозиторий ansible и выложить туда плейбук
=======================================================

ansible.cfg - host /etc/ansible/ansible.cfg
hosts - /etc/ansible/hosts
mylog.txt - output 
netdata.conf (u21) /etc/netdata/netdata.conf
nginx.conf (c8) /etc/nginx/nginx.conf

root без пароля по ключу

адрес для с8 - http://127.0.0.1/netdata/server1 проксируется на u21 172.21.0.101:19999