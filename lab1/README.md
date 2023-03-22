Получение сведений о системе
================
turiev02@mail.ru

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  Ноутбук ASUS TUF Gaming F15 FX507ZM_FX507ZM

2.  ОС Ubuntu

3.  Интерпретатор командной оболочки bash 5.2.15

4.  Эмулятор терминала Guake

## План

1.  Ввод команд в эмулятор терминала

2.  Анализ данных

## Ход работы

1.  Для начала получим сведения об используемом дистрибутиве:

``` bash
lsb_release -a
```

    LSB Version:    n/a
    Distributor ID: Ubuntu
    Description:    Ubuntu 22.04.1 LTS
    Release:        22.04
    Codename:       jammy

В результате выполнения данной команды было определён используемый
дистрибутив - Ubuntu 22.04.1 LTS.

1.  Затем получим сведения о версии ядра:

``` bash
uname -a
```

    Linux vm 5.15.0-47-generic #51-Ubuntu SMP Thu Aug 11 07:51:15 UTC 2022 x86_64 x86_64 x86_64 GNU/Linux

В результате выполнения данной команды была получена версия ядра -
5.15.0-47, дата компиляции ядра - 11 августа 2022 года.

1.  Далее можно получить сведения о процессоре:

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : Intel(R) Core(TM) i7-12700H CPU @ 2.3GHz
    model name  : Intel(R) Core(TM) i7-12700H CPU @ 2.3GHz
    model name  : Intel(R) Core(TM) i7-12700H CPU @ 2.3GHz
    model name  : Intel(R) Core(TM) i7-12700H CPU @ 2.3GHz

Было определено, что используемый процессор - двадцатипоточный Intel Core
i7-12700H с тактовой частотой 2.3 ГГц.

1.  Далее получим последние 30 строк логов системы:

``` bash
dmesg | tail -n 30
```

    [ 3954.221445] wlp3s0: 80 MHz not supported, disabling VHT
    [ 3954.234219] wlp3s0: send auth to 36:a0:57:b5:e4:1a (try 1/3)
    [ 3954.238727] wlp3s0: authenticated
    [ 3954.241726] wlp3s0: associate with 36:a0:57:b5:e4:1a (try 1/3)
    [ 3954.249307] wlp3s0: RX AssocResp from 36:a0:57:b5:e4:1a (capab=0x431 status=0 aid=1)
    [ 3954.249485] wlp3s0: associated
    [ 3954.249725] ath: EEPROM regdomain: 0x8283
    [ 3954.249730] ath: EEPROM indicates we should expect a country code
    [ 3954.249733] ath: doing EEPROM country->regdmn map search
    [ 3954.249735] ath: country maps to regdmn code: 0x3d
    [ 3954.249737] ath: Country alpha2 being used: RU
    [ 3954.249739] ath: Regpair used: 0x3d
    [ 3954.249741] ath: regdomain 0x8283 dynamically updated by country element
    [ 3954.373849] wlp3s0: Limiting TX power to 0 (-128 - 0) dBm as advertised by 36:a0:57:b5:e4:1a
    [ 3954.397950] IPv6: ADDRCONF(NETDEV_CHANGE): wlp3s0: link becomes ready
    [ 5239.144114] wlp3s0: authenticate with 36:a0:57:b5:e4:1a
    [ 5239.144158] wlp3s0: 80 MHz not supported, disabling VHT
    [ 5239.157039] wlp3s0: send auth to 36:a0:57:b5:e4:1a (try 1/3)
    [ 5239.160732] wlp3s0: authenticated
    [ 5239.169136] wlp3s0: associate with 36:a0:57:b5:e4:1a (try 1/3)
    [ 5239.187045] wlp3s0: RX AssocResp from 36:a0:57:b5:e4:1a (capab=0x431 status=0 aid=1)
    [ 5239.187269] wlp3s0: associated
    [ 5239.187583] ath: EEPROM regdomain: 0x8283
    [ 5239.187591] ath: EEPROM indicates we should expect a country code
    [ 5239.187595] ath: doing EEPROM country->regdmn map search
    [ 5239.187599] ath: country maps to regdmn code: 0x3d
    [ 5239.187603] ath: Country alpha2 being used: RU
    [ 5239.187607] ath: Regpair used: 0x3d
    [ 5239.187611] ath: regdomain 0x8283 dynamically updated by country element
    [ 5239.252916] wlp3s0: Limiting TX power to 0 (-128 - 0) dBm as advertised by 36:a0:57:b5:e4:1a

## Оценка результата

В результате лабораторной работы была получена базовая информация об
используемой системе.

## Вывод

Таким образом. мы научились, используя команды Linux, получать сведения
о системе.
