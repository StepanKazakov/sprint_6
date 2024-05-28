# sprint_6
# Проект автоматизации тестирования сервиса "Яндекс.Самокат"

Этот проект содержит набор автоматизированных тестов для проверки функциональности сервиса [Яндекс.Самокат](https://qa-scooter.praktikum-services.ru/). 
Тесты написаны с использованием фреймворка Selenium и организованы по принципам Page Object Model.

## Структура проекта

Проект состоит из следующих модулей:

- `conftest.py`: файл конфигурации, содержащий фикстуру для запуска и завершения работы веб-драйвера.
- `locators`: директория, содержащая модули с локаторами для различных функций.
  - `scooter_order_locators.py`: локаторы для заказа самоката.
  - `faq_list_locators.py`: локаторы для часто задаваемых вопросов (FAQ).
  - `base_locators.py`: локаторы элементов, которые доступны на всех страницах (логотипы и предупреждение о куках).
- `page_objects`: директория, содержащая классы page object для различного функционала.
  - `scooter_order.py`:page object для функционала заказа самоката.
  - `faq_list.py`: page object для работы с FAQ.
  - `accept_cookie.py`: page object для работы с сообщением о приеме куки.
  - `logo_links.py`: page object для работы с логотипами в хедере страницы.
- `tests`: директория, содержащая тестовые классы.
  - `test_scooter_order.py`: модуль с тестами для проверки сценариев заказа самоката.
  - `test_faq_list.py`: модуль с тестами для проверки FAQ раздела.
- `allure_results`: директория для хранения результатов тестирования в allure.
- `order_dataset.py`: модуль для генерации данных для заказа.
- `requirements.txt`: файл с внешними зависимостями.

## Установка и запуск

### Требования

- Python 3.7 или выше
- Selenium
- pytest
- allure
- браузер Firefox и драйвер geckodriver

### Установка зависимостей

```
pip3 install -r requirements.txt
```

### Запуск тестов

```
pytest --alluredir=./allure_results
```

### Просмотр результатов тестирования

```
allure serve allure_results
```
