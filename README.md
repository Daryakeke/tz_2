# Техническое задание 2
![JavaCI](https://github.com/Daryakeke/tz2/actions/workflows/checker.yml/badge.svg)
------
### Описание проекта
Данная программа позволяет в файле, заполненного целыми (integer) числами, находить минимум, максимум, сумму и произведение.
### Установка программы
Для установки пользователю понадобится IntelliJ IDEA IDE. Необходимо загрузить содержимое директорий idea и src на Вашу машину, затем открыть проект с помощью IntelliJ IDEA. Альтернативно, пользователь может воспользоваться функциями (_max, _min, _sum, _mult), которые предоставляются в основном классе программы, и имплементировать их в свой код.
### Функционал программы
Программа позволяет находить минимум и максимум среди значений в изначальном файле (результат работы этих функций ограничен типом данных integer), а также сумму и произведение всех чисел в файле (результат работы этих функций ограничен типом данных long). Все значения выводятся едино после запуска программы, кроме того, производится вывод занявшего исполнением программы времени (в милисекундах).
Данные для работы всех вышеперечисленных функций берутся из локального файла, имя которого пользователь указывает при запуске основной программы.
Также в проекте есть 26 тестов, которые ответственны за проверку всех функций при увеличивающемся размере входных данных, а также за анализ работы функций максимума и минимума в крайних случаях. Также есть тесты, которые проверяют функцию поиска произведения (_mult) на выход за пределы типа данных long. 
### Ввод и вывод
В зависимости от нахождения файла с данными, которые задействуется в ходе работы программы, пользователю может понадобится ввести как просто имя файла с расширением, так и полный путь до файла.
*Пример работы программы:*
Название файла: test.txt, лежащий в той же папке, что и программа. Содержимое файла: "1 2 3 4 5 6 7 8 9". Ввод пользователя: "test.txt". Вывод программы: \
Минимум: 1 \
Максимум: 9 \
Сумма: 45 \
Произведение: 362880 \
Программа выполнилась за: 11 миллисекунд
Для запуска же тестов необходимо открыть tz_2_programTest.java в IntelliJ IDEA, а затем нажать на галочку рядом с public class tz_2_programTest.
### Время работы в зависимости от количества данных в файле
На этом графике изображена зависимость выполнения программы (то есть при выполнении всех функций: _max, _min, _sum, _mult) в зависимости от количества чисел в входном файле. \
\
![Image alt](https://github.com/Daryakeke/tz2/raw/main/time_tz2.jpg)
### Работа с GitHub Actions в репозитории
При любом коммите автоматически запускаются 26 тестов, которые проверяют корректность работы программы. Эти тесты так же можно запустить вручную, перейдя в Actions, затем в Java CI, там в строке *"This workflow has a workflow_dispatch event trigger."* нажать на кнопку "Run workflow", после чего в выпадающем меню снова нажать "Run workflow" без изменения поля branch.
### Telegram бот
К проекту привязан Telegram бот, который посылает уведомления о коммитах: название коммита, в каком репозитории, а также статус прохождения тестов: passing (все тесты пройдены) или failing (есть ошибка в работе).
