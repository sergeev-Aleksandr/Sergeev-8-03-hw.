
Домашнее задание к занятию "Disaster recovery и Keepalived" - Сергеев Александр
Задание 1

    Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.
    На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
    Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
    Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
    На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

Скриншот вывода команд sho standby, на которых видно что для интерфейсов g0/0 g0/1 настроен hsrp preempt, позволяет сделать роутер активным сразу как приоритет становится большим по отношению к партнеру.
А так же настроен standby track, который позволяет отслеживать состояние того или иного интерфейса и изменять приоритет интерфейса
![Image ait](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/Z1.PNG)
Файл packet tracer
 [pkt file](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/hsrp_advanced_Z1.pkt)


Задание 2

    Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в 
    лекции, используя пример конфигурационного файла.
    Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
    Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование 
    файла index.html в root-директории данного веб-сервера.
    Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный I
    P на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера 
    был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
    На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот 
    с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

    Tracking script
keepalived запускает скрипт с определенным интервалом, если скрипт возвращает статус 0, то ничего не происходит, 
если 1, то keepalived переходит в статус fault.
Получившийся bash-скрипт
[script](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/script)

Конфигурационный файл keepalived с настройкой tracking script
[creat script](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/creat%20script)


Результаты переезда плавающего ip
![Image ait](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202024-01-30%2002-10-23.png)