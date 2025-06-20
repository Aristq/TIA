1. Теоретические основы информационной безопасности
1. Дайте определение угрозам информационной безопасности и их классификация.

Угроза информационной безопасности — это потенциальное событие или действие, которое может нанести ущерб конфиденциальности, целостности или доступности информации.
Классификация угроз:

По источнику: внутренние (сотрудники), внешние (взлом снаружи);

По характеру: умышленные (атаки), случайные (ошибки);

По способу реализации: программные, аппаратные, организационные.

2. Перечислите основные виды атак на информационные системы и их характеристики.

DoS/DDoS — перегрузка ресурсов, отказ в обслуживании;

Фишинг — обман пользователей для получения конфиденциальных данных;

SQL-инъекции — внедрение вредоносного SQL-кода;

XSS — выполнение вредоносных скриптов в браузере;

Brute force — перебор логинов и паролей;

MITM (Man-in-the-middle) — перехват и изменение передаваемых данных.

3. Какие методы используются для обнаружения и предотвращения угроз в информационных системах?

Сигнатурный анализ (IDS/IPS);

Аномальный анализ поведения;

SIEM-системы;

Антивирусы и брандмауэры;

Сканеры уязвимостей (Nessus, OpenVAS).

4. Чем отличаются сигнатурные и аномальные методы обнаружения угроз?

Сигнатурные методы ищут совпадения с известными шаблонами атак (быстро, но неэффективно против новых угроз).

Аномальные методы фиксируют отклонения от нормального поведения системы (могут обнаружить новые угрозы, но есть риск ложных срабатываний).

5. Опишите роль политики информационной безопасности в предотвращении угроз.
Политика ИБ определяет принципы, правила и процедуры обеспечения безопасности. Она регулирует доступ, поведение сотрудников, реагирование на инциденты и помогает минимизировать риски угроз.

2. Анализ сетевого трафика и логи
6. Как проводится анализ сетевого трафика с использованием инструментов, таких как Wireshark?
Wireshark позволяет захватывать и анализировать сетевые пакеты в реальном времени. Анализ включает фильтрацию трафика по IP, портам и протоколам, проверку заголовков, выявление подозрительных пакетов или взаимодействий.

7. Какие типы информации содержатся в логах сетевых устройств?

IP-адреса источника и назначения;

Дата и время события;

Протоколы;

Ошибки, предупреждения;

Попытки доступа;

Состояния соединений.

8. Что такое индикаторы компрометации (IoC), и как они используются в системах анализа логов?
IoC (Indicators of Compromise) — это признаки, указывающие на факт взлома или атаки. Примеры: вредоносные IP, хэши файлов, домены. Используются для автоматического обнаружения и реагирования на инциденты в SIEM и IDS.

9. Какую роль играют метаданные в анализе сетевого трафика?
Метаданные — это данные о данных. Они помогают без анализа содержимого установить: кто с кем взаимодействует, когда, как долго, с каким объемом данных — и выявить аномалии.

10. Какие типы атак можно выявить с помощью анализа сетевого трафика?

Сканирование портов;

DDoS-атаки;

Перехват сессий (MITM);

Использование уязвимостей протоколов;

Внезапное увеличение объема трафика (эксфильтрация данных).

3. Инструменты и технологии обнаружения угроз
11. Охарактеризуйте системы IDS и IPS. Приведите примеры.

IDS (Intrusion Detection System) — система обнаружения атак, например Snort, Suricata.

IPS (Intrusion Prevention System) — система предотвращения атак, способна блокировать трафик в реальном времени (например, Suricata в режиме IPS, Cisco IPS).

12. Какие возможности предоставляет ELK-стек для анализа угроз?
ELK (Elasticsearch, Logstash, Kibana):

Сбор и хранение логов (Logstash, Beats);

Индексация и поиск (Elasticsearch);

Визуализация, алерты и дашборды (Kibana);

Корреляция событий, выявление инцидентов.

13. Расскажите об особенностях работы Snort и Suricata.

Snort — легковесная IDS, основанная на сигнатурах, подходит для анализа пакетов и обнаружения атак.

Suricata — более современная, поддерживает многопоточность, работает как IDS/IPS/NSM, поддерживает JSON-логи, TLS-декодинг.

14. Что такое Zeek (Bro), и как он используется в анализе сетевого трафика?
Zeek — это сетевой анализатор событий, который не просто фиксирует пакеты, а анализирует поведение. Используется для создания подробных логов по сессиям, DNS, SSL, HTTP и другим протоколам. Поддерживает собственный язык скриптов.

15. Какие инструменты используются для автоматического реагирования на угрозы?

SOAR-платформы (например, Cortex XSOAR);

Wazuh;

OSSEC;

ELK с ElastAlert;

SIEM с функцией автоматических действий (IBM QRadar, Splunk).

4. Методы и алгоритмы выявления угроз
16. Объясните принципы работы алгоритмов машинного обучения для анализа сетевого трафика.
ML-алгоритмы обучаются на примерах нормального и аномального трафика. Они могут классифицировать пакеты, искать закономерности и отклонения. Примеры алгоритмов: деревья решений, SVM, нейросети.

