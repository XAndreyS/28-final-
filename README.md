Introduction
------------

This repository contains basic example of usage PageObject
pattern with Selenium and Python (PyTest + Selenium).

Video screencast with the description ot this code:
https://www.youtube.com/watch?v=BRxp1Kn1G7w


Files
-----

[conftest.py](conftest.py) содержит весь необходимый код для отлова неудачных тестовых случаев и создания снимка экрана
страницы на случай, если какой-либо тест не пройдёт.

[settings.py] - содержит тестовые данные

[pages/base.py](pages/base.py) содержит реализацию шаблона PageObject для Python.

[pages/elements.py](pages/elements.py) содержит вспомогательный класс для определения веб-элементов на веб-страницах.

[tests/](tests/test_general_searh.py, test_header_menu.py, test_per_area.py) содержат Web UI тесты для Лабиринт (https://labirint.ru/)


How To Run Tests
----------------

1) Install all requirements:

    ```bash
    pip3 install -r requirements
    ```

2) Download Selenium WebDriver from https://chromedriver.chromium.org/downloads (choose version which is compatible with your browser)

3) Run tests:

    ```bash
    python3 -m pytest -v --driver Chrome --driver-path ~/chrome tests/*
    ```

   ![alt text](example.png)

Note:
~/chrome in this example is the file of Selenium WebDriver downloaded and unarchived on step #2.
