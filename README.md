# Домашнее задание к занятию "`9.2. Zabbix. Часть 1`" - `Вахрамеев А.В`
---

### Задание 1

Установите Zabbix Server с веб-интерфейсом.

Приложите скриншот авторизации в админке. Приложите текст использованных команд в GitHub.

---

```
root@zabbix:/home/admin# history 
    1  passwd root
    2  apt update
    3  apt install postgresql
    4  wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4%2Bdebian11_all.deb
    5  dpkg -i zabbix-release_6.0-4+debian11_all.deb
    6  apt update 
    7  sudo apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts nano -y #
    8  zabbix-agent
    9  ls
   10  dpkg -i zabbix-release_6.0-4+debian11_all.deb
   11  dpkg -i zabbix-release_6.0-4+debian11_all.deb
   12  sudo -u postgres createuser --pwprompt zabbix
   13  sudo -u postgres createdb -O zabbix zabbix
   14  zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix 
   15  sudo nano /etc/zabbix/zabbix_server.conf
   16  vim /etc/zabbix/zabbix_server.conf
   17  sudo systemctl restart zabbix-server apache2
   18  sudo systemctl enable zabbix-server apache2
   19  history 
```

`Zabbix`
![Снимок экрана от 2022-11-10 14-43-55](https://user-images.githubusercontent.com/75438030/201082154-8f28d323-46f4-49fd-ba41-e745d16d389e.png)

---

### Задание 2

`Приведите ответ в свободной форме........`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 2](ссылка на скриншот 2)`


---


## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.

### Задание 3

`Приведите ответ в свободной форме........`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`
