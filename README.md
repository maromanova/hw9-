# hw9-
Сделано в Notepad++
1. Вот, как это выглядило изначально
https://github.com/maromanova/hw9-/blob/master/0.PNG
Затем используем регулярные выражения \n\r и \0, чтобы найти и удалить все пустые строки 
https://github.com/maromanova/hw9-/blob/master/1.PNG
2. Найти всех князей и города, имя и название которых оканчивается на "слав". В выдаче должны быть такие слова как "Ярославля, Ростиславъ, Ростиславу, Переяславлъ" и т.п. Но не должно быть "славу, выславше" и т.п.
Для этого используем несколько регулярных выражений и вставляем в поиск ([А-Я])([а-я]){1,10}(слав)([а-я]){1,10}

([А-Я]) - первыя заглавная буква

([а-я]){1,10} - какое-то кол-во текста после первой буквы и перед "слав". 10 было выбрано рандомно

(слав) - основная часть, которая должна повторяться в каждом городе или имени

([а-я]){1,10} - см.выше

Упоминаний 559
https://github.com/maromanova/hw9-/blob/master/2.PNG
3.Найти все упоминания Новгорода. Учтите, что написание может быть разным . В выдаче должны быть такие слова как "Новѣгородѣ, Новъгородъ, Новгородцю, Новагорода, Новугороду"

Получилось (Нов)([а-я]){1,10}(город)([а-я]){1,10}

(Нов) и (город) - те части, что точно должны присутствовать во всех вариациях названия Новгорода. Между этими частями и после второй части еще могут быть буквы, так что вставляем ([а-я]){1,10}

Упоминаний Новгорода 30 
