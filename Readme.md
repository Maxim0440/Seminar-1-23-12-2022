# Инструкция по работе с Git

## Что такое Git

##  Подготовка репозитория

## Создание "сохранений"

## Перемещение между "сохранениями"

Для перемещения на другую фиксацию(коммит) используется команда*git checkout*. Для этого необходимо, как показано в прошлом пункте, в журнале изменений найти необходимый коммит и егохеш(номер), после чего в терминале с папкой репозиториемнадо написать *git checkout <хеш коммита>*.
После выполнения этой команды мы попадаем в состояние **detached head**, в котором следующие коммиты сохраняться не будут. Для выхода из этого состояния необходимо писать 
*checkout master*.

## Журнал изменений

## Ветки в гит

## Слияние веток и разрешение конфликтов

## Удаление веток