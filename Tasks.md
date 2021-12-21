# Создать Dockerfiles для приложений и docker-compose проекта

__* Сбор метрик, логов, данных и передача на базе ОС balena.io и Raspberry PI 4 + LTE modem"__

1. запаковать в docker:debian 10 приложение по пути (\tm_server\tm_cpps_RPi4b64_13633.deb)

2. IPSec Client для связи tm_cpps_RPi4b64_13633 с сервером по параметрам:

```con
Тип VPN site to site IPsec/IKEv2
    IKEv2 policy
    Encription    AES-256
    Integrity    SHA-512
    DH group    14
    Lifetime, с    86400
    Peer    xxx.xxx.xxx.xxx
IPsec polisy
    Encription    AES-256
    Integrity    SHA-512
    Peer    xxx.xxx.xxx.xxx
```

3. Сбор метрик и логов с хоста и по SNMP роутеры iRZ 2x, iRZ 4x и Teltonika 955 (https://github.com/influxdata/telegraf/blob/release-1.20/plugins/inputs/snmp/README.md)

4. Опрос оборудования Modbus с помощью агента Telegraf https://github.com/influxdata/telegraf/blob/master/plugins/inputs/modbus/README.md
