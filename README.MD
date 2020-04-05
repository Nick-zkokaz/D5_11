# Модуль D5
Начальный проект домашней библиотеки.
Для того, чтобы запустить локальный сервер необходимо, например, с помощью терминала PyCharm:
1) Открыть проект в папке C:\D5
2) Откройте командную строку и зайдите в директорию проекта:
   cd C:\D5
3) Создать виртуальное окружение через PyCharm Trminal - обязательно сделать эту команду - в директроии D5 должны появится папка django
   python -m venv django
4) Активировать виртуальное окружение через PyCharm Trminal:
   django\Scripts\activate.bat
5) Установить все необходимые пакеты через PyCharm Trminal:
   pip install -r requirements.txt

6) НООБЯЗАТЕЛЬНАЯ КОМАНДА при ззагрузке архива с GitHab
	Выполнить следующие команды через PyCharm Trminal:
   python manage.py makemigrations
   python manage.py migrate
		если не проходят, то с явным указанием приложения:
		python manage.py makemigrations p_library
		python manage.py migrate p_library
   python manage.py loaddata data.xml
			
 
7) для использования админки необходимо сформировать ВАШЕГО суперюзера:   
	python manage.py createsuperuser 
	Username (leave blank to use '12345'): 12345@mail.ru
    Email address: 12345@mail.ru
    Password:
    Password (again):
    Superuser created successfully.

	
7)Запуск сервера
	python manage.py runserver

После запуска сервера - прогон по адресам:
http://127.0.0.1:8000/admin/
http://127.0.0.1:8000/index/
http://127.0.0.1:8000/publisher_new/
http://127.0.0.1:8000/friend_list/
http://127.0.0.1:8000/author/create 
http://127.0.0.1:8000/ - попадает в список друзей 
http://127.0.0.1:8000/authors  
http://127.0.0.1:8000/author/create_many  
http://127.0.0.1:8000/author_book/create_many  
http://127.0.0.1:8000/friend/create  
http://127.0.0.1:8000/friends  
http://127.0.0.1:8000/book_friend/create  

