<!----- Conversion time: 0.718 seconds.
Using this Markdown file:

1. Cut and paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β17
* Wed Sep 18 2019 01:52:00 GMT-0700 (PDT)
* Source doc: https://docs.google.com/open?id=1SEODmwLcgVdQijJMZ6Xc3YQ0lqnkc72w-gccG4AkpqU
----->

## Создание простого многопоточного сервера

### Цель работы

Познакомиться с приемами работы с многопоточностью на примере создания сокетного TCP-сервера, способного работать с несколькими клиентами одновременно



### Дополнительные задания

2. Модифицировать простой эхо-сервер таким образом, чтобы при подключении клиента создавался новый поток, в котором происходило взаимодействие с ним.

![image](https://user-images.githubusercontent.com/90088335/142394418-746919fb-72fc-4dab-a28f-6fb557586d4e.png)

3. Реализовать простой чат сервер на базе сервера аутентификации. Сервер должен обеспечивать подключение многих пользователей одновременно, отслеживание имен пользователей, поддерживать историю сообщений и пересылку сообщений от каждого пользователя всем остальным. 

![image](https://user-images.githubusercontent.com/90088335/142394771-9f05c03d-fcbe-4e84-aa52-560f4667c277.png)

![image](https://user-images.githubusercontent.com/90088335/142394833-f76f083c-e249-4290-acc1-3fc321e66793.png)

![image](https://user-images.githubusercontent.com/90088335/142394872-a0f1db57-06be-4f57-aec0-15415b5bdb31.png)

4. Реализовать сервер с управляющим потоком. При создании сервера прослушивание портов происходит в отдельном потоке, а главный поток программы в это время способен принимать команды от пользователя. Необходимо реализовать следующие команды:

![image](https://user-images.githubusercontent.com/90088335/142395242-f047e194-1f32-4758-a8b9-abba8b3e0904.png)

![image](https://user-images.githubusercontent.com/90088335/142395287-c6790955-2b9e-49fe-8501-4de301951e06.png)

    1. Отключение сервера (завершение программы);
    
    ![image](https://user-images.githubusercontent.com/90088335/142395419-2cc84ed5-4cd9-4cb9-b04e-44606452c970.png)

    2. Пауза (остановка прослушивание порта);

    ![image](https://user-images.githubusercontent.com/90088335/142395601-180fc6d4-e3c6-48cd-8cb7-e3c6e8ea9b0b.png)

    ![image](https://user-images.githubusercontent.com/90088335/142395709-6ad7edf4-957c-4737-9c21-e81c7f426719.png)

    3. Показ логов;

    ![image](https://user-images.githubusercontent.com/90088335/142395804-7e22c6f0-cf3d-4130-8554-b40c04133e65.png)

    4. Очистка логов;

    ![image](https://user-images.githubusercontent.com/90088335/142395895-d17edfed-38d5-4226-a241-528e045c5598.png)

    5. Очистка файла идентификации.
      
    ![image](https://user-images.githubusercontent.com/90088335/142396040-b345b975-7fd3-4302-bf8b-fcf91414b239.png)
    
    ![image](https://user-images.githubusercontent.com/90088335/142396130-84faf35a-8b9e-4076-8d75-3cacb158fb5c.png)


<!-- Docs to Markdown version 1.0β17 -->
