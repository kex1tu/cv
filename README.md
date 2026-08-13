# Михеев Григорий

**C++ Developer**  
Санкт-Петербург / Удалённо  
8 (952)-263-06-52 - [grishasev@bk.ru](mailto:grishasev@bk.ru) - [@kex1tu](https://t.me/kex1tu) - [github.com/kex1tu](https://github.com/kex1tu)

---

## Образование

**Санкт-Петербургский государственный университет (СПбГУ)**  
Факультет ПМ-ПУ | Направление: Программирование и информационные технологии  
*2024 - 2028 (3 курс)*

---

## Навыки

| Категория | Технологии |
|-----------|-----------|
| **Языки** | C++17/20, C|
| **Парадигмы** | STL, RAII, Rule of 3/5/0, Move-семантика, ООП |
| **Библиотеки** | Qt 5/6 (Widgets, WebSockets, Network), Monocypher, Opus |
| **Инфраструктура** | Git, CMake, Docker, GitHub Actions, GCC/Clang, Linux |
| **Тестирование** | Google Test (GTest), Valgrind Memcheck, Heaptrack |
| **БД и Протоколы** | PostgreSQL, SQLite, WebSocket, TCP/IP, TCP/UDP, L3-L7 |
| **Английский** | В2-B2+ (Upper-Intermediate) - свободное чтение документации |

---

## Проекты

### YADRO TATLIN.UNIFIED DataPath (Test Task) - C++ - [github.com/kex1tu/test_Tatlin.Unified-DataPath](https://github.com/kex1tu/test_Tatlin.Unified-DataPath)
*Реализация алгоритма внешней сортировки для устройства хранения типа «магнитная лента» в условиях жестких ограничений RAM.*
- **Алгоритмы и I/O:** Разработана K-way внешняя сортировка слиянием (min-heap на std::priority_queue) в связке с поразрядной сортировкой (Radix Sort). Динамический расчет потребления памяти и многоуровневое слияние файлов для обхода лимитов ОС на дескрипторы.
- **Архитектура и качество кода:** Строгое следование RAII и стандартам C++17, ООП-интерфейсы. Полное покрытие юнит-тестами (Google Test), контроль утечек памяти через Valgrind Memcheck. CI/CD автоматизация (cppcheck, clang-format) через GitHub Actions.
- **Автоматизация:** Написание Python-скриптов для генерации бинарных датасетов и автоматической валидации результатов сортировки.

### Slav Messenger - C++/Qt - [github.com/kex1tu/slav_Messenger](https://github.com/kex1tu/slav_Messenger)
*Защищенный мессенджер с E2EE, VoIP*
- **Серверная часть на C++:** обработка подключений через WebSocket, хранение данных в PostgreSQL, протокол для обмена публичными ключами
- **Криптография:** Реализация E2EE (X25519 + ChaCha20-Poly1305) через Monocypher; хеширование паролей Argon2.
- **VoIP:** Интеграция кодека Opus для передачи аудио в реальном времени с низкой задержкой.
- **Desktop:** Qt 5/6 Widgets с использованием Model/View (кастомные модели и делегаты) для отображения чатов и списков.

### BigInteger Library - C++ - [github.com/kex1tu/big_integer](https://github.com/kex1tu/big_integer)
*Библиотека для работы с числами произвольной точности без сторонних зависимостей.*
- **Реализация:** Знаковый BigInt, хранение в base-2^32 (массив uint32_t), поддержка арифметики (+, -, *, /), RSA-шифрование на базе библиотеки.
- **Качество кода:** Следование Rule of 5, использование Move-семантики.
- **Инфраструктура:** **Полное покрытие Google Test**, автоматизация сборки и тестов через **Docker + GitHub Actions**.

### DateTime Library - C++ - [github.com/kex1tu/date_time](https://github.com/kex1tu/date_time)
*Набор классов (date, time, datetime, timediff) для работы со временем.*
- **Функционал:** Арифметика дат, корректная обработка високосных лет, форматирование.
- **Инфраструктура:** Юнит-тестирование (**GTest**), автоматизация сборки и тестов через **Docker + GitHub Actions**.

### Прочие задачи - C++ - [github.com/kex1tu/some_tasks](https://github.com/kex1tu/some_tasks)
- **Busy Beaver:** Эмулятор машины Тьюринга.
- **Crockford's Base32:** Эффективная работа с битами и кодированием данных.
- **Gauss Circle Problem:** Оптимизация вычислений до O(R) при огромных радиусах (2*10^9).
- **MatrixCalc:** Линейная алгебра без использования STL.

---
*Резюме актуально на 08.2026. Готов к стажировкам.*
