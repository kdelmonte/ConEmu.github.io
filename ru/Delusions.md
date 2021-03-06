---
title: ConEmu | Околоконсольные заблужения

description: "Частые заблуждения пользователей
   относительно консольных приложений"

breadcrumbs:
 - url: TableOfContents.html#conemu
   title: ConEmu

readalso:
 - url: TableOfContents.html#terms
   title: Термины ConEmu
 - url: ConEmuFAQ.html
   title: Частые вопросы
 - url: TerminalVsShell.html
   title: Terminal или Shell

otherlang:
   eng: /en/Delusions.html
   rus: /ru/Delusions.html
---

# Околоконсольные заблужения

## Называть PuTTY, mintty и др. консольными приложениями.

Упрощая, консольное приложение это специальным образом созданное
приложение которое взаимодействует с "пользователем" только
посредством ввода-вывода данных (например текста). По умолчанию КП
не умеет ничего "отрисовывать", у него вообще нет графического
интерфейса. Оно работает ТОЛЬКО с потоками ввода-вывода
(перенаправление, пайпы, волшебные символы `<`, `>`, `|`).

    cmd /? > cmd.log & type cmd.log | find "HKEY"

При запуске такого приложения в Windows создается специальное
консольное окно и именно оно занимается отрисовкой текста,
выводимого КП, и перенаправлением нажимаемых пользователем клавиш в
буфер ввода КП. Это консольное окно также называется терминалом.

PuTTY, KiTTY, mintty и другие терминалы НЕ являются консольными
приложениями. Это графические приложения (имеющие свой графические
интерфейс) умеющие либо подключаться к удаленным серверам для
запуска консольных приложений удаленно, либо работают как локальные
терминалы, предоставляя возможности ввода-вывода консольным
приложениям на локальном компьютере.

Вы не можете перенаправить "вывод" терминала в файл, т.к терминал
работает с дисплеем и клавиатурой, а не с потоками ввода-вывода.
Исключение - логирование, настраиваемое специально в самом
терминале.


## Называть стандартную консоль Windows - cmd.exe.

В Windows есть встроенный терминал (или "консольное окно") которое
часто ошибочно называют "cmd.exe". Нажмите Win+R и запустите,
например, "powershell.exe". Среди запущенных процессов не будет
"cmd.exe". В разных версиях Windows консольное окно создают разные
процессы, в актуальных – это "conhost.exe".

Не ‘cmd.exe’, а просто ‘консоль’!
