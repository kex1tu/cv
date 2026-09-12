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
| **Языки** | C++17/20, C |
| **Парадигмы** | STL, RAII, Rule of 3/5/0, Move-семантика, ООП |
| **Библиотеки** | Qt 5/6 (Widgets, WebSockets, Network), Monocypher, Opus |
| **Инфраструктура** | Git, CMake, Docker, GitHub Actions, GCC/Clang, Linux |
| **Тестирование** | GTest, Valgrind Memcheck, Heaptrack |
| **БД и Протоколы** | PostgreSQL, SQLite, WebSocket, TCP/IP, TCP/UDP, L3-L7 |
| **Английский** | В2-B2+ (Upper-Intermediate) - свободное чтение документации |

---

## Проекты

### YADRO TATLIN.UNIFIED DataPath (Test Task) - C++ - [github.com/kex1tu/test_Tatlin.Unified-DataPath](https://github.com/kex1tu/test_Tatlin.Unified-DataPath)
*Реализация алгоритма внешней сортировки для устройства хранения типа «магнитная лента» в условиях жестких ограничений RAM.*
- **Алгоритмы и I/O:** Разработана K-way внешняя сортировка слиянием (min-heap на std::priority_queue) в связке с поразрядной сортировкой (Radix Sort). Динамический расчет потребления памяти и многоуровневое слияние файлов для обхода лимитов ОС на дескрипторы.
- **Архитектура и качество кода:** Строгое следование RAII и стандартам C++17, ООП-интерфейсы. Полное покрытие юнит-тестами (Google Test), контроль утечек памяти через Valgrind Memcheck. CI/CD автоматизация (cppcheck, clang-format) через GitHub Actions.
- **Автоматизация:** Написание Python-скриптов для генерации бинарных датасетов и автоматической валидации результатов сортировки.

### Infotecs Web Service — C++/Boost.Asio - [github.com/kex1tu/test_infotecs.issledovatel_C_Cpp](https://github.com/kex1tu/test_infotecs.issledovatel_C_Cpp)
*Тестовое задание (Исследователь-системный программист): асинхронный REST-сервис для выборки из PostgreSQL.*
- **Сеть и производительность:** Boost.Asio/Boost.Beast, пул из 4 worker-потоков, отдельный acceptor-поток; потокобезопасный пул соединений к БД (RAII-страж DbConnectionGuard) — устраняет накладные расходы на TCP-handshake при каждом запросе.
- **БД:** PostgreSQL + libpqxx, индекс по (ts, level), параметризованные запросы, фильтрация и лимит выдачи.
- **Эксплуатация:** graceful shutdown по SIGINT/SIGTERM (boost::asio::signal_set), спецификация OpenAPI 3.1.0.
- **Тестирование:** юнит- и интеграционные тесты (CTest), Valgrind Memcheck.

### Infotecs Logger + Stat Server — C++ - [github.com/kex1tu/test_infotecs.DeveloperCpp](https://github.com/kex1tu/test_infotecs.DeveloperCpp)
*Тестовое задание (Разработчик C++): библиотека многоуровневого логирования и сервер агрегации метрик.*
- **Библиотека логирования:** static/shared сборка, Strategy-паттерн (ISink) для файлового и сетевого (TCP) вывода без изменения ядра Logger; zero-exceptions с кодами возврата (LoggerError, Result<T>).
- **Многопоточность:** потокобезопасная блокирующая очередь (mutex + condition_variable) для передачи сообщений из потока ввода в поток записи.
- **Сервер статистики:** мультиплексирующий TCP-сервер (poll) с расчетом метрик (min/max/avg длин, счетчики по уровням, скользящее окно за час).
- **Инфраструктура:** Tests, Valgrind, CI (GitHub Actions), clang-tidy/clang-format.

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

---
*Резюме актуально на 09.2026. Готов к стажировкам.*
