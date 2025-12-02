# Шпаргалка для тупеньких по GITу

0. Базовые команды командной строки:


- *pwd* (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке;
- *ls* (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;
- *ls* -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;
- *cd* directory/path (от англ. change directory, «сменить директорию») — перейди в папку directory/path (cd .. — перейди на уровень выше, в родительскую папку, cd ~ — перейди в домашнюю директорию);
- *touch* index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке (если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел);
- *mkdir* second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке.
- *cp* file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место;
- *mv* file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место;
- *cat* file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt;
- *nano* file.txt - редактровать файл file.txt при помощи утилиты nano;
- *rm* about.html (от англ. remove, «удалить») — удали файл about.html;
- *rmdir* images (от англ. remove directory, «удалить директорию») — удали папку images;
- *rm* -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.



1. команды GIT:


- git init - создание репозитория. вызывать из корня репы
- git status - запрос сотояния файлов репозитория. вызывать из корня репы


2. Статусная модель файла в git:


```mermaid
%% описание схемы
graph LR;
  untracked -- "git add" --> staged+tracked -- "git commit" --> tracked;
  modified -- "git add" --> staged+tracked;
  tracked -- "изменение" --> modified;
  staged+tracked -- "изменение" --> modified;

```

