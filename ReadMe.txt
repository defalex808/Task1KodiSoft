В попоследнем обновлении добавлена инициализация бд по принципу code- first. 

При первом запуске попросит email и password. (Тестовые данные: 
email: test@test.com 
password: Root123_ 


Или

Email: admin@gadmin@gmail.com
Password:_Aa123456
)
(Нижний пробел обязательно :) )
Также там можно зарегистрировать новую учетную запись. Но чтобы не регистрировались все подряд, я создал в регистрации поле Manager Code, чтобы только менеджер знающий данный код смог зарегистрировать своих сотрудников или колег. 
Кстати по умолчанию это строчка: code
(Зашифрован в коде с помощью MD5)

Реализовано адаптивный дизайн для мобильных и пк версий. 
Использовано генерация динамического представления с использованием объектов в качестве модели.
На первом слайде сразу же  с помощью Ajax подгружается график при выборе определенного варианта.
Что касается модели, для того чтобы статистика не искажалась с течением времени, при изменении цены на блюдо, например, добавил стоимость блюда в связующей таблице блюдо-заказ (OrderItemOrders, не лучшее название :D), а также в каждом заказе есть поле TotalPrice для закрепления цены на данный заказ по все той же причине.

При соединении с приложением обновляется в бд поле TotalPrice у заказов, которые закрыты, у текущих по умолчанию 0.

Также добавил способ оплаты по карте или наличными для слайда Payments dashboard.
На этом основные моменты закончились)
