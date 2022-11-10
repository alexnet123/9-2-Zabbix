# Домашнее задание к занятию "`9.2. Zabbix. Часть 1`" - `Вахрамеев А.В`
---

### Задание 1

Установите Zabbix Server с веб-интерфейсом.

Приложите скриншот авторизации в админке. Приложите текст использованных команд в GitHub.

---

```
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
```

`Zabbix`
![Снимок экрана от 2022-11-10 14-43-55](https://user-images.githubusercontent.com/75438030/201082154-8f28d323-46f4-49fd-ba41-e745d16d389e.png)

---

### Задание 2

Установите Zabbix Agent на два хоста.

Приложите скриншот раздела Configuration > Hosts, где видно, что агенты подключены к серверу. Приложите скриншот лога zabbix agent, где видно, что он работает с сервером. Приложите скриншот раздела Monitoring > Latest data для обоих хостов, где видны поступающие от агентов данные. Приложите текст использованных команд в GitHub.

---

```
1  wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4%2Bdebian11_all.deb
2  dpkg -i zabbix-release_6.0-4+debian11_all.deb
3  apt update
4  sudo apt install zabbix-agent -y
5  sudo systemctl restart zabbix-agent
6  sudo systemctl enable zabbix-agent
7  vim /etc/zabbix/zabbix_agentd.conf 
8  sudo systemctl restart zabbix-agent

```

`Агенты`
![Снимок экрана от 2022-11-10 15-12-35](https://user-images.githubusercontent.com/75438030/201088773-6a938c2c-545f-45eb-b73d-a82913fbda33.png)
`Агент log`
![Снимок экрана от 2022-11-10 15-18-54](https://user-images.githubusercontent.com/75438030/201089861-8ee20e0f-41d2-4234-8d73-e777edac5983.png)
`Latest data`
![Снимок экрана от 2022-11-10 15-20-37](https://user-images.githubusercontent.com/75438030/201090188-82420f82-ea02-4dc7-bf2e-2c62ae98e598.png)


---
