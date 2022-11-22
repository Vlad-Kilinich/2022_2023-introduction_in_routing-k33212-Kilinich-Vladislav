# Отчёт по лабораторной работе №1 "Установка ContainerLab и развертывание тестовой сети связи"
Цель: ознакомиться с инструментом ContainerLab и методами работы с ним, изучить работу VLAN, IP адресации и т.д.
***
University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Introduction in routing](https://github.com/itmo-ict-faculty/introduction-in-routing)
Year: 2022/2023
Group: K33212
Author: Kilinich Vladislav
Lab: Lab1
Date of create: 18.11.2022
Date of finished: 3.12.2022

***
Ход работы
-
1. Устройства в сети:
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/Снимок.PNG?raw=true)
2. Конфигурации устройств: Роутер R01
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/2.PNG?raw=true)
Коммутатор первого уровня SW01.L3.01
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/3.PNG?raw=true)
Коммутатор второго уровня SW02.L3.01
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/4.PNG?raw=true)
Коммутатор второго уровня SW02.L3.02
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/5.PNG?raw=true)
***
Найстройка DHCP
-
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/7.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/8.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/9.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/10.PNG?raw=true)
***
Проверка пингов
-
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/11.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/12.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/13.PNG?raw=true)
***
Добавление пользователя
-
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/14.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/15.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/16.PNG?raw=true)
![avatar](https://github.com/Vladkilinichh/routing/blob/main/lab1/pictures/17.PNG?raw=true)
***
Вывод
-
В ходе лабораторной работы  я познакомился с инструментом Сontainerlab. С помощью файла конфигурации сети .yaml была развернута сеть из роутера, 3-х коммутаторов и 2х ПК. В сети настроены 2 vlan и 2 dhcp-сервера для автоматической раздачи ip адресов. 
