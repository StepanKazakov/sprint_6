# sprint_6
# Проект автоматизации тестирования сервиса "Яндекс.Самокат"

Этот проект содержит набор автоматизированных тестов для проверки функциональности сервиса [Яндекс.Самокат](https://qa-scooter.praktikum-services.ru/). 
Тесты написаны с использованием фреймворка Selenium и организованы по принципам Page Object Model.

## Структура проекта

Проект состоит из следующих модулей:

- `conftest.py`: файл конфигурации, содержащий фикстуру для запуска и завершения работы веб-драйвера.
- `locators`: директория, содержащая модули с локаторами для различных функций.
  - `scooter_order_locators.py`: локаторы для заказа самоката.
  - `home_page_locators.py`: локаторы для ссылок, предупреждения о куках, часто задаваемых вопросов (FAQ).
- `page_objects`: директория, содержащая классы page object для различного функционала.
  - `order_page.py`:page object для страницы заказа самоката.
  - `home_page.py`: page object для работы с элементами стартовой страницы.
  - `base_page.py`: page object со стандартными методами.
- `tests`: директория, содержащая тестовые классы.
  - `test_scooter_order.py`: модуль с тестами для проверки сценариев заказа самоката.
  - `test_faq_list.py`: модуль с тестами для проверки FAQ раздела.
  - `test_redirections`: модуль с тестами перехода по ссылкам в хедере.
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
