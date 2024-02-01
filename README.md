Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки»


Задание 1

    Запустите два simple python сервера на своей виртуальной машине на разных портах
    Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
    Настройте балансировку Round-robin на 4 уровне.
    На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.
![image](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/server1.png)
![image](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202024-02-01%2023-45-00.png)
![image](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202024-02-02%2000-49-49.png)


[script](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/haproxy.cfg)


Задание 2

    Запустите три simple python сервера на своей виртуальной машине на разных портах
    Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
    HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
    На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.
![image](https://github.com/sergeev-Aleksandr/Sergeev-8-03-hw./blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202024-02-02%2000-57-51.png)
