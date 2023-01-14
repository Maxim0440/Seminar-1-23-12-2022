# Инструкция по работе с Git

## Что такое Git

***Git***  - Это самая популярная организация распределеннной системы контроля версиий (версионность поддерживается и на сервере и у каждого клиента). Самый распространенной реализацией ***Git*** является (GitHub)[http://github.com].

##  Подготовка репозитория

Для созданиния репозитория используется команда *git init*. Для этого нужно открыть в терминале папку с будущим репозиторием и написать *git init*.


### Создание коммита

Для создания новой фиксации (коммита)
используется команда *git commit*. для этого в терминале с папкой-репозиторием пишем *git commit -m"<сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.


### Добавление файлов к коммиту

Для добавления файла к новому коммиту используется команда "git add". используется она в терминале с папкой -репозиторием пишем *git add <название файла>*.


## Перемещение между между коммитами

Для перемещения на другую фиксацию(коммит) используется команда*git checkout*. Для этого необходимо, как показано в прошлом пункте, в журнале изменений найти необходимый коммит и егохеш(номер), после чего в терминале с папкой репозиториемнадо написать *git checkout <хеш коммита>*.
После выполнения этой команды мы попадаем в состояние **detached head**, в котором следующие коммиты сохраняться не будут. Для выхода из этого состояния необходимо писать 
*checkout master*.

## Журнал изменений

Для просмотра истории изменений используется команда*git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.


## Ветки в гит
Во время разработки новой функциональности считается хорошей практикой работать с копией оригинального проекта, которую называют веткой. Ветви имеют свою собственную историю и изолированные друг от друга изменения до тех пор, пока вы не решаете слить изменения вместе.  Основная ветка в каждом репозитории называется master. Чтобы создать еще одну ветку, используем команду branch <name>
 
 ### Для создания новой ветки используется команда "git branch". Для этого в терминале с папкой-репозиторием необходимо написать "git branch" <название ветки>. 

## Слияние веток 
Для слияния веток используется команда git merge <branch name>. этот момент нужно находиться в ветке, в которую нужно внести изменения



## Разрешение конфликтов

Обычно конфликты возникают, когда два человека изменяют одни и те же строки в файле или один разработчик удаляет файл, который в это время изменяет другой разработчик. В таких случаях Git не может автоматически определить, какое изменение является правильным. Конфликты затрагивают только того разработчика, который выполняет слияние, остальная часть команды о конфликте не знает. Git помечает файл как конфликтующий и останавливает процесс слияния. В этом случае ответственность за разрешение конфликта несут разработчики. 

## Удаление веток

 Бывают ситуации, когда после слива каких-то изменений из рабочей ветки в исходную версию проекта, ее, по правилам хорошего тона, необходимо удалить, чтобы она более не мешалась в вашем коде. Для локально расположенных веток существует команда:
git branch -d local_branch_name
где флажок -d являющийся опцией команды git branch - это сокращенная версия ключевого слова --delete, предназначенного для удаления ветки, а local_branch_name – название ненужной нам ветки.
