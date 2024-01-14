# lesson16

Настраиваем центральный сервер для сбора логов

**Домашнее задание**

1. в вагранте поднимаем 2 машины web и log
2. на web поднимаем nginx
3. на log настраиваем центральный лог сервер на любой системе на выбор
-journald;
-rsyslog;
-elk.
4. настраиваем аудит, следящий за изменением конфигов нжинкса

ДЗ выполнял согласно методичке </br>
Поднял две машины  по vagrantfile </br>
На web установил epel-release  и  nginx</br>
Синхронизировал по времени каждую машину </br>
![image](https://github.com/movik242/lesson16/assets/143793993/5447fdb1-a45f-4376-ac68-33272da94c1c) </br>
![image](https://github.com/movik242/lesson16/assets/143793993/d3ae00e1-66ac-4c88-b4f3-3cc142659970) </br>

Настраиваю rsyslog на log

![image](https://github.com/movik242/lesson16/assets/143793993/0f90544f-53ed-4437-a85d-f93a828cb4e4) </br>

Настроил пересылку логов

![image](https://github.com/movik242/lesson16/assets/143793993/b8122858-4d8e-4465-97ce-0c39932e0786) </br>

![image](https://github.com/movik242/lesson16/assets/143793993/d337c907-b786-4486-915b-d0f0cd976ef2)


Проверяем приходят ли логи на log

![image](https://github.com/movik242/lesson16/assets/143793993/0063f90f-b00d-4d1f-90eb-a4b4f19ed3f9)  </br>
![image](https://github.com/movik242/lesson16/assets/143793993/d5f047b3-ee01-4d15-a6bd-2bf8c6d5a1c3) </br>

Логи по метке nginx_conf

![image](https://github.com/movik242/lesson16/assets/143793993/c71799c7-4867-4a57-800b-7c6a182b3d78) </br>

Настройка audit, установка </br>
      yum -y install audispd-plugins

![image](https://github.com/movik242/lesson16/assets/143793993/376046b0-fc84-40ef-b1f9-bbeabf3b04a1)

При изменении прав на nginx.conf, логи приходят на машину log

![image](https://github.com/movik242/lesson16/assets/143793993/5bf658aa-0deb-4780-b882-a6e8c3b1ad71)