17. Чем отличается кластеризация от классификации в контексте анализа угроз?

Классификация — определение принадлежности объекта к заранее известному классу (атака/не атака).

Кластеризация — группировка похожих объектов без заранее заданных меток (например, выявление новых типов аномалий).

18. Какие параметры сетевого трафика могут использоваться для выявления аномалий?

Частота и объем соединений;

Средний размер пакетов;

Количество запросов за единицу времени;

IP-адреса и порты;

Протоколы и флаги TCP.

19. Как работают алгоритмы обнаружения DDoS-атак?
Они анализируют резкое увеличение количества запросов, нестандартные паттерны активности, одинаковые IP-адреса. Используются статистические и ML-методы, которые сравнивают поведение с нормой.

20. Что такое статистические методы анализа сетевого трафика?
Это методы, основанные на сборе и анализе числовых характеристик трафика (среднее, медиана, дисперсия, плотность вероятности). Применяются для выявления аномалий и трендов.

5. Мониторинг и реагирование на инциденты
21. Какие этапы включает процесс мониторинга информационной системы?

Сбор данных (логи, трафик);

Обнаружение инцидентов;

Анализ и корреляция;

Уведомление и реагирование;

Документирование;

Аудит и улучшения.

22. Что такое система SIEM, и как она применяется в анализе угроз?
SIEM (Security Information and Event Management) — платформа для сбора, хранения, анализа и корреляции логов. Позволяет выявлять и реагировать на угрозы в режиме реального времени.

23. Как организована работа систем оповещения о подозрительных событиях в ELK?
С помощью ElastAlert или Watcher можно настроить правила, при срабатывании которых отправляется уведомление на почту, в Slack или в SIEM. Используются фильтры и пороговые значения.

24. Какие действия выполняются при реагировании на инциденты?

Идентификация инцидента;

Изоляция системы;

Устранение уязвимости;

Восстановление работы;

Анализ и отчёт;

Обновление политик безопасности.

25. Как документируются выявленные угрозы и инциденты?

Создаются отчёты: что произошло, когда, какие системы затронуты;

Указываются меры реагирования;

Хранятся логи, скриншоты, IoC;

Используется формат STIX/TAXII, журналы SIEM.

6. Современные тенденции и технологии
26. Какие современные угрозы информационной безопасности наиболее актуальны?

Целевые атаки (APT);

Вымогатели (ransomware);

Supply chain атаки;

Фишинг и социальная инженерия;

Угрозы для IoT и мобильных устройств.

27. Расскажите о применении искусственного интеллекта в обнаружении и классификации угроз.
ИИ используется для:

Обнаружения аномалий;

Классификации атак;

Предиктивной аналитики;

Автоматического реагирования (SOAR);

Умного анализа поведения пользователей (UEBA).

28. Что такое киберугрозы, связанные с IoT-устройствами, и как их предотвращать?
IoT-устройства часто имеют уязвимости: слабые пароли, отсутствие обновлений.
Меры защиты:

Сегментация сети;

Обновления ПО;

Ограничение доступа;

IDS/IPS;

Установка доверенных сертификатов.

29. Как используются блочные цепи (blockchain) в системах информационной безопасности?
Blockchain применяется для:

Защиты журналов логов от подмены;

Доверенной аутентификации;

Цифровых подписей;

Проверки целостности данных.

30. Какие преимущества и ограничения имеют облачные системы анализа угроз?
Преимущества: масштабируемость, доступность, автоматизация.
Ограничения: зависимость от провайдера, вопросы конфиденциальности, регуляторные ограничения.

7. Нормативные документы и стандарты
31. Какие требования к обеспечению информационной безопасности содержатся в стандарте ISO/IEC 27001?
ISO/IEC 27001 устанавливает требования к системе управления информационной безопасностью (СУИБ), включая:

Оценку рисков;

Контроль доступа;

Политику безопасности;

Управление инцидентами;

Постоянное улучшение.

32. Что регламентирует ГОСТ Р 57580.1-2017?
Это стандарт по ИБ в финансовом секторе РФ. Устанавливает уровни защищённости, требования к контролю доступа, криптографии, управлению инцидентами и рисками.

33. Какие рекомендации дает NIST по организации систем обнаружения и предотвращения вторжений?
NIST (например, SP 800-94) рекомендует:

Использовать многослойную защиту;

Разделять сеть;

Применять IDS/IPS;

Вести аудит и логирование;

Регулярно обновлять правила и сигнатуры.

34. Какова роль нормативных документов в обеспечении информационной безопасности организаций?
Они задают единые стандарты, помогают соблюсти законодательство, минимизируют риски, способствуют внедрению проверенных практик ИБ.

35. Перечислите основные стандарты и руководства в области мониторинга и предотвращения угроз.

ISO/IEC 27001, 27002;

NIST SP 800-53, 800-94;

ГОСТ Р 57580.1-2017;

PCI DSS (для финансов);

OWASP (для веб-приложений).
