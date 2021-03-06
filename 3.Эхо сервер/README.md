## Практикум по программированию.   Лабораторная работа "Эхо-сервер" 
### **Цель работы**
Познакомиться с приемами работы с сетевыми сокетами в языке программирования Python.
### **Задания для самостоятельного выполнения**
1.Модифицируйте код сервера таким образом, чтобы при разрыве соединения клиентом он продолжал слушать данный порт и, таким образом, был доступен для повторного подключения. По логам можно заметить, что клиент отключался, а потом вновь подключался к серверу:

![image](https://user-images.githubusercontent.com/90088335/142391045-7d55a887-907a-45c7-bf74-b4d7f4d7a531.png)

По логам видно, что пользователь подключился несколько раз.

2.Модифицируйте код клиента и сервера таким образом, чтобы номер порта и имя хоста (для клиента) они спрашивали у пользователя. Реализовать безопасный ввод данных и значения по умолчанию.

Если правильные значения или по умолчанию:

![image](https://user-images.githubusercontent.com/90088335/142391181-65d99e19-c59e-4ada-84bd-009311a0833a.png)

Неправильные значения:

![image](https://user-images.githubusercontent.com/90088335/142391263-2af98b87-49aa-4fe2-8c6d-aa0aecb83c22.png)

3.Модифицировать код сервера таким образом, чтобы все служебные сообщения выводились не в консоль, а в специальный лог-файл.

![image](https://user-images.githubusercontent.com/90088335/142391601-b43774b6-0c22-4688-ac80-7575aed1e994.png)

4.Модифицируйте код сервера таким образом, чтобы он автоматически изменял номер порта, если он уже занят. Сервер должен выводить в консоль номер порта, который он слушает.


5.Реализовать сервер идентификации. Сервер должен принимать соединения от клиента и проверять, известен ли ему уже этот клиент (по IP-адресу). Если известен, то поприветствовать его по имени. Если неизвестен, то запросить у пользователя имя и записать его в файл. Файл хранить в произвольном формате.

![image](https://user-images.githubusercontent.com/90088335/142392360-67a4b202-4208-4b1c-a317-7b13d999bf36.png)

Так как новый пользователь, нас сервер спрашивает имя и пароль. 

При повторном подключении:

![image](https://user-images.githubusercontent.com/90088335/142392522-3c446b44-5afe-4455-8221-dad973c8cccb.png)

6.Реализовать сервер аутентификации. Похоже на предыдущее задание, но вместе с именем пользователя сервер отслеживает и проверяет пароли. Дополнительные баллы за безопасное хранение паролей. Дополнительные баллы за поддержание сессии на основе токена наподобие cookies

![image](https://user-images.githubusercontent.com/90088335/142392675-13c127c0-d4a9-4612-8a40-1febba4f0cdb.png)

Сервер не спрашивает пароль и логин так как у профиля сохранён токен.

![image](https://user-images.githubusercontent.com/90088335/142392732-f6d41279-5d9e-43ba-9754-c052d28c2098.png)

К каждому паролю создается уникальный ключ

![image](https://user-images.githubusercontent.com/90088335/142392852-ba481257-cf6c-4b9e-b158-379d20780203.png)

Если удалить токен, то автоматически вход не выполнится и программа запросит пароль(если ввести неправильный пароль, то сервер выдаст, что пароль неправильный)

![image](https://user-images.githubusercontent.com/90088335/142393067-63a72a51-40d5-41a2-bb51-a39a900cce07.png)

**Если ввести верный пароль** 

![image](https://user-images.githubusercontent.com/90088335/142393155-e4d47d28-7a6a-45e7-a885-577ee16b413c.png)

7.Напишите вспомогательные функции, которые реализуют отправку и принятие текстовых сообщений в сокет. Функция отправки должна дополнять сообщение заголовком фиксированной длины, в котором содержится информация о длине сообщения. Функция принятия должна читать сообщение с учетом заголовка. В дополнении реализуйте преобразование строки в байтовый массив и обратно в этих же функциях. Дополнително оценивается, если эти функции будут реализованы как унаследованное расширение класса socket библиотеки socket.

![image](https://user-images.githubusercontent.com/90088335/142393318-e14a2e38-afe5-4bcf-b135-7129cb9c84c5.png)

![image](https://user-images.githubusercontent.com/90088335/142393403-1aafd185-2018-41db-821c-c8e3de4ced84.png)

8.Дополните код клиента и сервера таким образом, чтобы они могли посылать друг другу множественные сообщения один в ответ на другое.

![image](https://user-images.githubusercontent.com/90088335/142393670-ee949e83-1aec-4ba8-895d-511f5209c200.png)

Клиент отправляет одно сообщение сервер в ответ 5 
