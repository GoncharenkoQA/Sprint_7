# Sprint_7
### Введение в проект
«Яндекс Самокат» — это сервис для аренды самокатов в Москве и Московской области. Приложение создано специально для отработки навыков студентов «Практикума».
Для отправки запросов автотесты используют библиотеку Requests. Отчет о тестировании генерируется с помощью фреймворка Allure и библиотеки allure-pytest.

### Покрытие
Задание проекта не требует полного покрытия. В рамках тестирования нужно проверить лишь некоторый функционал

## TestCourierCreateAPI: ##
Тесты ручки создания курьера:
- test_courier_create_new_courier_success — успешное создание курьера
- test_courier_create_already_existing_user_fail — создание курьера с существующими данными
- test_courier_create_no_data_fail — создание курьера с неполным набором данных

## TestCourierLoginAPI: ##
Тесты ручки логина курьера:
- test_courier_login_success — успешный логин курьера
- test_courier_login_no_such_user_fail — логин с несуществующими данными
- test_courier_login_no_data_fail — логин с недостаточными данными (падает на отправке только логина)

## TestCourierDeleteAPI: ##
- test_courier_delete_success — успешное удаление курьера
- test_courier_delete_no_id_fail — удаление при несуществующем id
- test_courier_delete_without_id_fail - удаление при отправке без id в теле (падает, так как без id в теле запроса курьер все равно удаляется)

## TestGetOrdersList: ##
- test_get_orders_list_success - успешное получение списка заказов

## TestCreateOrder: ##
- test_order_creation_with_different_colors_success - успешное создание заказа с разными цветами

## TestTrackOrder: ##
- test_order_track_success - успешное получение заказа
- test_order_track_no_order_id_fail - получение заказа без номера
- test_order_track_wrong_order_id_fail - получение заказа с некорректным номером

## TestAcceptOrder: ##
- test_order_accept_success - успешный акцепт заказа
- test_order_accept_no_сourier_id_fail - акцепт без id клиента
- test_order_accept_no_order_id_fail - акцепт без номера заказа (падает)
- test_order_accept_wrong_courier_id_fail - акцепт с некорректным курьером

### Запуск всех тестов

Установка всех зависимостей: `pip install -r requirements.txt`.

Запуск всех тестов: `pytest -v`.


### Отчет о тестировании

Allure-отчет в формате веб-страницы генерируется командой `allure serve allure_results`.