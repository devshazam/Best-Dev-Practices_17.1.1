	$ rm -rf app // удалени файлов и папок рекурсивно 
	$ mv book_list.txt movie_list.txt // в текущей папке
		$ cp  // Копировать файл или каталог
	$ > file.md // очистить содержимое файла

	$ nano test.txt // возможно редактирование кода вставка 
	$ cat test.txt // Отображение содержимого файла
	$ tail -15 mylogfile.txt // вывод 15 последних строк
	$ grep <search-word> /var/log/auth.log // поиск по файлу

	$ history | grep <search-word>
		!<command-number> // вбить номер команды для повторения

	$ ping domail.com // проверка привязанного IP адреса домена

Options:
	> - перенаправление результатов команды в файл
	| // перенаправление результатов команды в следующую команду
	; // использование последовательно в не зависимости от успешности исполнения предведущей команды
	&& // последовательное исполнение команд только при условии успешного исполнения предведущей команды
	|| // если одно выполнилост, то остальные не выполняются

