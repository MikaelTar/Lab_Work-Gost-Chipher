Лабораторная работа 2: Хэширование с использованием ГОСТ 28147-89

Цель работы:

Реализовать алгоритм хэширования данных с использованием блочного шифра ГОСТ 28147-89. Программа должна позволять пользователю вводить данные и ключ, а затем вычислять хэш-значение на основе введенных данных.

Описание алгоритма ГОСТ 28147-89:

ГОСТ 28147-89 — это советский и российский стандарт симметричного шифрования, который также может быть использован для хэширования данных. Алгоритм работает с блоками данных размером 64 бита (8 байт) и использует ключ длиной 256 бит (32 байта). Основные этапы работы алгоритма:

Шифрование блока данных:
Данные разбиваются на блоки по 64 бита.
Каждый блок шифруется с использованием ключа и таблицы замен.
Хэширование:
Хэш-значение вычисляется по формуле: H(i) = E(H(i-1)) ⊕ M(i), где:
H(i-1) — предыдущее хэш-значение.
E — функция шифрования ГОСТ 28147-89.
M(i) — текущий блок данных.
Как пользоваться приложением:

Запуск программы:
Убедитесь, что у вас установлен Python и библиотека PyQt5.
Запустите программу, выполнив команду:
bash
Copy
python GOSTHashApp.py
Ввод данных:
Ключ: Введите ключ длиной 32 байта в поле "Ключ (32 байта)".
Данные: Введите данные для хэширования в поле "Введите данные для хэширования".
Хэширование:
Нажмите кнопку "Хэшировать".
Результат хэширования будет отображен в поле "Результат" в шестнадцатеричном формате.
Установка необходимых библиотек:

Для работы программы необходимо установить библиотеку PyQt5. Выполните следующую команду:

bash
Copy
pip install PyQt5
Пример работы:

Ввод данных:
Ключ: 12345678901234567890123456789012
Данные: Привет, мир!
Результат хэширования:
После нажатия кнопки "Хэшировать" в поле "Результат" отобразится хэш-значение, например:
Copy
3a4b5c6d7e8f9a0b
Особенности программы:

Интерфейс:
Программа имеет графический интерфейс, созданный с использованием библиотеки PyQt5.
Пользователь может вводить данные и ключ через текстовые поля.
Хэширование:
Программа вычисляет хэш-значение с использованием алгоритма ГОСТ 28147-89.
Результат отображается в шестнадцатеричном формате.
Обработка ошибок:
Если ключ имеет неправильную длину (не 32 байта), программа выводит сообщение об ошибке.
Автор:

Таран Михаил Иванович
Группа ИТ-41
Примечания:

Программа реализована в рамках лабораторной работы по курсу "Криптографические методы защиты информации".
Исходный код программы находится в файле GOSTHashApp.py.
