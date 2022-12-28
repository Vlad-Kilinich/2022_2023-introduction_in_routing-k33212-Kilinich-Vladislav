# Лабораторная работ №4 "Эмуляция распределенной корпоративной сети связи, настройка iBGP, организация L3VPN, VPLS"
---
University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Introduction in routing](https://github.com/itmo-ict-faculty/introduction-in-routing)  
Year: 2022/2023  
Group: K33212  
Author: Kilinich Vladislav Aleksandrovich  
Lab: Lab4  
Date of create: 16.12.2022  
Date of finished: 10.01.2023 
---  
# Ход работы  
---  
1) Развертывание контейнера:  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/Снимок.PNG?raw=true)  
# Часть 1 Найстройка всех устройств  
* На всех роутерах были настроены OSPF и MPLS, iBGP, в том числе с route reflector кластером для 3 роутеров HKI, LBN, LND  
* На роутерах SPB, NY, SVL были настроены VRF, RD и RT.  
2) Конфигурация настройки OSPF, MPLS, iBGP и VRF на RO1.NY  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/2.PNG?raw=true)  
3) Конфигурация настройки OSPF, MPLS, iBGP и VRF на RO1.LND  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/1.PNG?raw=true)  
4) Конфигурация настройки OSPF, MPLS, iBGP и VRF на RO1.LBN  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/3.PNG?raw=true)  
5) Конфигурация настройки OSPF, MPLS, iBGP и VRF на RO1.SVL  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/4.PNG?raw=true)  
6) Конфигурация настройки OSPF, MPLS, iBGP и VRF на RO1.HKI  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/5.PNG?raw=true)  
7) Конфигурация настройки OSPF, MPLS, iBGP и VRF на RO1.SPB  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/6.PNG?raw=true)  
---  
8) Проверка BGP и VRF:  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/20%20e.PNG?raw=true)   
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/21%20e.PNG?raw=true)   
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/22.PNG?raw=true)   
9) Пинги VRF_DEVOPS  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/7ПРоверка%20пингов%20vrf.PNG?raw=true)   
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/8Проверка%20пингов%20VRF.PNG?raw=true)   
---  
# Вторая часть  
---  
Был разобран VRF на SPB, NY, SVL. Далее на этих 3 роутерах был настроен VPLS. 
Для начала удалили интерфейсы для связи с компьютерами, а также обновили конфигурацию роутеров. Также на компьютерах была настроена IP-адресация в одной сети (172.10.10.*/24).  
1. Обновленная конфигурация RO1.NY  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/9%20настройка%20VPLS%20NY.PNG?raw=true)  
2. Обновленная конфигурация RO1.SVL   
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/10%20Найстрока%20VPLS%20SVL.PNG?raw=true)  
3. Обновленная конфигурация RO1.SPB    
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/11%20VPLS%20SPB.PNG?raw=true)      
4. PC1  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/13%20PC1.PNG?raw=true)  
5. PC2  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/15%20PC2%20а%20не%203.PNG?raw=true)  
6. PC3  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/14%20pc2.PNG?raw=true)  
---  
# Проверка VPLS  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/16%20проверка%20пингов%20pc.PNG?raw=true)  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/17%20пинги%20PC.PNG?raw=true)  
Пример ip neighbor print на RO1.NY  
![avatar](https://github.com/Vladkilinichh/2022_2023-introduction_in_routing-k33212-Kilinich-Vladislav/blob/main/lab4/pictures/18%20IP%20nei%20p%20NY.PNG?raw=true)  
---









