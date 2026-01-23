# Расшифровка значения Post-кодов для китайских LGA2011\2011-3 плат

[Источник] (https://e5450.com/rasshifrovka-post-kodov-dlya-kitajskih-lga2011/)

Таблицы взятые из PDF документов помогут понять, что именно значит каждый конкретный пост-код или бип-сигнал на материнских платах сокета 2011 и 2011-3 китайского производства.

Подойдет инструкция также и для любых других плат, работающих на биосе Aptio 4.x (на этой версии работают китайские платы на сокетах 2011 и 1356) и 5.x (для плат на 2011-3) от American Megatrends.

Сами коды в инструкции представлены в виде 0xB7, при этом на встроенном в некоторые платы индикаторе отображаться они будут без 0x, то есть просто B7.

## Aptio 4.x Status Codes (AMI Aptio 4.x) — перевод на русский

Источник: *Aptio 4.x Status Codes — Checkpoints & Beep Codes for Debugging*, Rev 1.13 (2013‑03‑14). fileciteturn0file0

> Примечание: коды ниже — **стандартные** (generic) для Aptio 4.x и не включают специфичные для чипсета/платы OEM коды.

---

### Диапазоны кодов (Checkpoint ranges)

| Диапазон | Описание (EN) | Перевод (RU) |
|---|---|---|
| 0x01–0x0B | SEC execution | Выполнение фазы SEC |
| 0x0C–0x0F | SEC errors | Ошибки фазы SEC |
| 0x10–0x2F | PEI execution up to and including memory detection | Выполнение PEI до и включая обнаружение памяти |
| 0x30–0x4F | PEI execution after memory detection | Выполнение PEI после обнаружения памяти |
| 0x50–0x5F | PEI errors | Ошибки PEI |
| 0x60–0x8F | DXE execution up to BDS | Выполнение DXE до фазы BDS |
| 0x90–0xCF | BDS execution | Выполнение фазы BDS |
| 0xD0–0xDF | DXE errors | Ошибки DXE |
| 0xE0–0xE8 | S3 Resume (PEI) | Возврат из S3 (PEI) |
| 0xE9–0xEF | S3 Resume errors (PEI) | Ошибки возврата из S3 (PEI) |
| 0xF0–0xF8 | Recovery (PEI) | Восстановление (PEI) |
| 0xF9–0xFF | Recovery errors (PEI) | Ошибки восстановления (PEI) |

---

### SEC Phase

#### Стандартные коды (Progress)

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x00 | Not used | Не используется |
| 0x01 | Power on. Reset type detection (soft/hard). | Включение питания. Определение типа сброса (мягкий/жёсткий). |
| 0x02 | AP initialization before microcode loading | Инициализация AP (доп. процессоров/ядер) до загрузки микрокода |
| 0x03 | North Bridge initialization before microcode loading | Инициализация северного моста до загрузки микрокода |
| 0x04 | South Bridge initialization before microcode loading | Инициализация южного моста до загрузки микрокода |
| 0x05 | OEM initialization before microcode loading | Инициализация OEM до загрузки микрокода |
| 0x06 | Microcode loading | Загрузка микрокода |
| 0x07 | AP initialization after microcode loading | Инициализация AP после загрузки микрокода |
| 0x08 | North Bridge initialization after microcode loading | Инициализация северного моста после загрузки микрокода |
| 0x09 | South Bridge initialization after microcode loading | Инициализация южного моста после загрузки микрокода |
| 0x0A | OEM initialization after microcode loading | Инициализация OEM после загрузки микрокода |
| 0x0B | Cache initialization | Инициализация кэша |

#### SEC Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x0C–0x0D | Reserved for future AMI SEC error codes | Зарезервировано для будущих ошибок SEC (AMI) |
| 0x0E | Microcode not found | Микрокод не найден |
| 0x0F | Microcode not loaded | Микрокод не загружен |

#### SEC Beep Codes
Нет. (None)

---

### PEI Phase

#### Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x10 | PEI Core is started | Запущено ядро PEI |
| 0x11 | Pre-memory CPU initialization is started | Старт пред-памятной инициализации CPU |
| 0x12 | Pre-memory CPU initialization (CPU module specific) | Пред-памятная инициализация CPU (зависит от модуля CPU) |
| 0x13 | Pre-memory CPU initialization (CPU module specific) | Пред-памятная инициализация CPU (зависит от модуля CPU) |
| 0x14 | Pre-memory CPU initialization (CPU module specific) | Пред-памятная инициализация CPU (зависит от модуля CPU) |
| 0x15 | Pre-memory North Bridge initialization is started | Старт пред-памятной инициализации северного моста |
| 0x16 | Pre-Memory North Bridge initialization (North Bridge module specific) | Пред-памятная инициализация северного моста (зависит от модуля) |
| 0x17 | Pre-Memory North Bridge initialization (North Bridge module specific) | Пред-памятная инициализация северного моста (зависит от модуля) |
| 0x18 | Pre-Memory North Bridge initialization (North Bridge module specific) | Пред-памятная инициализация северного моста (зависит от модуля) |
| 0x19 | Pre-memory South Bridge initialization is started | Старт пред-памятной инициализации южного моста |
| 0x1A | Pre-memory South Bridge initialization (South Bridge module specific) | Пред-памятная инициализация южного моста (зависит от модуля) |
| 0x1B | Pre-memory South Bridge initialization (South Bridge module specific) | Пред-памятная инициализация южного моста (зависит от модуля) |
| 0x1C | Pre-memory South Bridge initialization (South Bridge module specific) | Пред-памятная инициализация южного моста (зависит от модуля) |
| 0x1D–0x2A | OEM pre-memory initialization codes | OEM‑коды пред‑памятной инициализации |
| 0x2B | Memory initialization. Serial Presence Detect (SPD) data reading | Инициализация памяти. Чтение SPD данных |
| 0x2C | Memory initialization. Memory presence detection | Инициализация памяти. Обнаружение модулей памяти |
| 0x2D | Memory initialization. Programming memory timing information | Инициализация памяти. Программирование таймингов |
| 0x2E | Memory initialization. Configuring memory | Инициализация памяти. Конфигурирование памяти |
| 0x2F | Memory initialization (other). | Инициализация памяти (прочее) |
| 0x30 | Reserved for ASL (see ASL Status Codes section below) | Зарезервировано для ASL (см. раздел ASL) |
| 0x31 | Memory Installed | Память установлена |
| 0x32 | CPU post-memory initialization is started | Старт пост‑памятной инициализации CPU |
| 0x33 | CPU post-memory initialization. Cache initialization | Пост‑памятная инициализация CPU. Инициализация кэша |
| 0x34 | CPU post-memory initialization. Application Processor(s) (AP) initialization | Пост‑памятная инициализация CPU. Инициализация AP |
| 0x35 | CPU post-memory initialization. Boot Strap Processor (BSP) selection | Пост‑памятная инициализация CPU. Выбор BSP |
| 0x36 | CPU post-memory initialization. System Management Mode (SMM) initialization | Пост‑памятная инициализация CPU. Инициализация SMM |
| 0x37 | Post-Memory North Bridge initialization is started | Старт пост‑памятной инициализации северного моста |
| 0x38 | Post-Memory North Bridge initialization (North Bridge module specific) | Пост‑памятная инициализация северного моста (зависит от модуля) |
| 0x39 | Post-Memory North Bridge initialization (North Bridge module specific) | Пост‑памятная инициализация северного моста (зависит от модуля) |
| 0x3A | Post-Memory North Bridge initialization (North Bridge module specific) | Пост‑памятная инициализация северного моста (зависит от модуля) |
| 0x3B | Post-Memory South Bridge initialization is started | Старт пост‑памятной инициализации южного моста |
| 0x3C | Post-Memory South Bridge initialization (South Bridge module specific) | Пост‑памятная инициализация южного моста (зависит от модуля) |
| 0x3D | Post-Memory South Bridge initialization (South Bridge module specific) | Пост‑памятная инициализация южного моста (зависит от модуля) |
| 0x3E | Post-Memory South Bridge initialization (South Bridge module specific) | Пост‑памятная инициализация южного моста (зависит от модуля) |
| 0x3F–0x4E | OEM post memory initialization codes | OEM‑коды пост‑памятной инициализации |
| 0x4F | DXE IPL is started | Запущен DXE IPL |

#### PEI Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x50 | Memory initialization error. Invalid memory type or incompatible memory speed | Ошибка инициализации памяти: неверный тип или несовместимая скорость |
| 0x51 | Memory initialization error. SPD reading has failed | Ошибка инициализации памяти: не удалось прочитать SPD |
| 0x52 | Memory initialization error. Invalid memory size or memory modules do not match. | Ошибка инициализации памяти: неверный размер или модули не совпадают |
| 0x53 | Memory initialization error. No usable memory detected | Ошибка инициализации памяти: не обнаружено пригодной памяти |
| 0x54 | Unspecified memory initialization error. | Неуточнённая ошибка инициализации памяти |
| 0x55 | Memory not installed | Память не установлена |
| 0x56 | Invalid CPU type or Speed | Неверный тип CPU или частота |
| 0x57 | CPU mismatch | Несоответствие CPU |
| 0x58 | CPU self test failed or possible CPU cache error | Самотест CPU не пройден или возможна ошибка кэша |
| 0x59 | CPU micro-code is not found or micro-code update is failed | Микрокод CPU не найден или обновление микрокода не удалось |
| 0x5A | Internal CPU error | Внутренняя ошибка CPU |
| 0x5B | reset PPI is not available | Reset PPI недоступен |
| 0x5C–0x5F | Reserved for future AMI error codes | Зарезервировано для будущих ошибок AMI |

#### S3 Resume (PEI) — Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xE0 | S3 Resume is stared (S3 Resume PPI is called by the DXE IPL) | Начат возврат из S3 (S3 Resume PPI вызван DXE IPL) |
| 0xE1 | S3 Boot Script execution | Выполнение S3 Boot Script |
| 0xE2 | Video repost | Повторная инициализация видео (repost) |
| 0xE3 | OS S3 wake vector call | Вызов wake‑вектора ОС для S3 |
| 0xE4–0xE7 | Reserved for future AMI progress codes | Зарезервировано для будущих прогресс‑кодов AMI |

#### S3 Resume (PEI) — Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xE8 | S3 Resume Failed | Ошибка возврата из S3 |
| 0xE9 | S3 Resume PPI not Found | S3 Resume PPI не найден |
| 0xEA | S3 Resume Boot Script Error | Ошибка S3 Boot Script |
| 0xEB | S3 OS Wake Error | Ошибка пробуждения ОС из S3 |
| 0xEC–0xEF | Reserved for future AMI error codes | Зарезервировано для будущих ошибок AMI |

#### Recovery (PEI) — Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xF0 | Recovery condition triggered by firmware (Auto recovery) | Режим восстановления инициирован прошивкой (автовосстановление) |
| 0xF1 | Recovery condition triggered by user (Forced recovery) | Режим восстановления инициирован пользователем (принудительно) |
| 0xF2 | Recovery process started | Процесс восстановления запущен |
| 0xF3 | Recovery firmware image is found | Образ прошивки для восстановления найден |
| 0xF4 | Recovery firmware image is loaded | Образ прошивки для восстановления загружен |
| 0xF5–0xF7 | Reserved for future AMI progress codes | Зарезервировано для будущих прогресс‑кодов AMI |

#### Recovery (PEI) — Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xF8 | Recovery PPI is not available | Recovery PPI недоступен |
| 0xF9 | Recovery capsule is not found | Капсула восстановления не найдена |
| 0xFA | Invalid recovery capsule | Некорректная капсула восстановления |
| 0xFB–0xFF | Reserved for future AMI error codes | Зарезервировано для будущих ошибок AMI |

#### PEI Beep Codes

| Бипов | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 1 | Memory not Installed | Память не установлена |
| 1 | Memory was installed twice (InstallPeiMemory routine in PEI Core called twice) | Память “установлена” дважды (InstallPeiMemory в PEI Core вызван два раза) |
| 2 | Recovery started | Восстановление запущено |
| 3 | DXEIPL was not found | DXE IPL не найден |
| 3 | DXE Core Firmware Volume was not found | Том прошивки DXE Core (Firmware Volume) не найден |
| 4 | Recovery failed | Восстановление не удалось |
| 4 | S3 Resume failed | Возврат из S3 не удался |
| 7 | Reset PPI is not available | Reset PPI недоступен |

---

### DXE Phase (включая BDS коды)

#### DXE / BDS Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x60 | DXE Core is started | Запущено ядро DXE |
| 0x61 | NVRAM initialization | Инициализация NVRAM |
| 0x62 | Installation of the South Bridge Runtime Services | Установка runtime‑сервисов южного моста |
| 0x63 | CPU DXE initialization is started | Старт DXE‑инициализации CPU |
| 0x64 | CPU DXE initialization (CPU module specific) | DXE‑инициализация CPU (зависит от модуля CPU) |
| 0x65 | CPU DXE initialization (CPU module specific) | DXE‑инициализация CPU (зависит от модуля CPU) |
| 0x66 | CPU DXE initialization (CPU module specific) | DXE‑инициализация CPU (зависит от модуля CPU) |
| 0x67 | CPU DXE initialization (CPU module specific) | DXE‑инициализация CPU (зависит от модуля CPU) |
| 0x68 | PCI host bridge initialization | Инициализация PCI host bridge |
| 0x69 | North Bridge DXE initialization is started | Старт DXE‑инициализации северного моста |
| 0x6A | North Bridge DXE SMM initialization is started | Старт SMM‑инициализации северного моста (DXE) |
| 0x6B | North Bridge DXE initialization (North Bridge module specific) | DXE‑инициализация северного моста (зависит от модуля) |
| 0x6C | North Bridge DXE initialization (North Bridge module specific) | DXE‑инициализация северного моста (зависит от модуля) |
| 0x6D | North Bridge DXE initialization (North Bridge module specific) | DXE‑инициализация северного моста (зависит от модуля) |
| 0x6E | North Bridge DXE initialization (North Bridge module specific) | DXE‑инициализация северного моста (зависит от модуля) |
| 0x6F | North Bridge DXE initialization (North Bridge module specific) | DXE‑инициализация северного моста (зависит от модуля) |
| 0x70 | South Bridge DXE initialization is started | Старт DXE‑инициализации южного моста |
| 0x71 | South Bridge DXE SMM initialization is started | Старт SMM‑инициализации южного моста (DXE) |
| 0x72 | South Bridge devices initialization | Инициализация устройств южного моста |
| 0x73 | South Bridge DXE Initialization (South Bridge module specific) | DXE‑инициализация южного моста (зависит от модуля) |
| 0x74 | South Bridge DXE Initialization (South Bridge module specific) | DXE‑инициализация южного моста (зависит от модуля) |
| 0x75 | South Bridge DXE Initialization (South Bridge module specific) | DXE‑инициализация южного моста (зависит от модуля) |
| 0x76 | South Bridge DXE Initialization (South Bridge module specific) | DXE‑инициализация южного моста (зависит от модуля) |
| 0x77 | South Bridge DXE Initialization (South Bridge module specific) | DXE‑инициализация южного моста (зависит от модуля) |
| 0x78 | ACPI module initialization | Инициализация модуля ACPI |
| 0x79 | CSM initialization | Инициализация CSM |
| 0x7A–0x7F | Reserved for future AMI DXE codes | Зарезервировано для будущих DXE‑кодов AMI |
| 0x80–0x8F | OEM DXE initialization codes | OEM‑коды DXE‑инициализации |
| 0x90 | Boot Device Selection (BDS) phase is started | Запущена фаза выбора загрузочного устройства (BDS) |
| 0x91 | Driver connecting is started | Начато подключение драйверов |
| 0x92 | PCI Bus initialization is started | Старт инициализации PCI шины |
| 0x93 | PCI Bus Hot Plug Controller Initialization | Инициализация контроллера горячего подключения PCI |
| 0x94 | PCI Bus Enumeration | Перечисление устройств PCI |
| 0x95 | PCI Bus Request Resources | Запрос ресурсов для PCI |
| 0x96 | PCI Bus Assign Resources | Назначение ресурсов для PCI |
| 0x97 | Console Output devices connect | Подключение устройств вывода консоли |
| 0x98 | Console input devices connect | Подключение устройств ввода консоли |
| 0x99 | Super IO Initialization | Инициализация Super I/O |
| 0x9A | USB initialization is started | Старт инициализации USB |
| 0x9B | USB Reset | Сброс USB |
| 0x9C | USB Detect | Обнаружение USB |
| 0x9D | USB Enable | Включение USB |
| 0x9E–0x9F | Reserved for future AMI codes | Зарезервировано для будущих кодов AMI |
| 0xA0 | IDE initialization is started | Старт инициализации IDE |
| 0xA1 | IDE Reset | Сброс IDE |
| 0xA2 | IDE Detect | Обнаружение IDE |
| 0xA3 | IDE Enable | Включение IDE |
| 0xA4 | SCSI initialization is started | Старт инициализации SCSI |
| 0xA5 | SCSI Reset | Сброс SCSI |
| 0xA6 | SCSI Detect | Обнаружение SCSI |
| 0xA7 | SCSI Enable | Включение SCSI |
| 0xA8 | Setup Verifying Password | Проверка пароля в Setup |
| 0xA9 | Start of Setup | Запуск Setup |
| 0xAA | Reserved for ASL (see ASL Status Codes section below) | Зарезервировано для ASL (см. раздел ASL) |
| 0xAB | Setup Input Wait | Ожидание ввода в Setup |
| 0xAC | Reserved for ASL (see ASL Status Codes section below) | Зарезервировано для ASL (см. раздел ASL) |
| 0xAD | Ready To Boot event | Событие Ready To Boot |
| 0xAE | Legacy Boot event | Событие Legacy Boot |
| 0xAF | Exit Boot Services event | Событие Exit Boot Services |
| 0xB0 | Runtime Set Virtual Address MAP Begin | Runtime: начало установки карты виртуальных адресов |
| 0xB1 | Runtime Set Virtual Address MAP End | Runtime: конец установки карты виртуальных адресов |
| 0xB2 | Legacy Option ROM Initialization | Инициализация Legacy Option ROM |
| 0xB3 | System Reset | Системный сброс |
| 0xB4 | USB hot plug | Горячее подключение USB |
| 0xB5 | PCI bus hot plug | Горячее подключение на PCI шине |
| 0xB6 | Clean-up of NVRAM | Очистка/уборка NVRAM |
| 0xB7 | Configuration Reset (reset of NVRAM settings) | Сброс конфигурации (сброс настроек NVRAM) |
| 0xB8–0xBF | Reserved for future AMI codes | Зарезервировано для будущих кодов AMI |
| 0xC0–0xCF | OEM BDS initialization codes | OEM‑коды инициализации BDS |

#### DXE Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xD0 | CPU initialization error | Ошибка инициализации CPU |
| 0xD1 | North Bridge initialization error | Ошибка инициализации северного моста |
| 0xD2 | South Bridge initialization error | Ошибка инициализации южного моста |
| 0xD3 | Some of the Architectural Protocols are not available | Некоторые архитектурные протоколы недоступны |
| 0xD4 | PCI resource allocation error. Out of Resources | Ошибка распределения PCI‑ресурсов: ресурсов не хватает |
| 0xD5 | No Space for Legacy Option ROM | Нет места для Legacy Option ROM |
| 0xD6 | No Console Output Devices are found | Не найдены устройства вывода консоли |
| 0xD7 | No Console Input Devices are found | Не найдены устройства ввода консоли |
| 0xD8 | Invalid password | Неверный пароль |
| 0xD9 | Error loading Boot Option (LoadImage returned error) | Ошибка загрузки Boot Option (LoadImage вернул ошибку) |
| 0xDA | Boot Option is failed (StartImage returned error) | Boot Option не запущен (StartImage вернул ошибку) |
| 0xDB | Flash update is failed | Обновление прошивки (flash) не удалось |
| 0xDC | Reset protocol is not available | Протокол Reset недоступен |

#### DXE Beep Codes

| Бипов | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 1 | Invalid password | Неверный пароль |
| 4 | Some of the Architectural Protocols are not available | Некоторые архитектурные протоколы недоступны |
| 5 | No Console Output Devices are found | Не найдены устройства вывода консоли |
| 5 | No Console Input Devices are found | Не найдены устройства ввода консоли |
| 6 | Flash update is failed | Обновление прошивки (flash) не удалось |
| 7 | Reset protocol is not available | Протокол Reset недоступен |
| 8 | Platform PCI resource requirements cannot be met | Невозможно удовлетворить требования платформы по PCI‑ресурсам |

---

### ACPI/ASL Checkpoints

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x01 | System is entering S1 sleep state | Переход системы в сон S1 |
| 0x02 | System is entering S2 sleep state | Переход системы в сон S2 |
| 0x03 | System is entering S3 sleep state | Переход системы в сон S3 |
| 0x04 | System is entering S4 sleep state | Переход системы в сон S4 |
| 0x05 | System is entering S5 sleep state | Переход системы в S5 (выключение) |
| 0x10 | System is waking up from the S1 sleep state | Выход системы из сна S1 |
| 0x20 | System is waking up from the S2 sleep state | Выход системы из сна S2 |
| 0x30 | System is waking up from the S3 sleep state | Выход системы из сна S3 |
| 0x40 | System is waking up from the S4 sleep state | Выход системы из сна S4 |
| 0xAC | System has transitioned into ACPI mode. Interrupt controller is in PIC mode. | Переход в ACPI‑режим. Контроллер прерываний в режиме PIC. |
| 0xAA | System has transitioned into ACPI mode. Interrupt controller is in APIC mode. | Переход в ACPI‑режим. Контроллер прерываний в режиме APIC. |

---

### OEM‑Reserved Checkpoint Ranges

| Код/диапазон | Описание (EN) | Перевод (RU) |
|---|---|---|
| 0x05 | OEM SEC initialization before microcode loading | OEM‑инициализация SEC до загрузки микрокода |
| 0x0A | OEM SEC initialization after microcode loading | OEM‑инициализация SEC после загрузки микрокода |
| 0x1D–0x2A | OEM pre-memory initialization codes | OEM‑коды пред‑памятной инициализации |
| 0x3F–0x4E | OEM PEI post memory initialization codes | OEM‑коды пост‑памятной инициализации PEI |
| 0x80–0x8F | OEM DXE initialization codes | OEM‑коды DXE‑инициализации |
| 0xC0–0xCF | OEM BDS initialization codes | OEM‑коды BDS‑инициализации |

## AMI Aptio 5.x — Status Codes (Checkpoints & Beep Codes) — перевод на русский

Источник: **AMI_Aptio_5.x_Status_Codes.pdf** (Aptio 5.x Status Codes, Rev 2.0, 2014-04-10).  

> Примечание: коды/диапазоны OEM (`OEM ...`) зависят от конкретной платы/BIOS-вендора.

---

### Диапазоны чекпоинтов (Checkpoint Ranges)

| Диапазон кода | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x01–0x0B | SEC execution | Выполнение фазы SEC |
| 0x0C–0x0F | SEC errors | Ошибки фазы SEC |
| 0x10–0x2F | PEI execution up to and including memory detection | Выполнение PEI до и включая обнаружение памяти |
| 0x30–0x4F | PEI execution after memory detection | Выполнение PEI после обнаружения памяти |
| 0x50–0x5F | PEI errors | Ошибки PEI |
| 0x60–0x8F | DXE execution up to BDS | Выполнение DXE до перехода в BDS |
| 0x90–0xCF | BDS execution | Выполнение BDS |
| 0xD0–0xDF | DXE errors | Ошибки DXE |
| 0xE0–0xE8 | S3 Resume (PEI) | Возврат из S3 (PEI) |
| 0xE9–0xEF | S3 Resume errors (PEI) | Ошибки возврата из S3 (PEI) |
| 0xF0–0xF8 | Recovery (PEI) | Восстановление (PEI) |
| 0xF9–0xFF | Recovery errors (PEI) | Ошибки восстановления (PEI) |

---

### SEC Phase

#### SEC — Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x00 | Not used | Не используется |
| 0x01 | Power on. Reset type detection (soft/hard). | Включение питания. Определение типа сброса (мягкий/жёсткий). |
| 0x02 | AP initialization before microcode loading | Инициализация AP (доп. процессоров/ядер) до загрузки микрокода |
| 0x03 | North Bridge initialization before microcode loading | Инициализация северного моста до загрузки микрокода |
| 0x04 | South Bridge initialization before microcode loading | Инициализация южного моста до загрузки микрокода |
| 0x05 | OEM initialization before microcode loading | OEM-инициализация до загрузки микрокода |
| 0x06 | Microcode loading | Загрузка микрокода |
| 0x07 | AP initialization after microcode loading | Инициализация AP после загрузки микрокода |
| 0x08 | North Bridge initialization after microcode loading | Инициализация северного моста после загрузки микрокода |
| 0x09 | South Bridge initialization after microcode loading | Инициализация южного моста после загрузки микрокода |
| 0x0A | OEM initialization after microcode loading | OEM-инициализация после загрузки микрокода |
| 0x0B | Cache initialization | Инициализация кэша |

#### SEC — Error Codes

| Код/диапазон | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x0C–0x0D | Reserved for future AMI SEC error codes | Зарезервировано для будущих ошибок SEC от AMI |
| 0x0E | Microcode not found | Микрокод не найден |
| 0x0F | Microcode not loaded | Микрокод не загружен |

#### SEC — Beep Codes

Нет.

---

### PEI Phase

#### PEI — Progress Codes (до обнаружения памяти)

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x10 | PEI Core is started | Запущено ядро PEI |
| 0x11 | Pre-memory CPU initialization is started | Начата пред-памятная инициализация CPU |
| 0x12 | Pre-memory CPU initialization (CPU module specific) | Пред-памятная инициализация CPU (зависит от CPU-модуля) |
| 0x13 | Pre-memory CPU initialization (CPU module specific) | Пред-памятная инициализация CPU (зависит от CPU-модуля) |
| 0x14 | Pre-memory CPU initialization (CPU module specific) | Пред-памятная инициализация CPU (зависит от CPU-модуля) |
| 0x15 | Pre-memory North Bridge initialization is started | Начата пред-памятная инициализация северного моста |
| 0x16 | Pre-Memory North Bridge initialization (North Bridge module specific) | Пред-памятная инициализация северного моста (зависит от модуля) |
| 0x17 | Pre-Memory North Bridge initialization (North Bridge module specific) | Пред-памятная инициализация северного моста (зависит от модуля) |
| 0x18 | Pre-Memory North Bridge initialization (North Bridge module specific) | Пред-памятная инициализация северного моста (зависит от модуля) |
| 0x19 | Pre-memory South Bridge initialization is started | Начата пред-памятная инициализация южного моста |
| 0x1A | Pre-memory South Bridge initialization (South Bridge module specific) | Пред-памятная инициализация южного моста (зависит от модуля) |
| 0x1B | Pre-memory South Bridge initialization (South Bridge module specific) | Пред-памятная инициализация южного моста (зависит от модуля) |
| 0x1C | Pre-memory South Bridge initialization (South Bridge module specific) | Пред-памятная инициализация южного моста (зависит от модуля) |
| 0x1D–0x2A | OEM pre-memory initialization codes | OEM-коды пред-памятной инициализации |
| 0x2B | Memory initialization. Serial Presence Detect (SPD) data reading | Инициализация памяти. Чтение SPD |
| 0x2C | Memory initialization. Memory presence detection | Инициализация памяти. Определение наличия модулей |
| 0x2D | Memory initialization. Programming memory timing information | Инициализация памяти. Программирование таймингов |
| 0x2E | Memory initialization. Configuring memory | Инициализация памяти. Конфигурирование памяти |
| 0x2F | Memory initialization (other). | Инициализация памяти (прочее) |

#### PEI — Progress Codes (после обнаружения памяти)

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x30 | Reserved for ASL (see ASL Status Codes section below) | Зарезервировано для ASL (см. раздел ASL) |
| 0x31 | Memory Installed | Память установлена |
| 0x32 | CPU post-memory initialization is started | Начата пост-памятная инициализация CPU |
| 0x33 | CPU post-memory initialization. Cache initialization | Пост-памятная инициализация CPU. Инициализация кэша |
| 0x34 | CPU post-memory initialization. Application Processor(s) (AP) initialization | Пост-памятная инициализация CPU. Инициализация AP |
| 0x35 | CPU post-memory initialization. Boot Strap Processor (BSP) selection | Пост-памятная инициализация CPU. Выбор BSP |
| 0x36 | CPU post-memory initialization. System Management Mode (SMM) initialization | Пост-памятная инициализация CPU. Инициализация SMM |
| 0x37 | Post-Memory North Bridge initialization is started | Начата пост-памятная инициализация северного моста |
| 0x38 | Post-Memory North Bridge initialization (North Bridge module specific) | Пост-памятная инициализация северного моста (зависит от модуля) |
| 0x39 | Post-Memory North Bridge initialization (North Bridge module specific) | Пост-памятная инициализация северного моста (зависит от модуля) |
| 0x3A | Post-Memory North Bridge initialization (North Bridge module specific) | Пост-памятная инициализация северного моста (зависит от модуля) |
| 0x3B | Post-Memory South Bridge initialization is started | Начата пост-памятная инициализация южного моста |
| 0x3C | Post-Memory South Bridge initialization (South Bridge module specific) | Пост-памятная инициализация южного моста (зависит от модуля) |
| 0x3D | Post-Memory South Bridge initialization (South Bridge module specific) | Пост-памятная инициализация южного моста (зависит от модуля) |
| 0x3E | Post-Memory South Bridge initialization (South Bridge module specific) | Пост-памятная инициализация южного моста (зависит от модуля) |
| 0x3F–0x4E | OEM post memory initialization codes | OEM-коды пост-памятной инициализации |
| 0x4F | DXE IPL is started | Запущен DXE IPL |

#### PEI — Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x50 | Memory initialization error. Invalid memory type or incompatible memory speed | Ошибка инициализации памяти. Неверный тип памяти или несовместимая частота |
| 0x51 | Memory initialization error. SPD reading has failed | Ошибка инициализации памяти. Не удалось прочитать SPD |
| 0x52 | Memory initialization error. Invalid memory size or memory modules do not match. | Ошибка инициализации памяти. Неверный объём или модули памяти не совпадают |
| 0x53 | Memory initialization error. No usable memory detected | Ошибка инициализации памяти. Не обнаружено пригодной памяти |
| 0x54 | Unspecified memory initialization error. | Неуточнённая ошибка инициализации памяти |
| 0x55 | Memory not installed | Память не установлена |
| 0x56 | Invalid CPU type or Speed | Неверный тип CPU или частота |
| 0x57 | CPU mismatch | Несовпадение/несовместимость CPU |
| 0x58 | CPU self test failed or possible CPU cache error | Самотест CPU не пройден или возможна ошибка кэша CPU |
| 0x59 | CPU micro-code is not found or micro-code update is failed | Микрокод CPU не найден или обновление микрокода не удалось |
| 0x5A | Internal CPU error | Внутренняя ошибка CPU |
| 0x5B | reset PPI is not available | Reset PPI недоступен |
| 0x5C–0x5F | Reserved for future AMI error codes | Зарезервировано для будущих ошибок AMI |

---

### S3 Resume (PEI)

#### S3 Resume — Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xE0 | S3 Resume is stared (S3 Resume PPI is called by the DXE IPL) | Начат возврат из S3 (S3 Resume PPI вызван DXE IPL) |
| 0xE1 | S3 Boot Script execution | Выполнение S3 Boot Script |
| 0xE2 | Video repost | Повторная инициализация видео (repost) |
| 0xE3 | OS S3 wake vector call | Вызов вектора пробуждения ОС из S3 |
| 0xE4–0xE7 | Reserved for future AMI progress codes | Зарезервировано для будущих прогресс-кодов AMI |

#### S3 Resume — Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xE8 | S3 Resume Failed | Возврат из S3 не удался |
| 0xE9 | S3 Resume PPI not Found | S3 Resume PPI не найден |
| 0xEA | S3 Resume Boot Script Error | Ошибка S3 Boot Script |
| 0xEB | S3 OS Wake Error | Ошибка пробуждения ОС (S3) |
| 0xEC–0xEF | Reserved for future AMI error codes | Зарезервировано для будущих ошибок AMI |

---

### Recovery (PEI)

#### Recovery — Progress Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xF0 | Recovery condition triggered by firmware (Auto recovery) | Условие восстановления инициировано прошивкой (автовосстановление) |
| 0xF1 | Recovery condition triggered by user (Forced recovery) | Условие восстановления инициировано пользователем (принудительное) |
| 0xF2 | Recovery process started | Процесс восстановления начат |
| 0xF3 | Recovery firmware image is found | Найден образ прошивки для восстановления |
| 0xF4 | Recovery firmware image is loaded | Загружен образ прошивки для восстановления |
| 0xF5–0xF7 | Reserved for future AMI progress codes | Зарезервировано для будущих прогресс-кодов AMI |

#### Recovery — Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xF8 | Recovery PPI is not available | Recovery PPI недоступен |
| 0xF9 | Recovery capsule is not found | Капсула восстановления не найдена |
| 0xFA | Invalid recovery capsule | Некорректная капсула восстановления |
| 0xFB–0xFF | Reserved for future AMI error codes | Зарезервировано для будущих ошибок AMI |

---

### PEI Beep Codes

| Кол-во сигналов | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 1 | Memory not Installed | Память не установлена |
| 1 | Memory was installed twice (InstallPeiMemory routine in PEI Core called twice) | Память установлена «дважды» (InstallPeiMemory вызван дважды в PEI Core) |
| 2 | Recovery started | Восстановление начато |
| 3 | DXEIPL was not found | DXE IPL не найден |
| 3 | DXE Core Firmware Volume was not found | Firmware Volume с DXE Core не найден |
| 4 | Recovery failed | Восстановление не удалось |
| 4 | S3 Resume failed | Возврат из S3 не удался |
| 7 | Reset PPI is not available | Reset PPI недоступен |

---

### DXE Phase / BDS Phase

#### DXE — Progress Codes (0x60+)

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x60 | DXE Core is started | Запущено ядро DXE |
| 0x61 | NVRAM initialization | Инициализация NVRAM |
| 0x62 | Installation of the South Bridge Runtime Services | Установка runtime-служб южного моста |
| 0x63 | CPU DXE initialization is started | Начата DXE-инициализация CPU |
| 0x64 | CPU DXE initialization (CPU module specific) | DXE-инициализация CPU (зависит от CPU-модуля) |
| 0x65 | CPU DXE initialization (CPU module specific) | DXE-инициализация CPU (зависит от CPU-модуля) |
| 0x66 | CPU DXE initialization (CPU module specific) | DXE-инициализация CPU (зависит от CPU-модуля) |
| 0x67 | CPU DXE initialization (CPU module specific) | DXE-инициализация CPU (зависит от CPU-модуля) |
| 0x68 | PCI host bridge initialization | Инициализация PCI host bridge |
| 0x69 | North Bridge DXE initialization is started | Начата DXE-инициализация северного моста |
| 0x6A | North Bridge DXE SMM initialization is started | Начата DXE SMM-инициализация северного моста |
| 0x6B | North Bridge DXE initialization (North Bridge module specific) | DXE-инициализация северного моста (зависит от модуля) |
| 0x6C | North Bridge DXE initialization (North Bridge module specific) | DXE-инициализация северного моста (зависит от модуля) |
| 0x6D | North Bridge DXE initialization (North Bridge module specific) | DXE-инициализация северного моста (зависит от модуля) |
| 0x6E | North Bridge DXE initialization (North Bridge module specific) | DXE-инициализация северного моста (зависит от модуля) |
| 0x6F | North Bridge DXE initialization (North Bridge module specific) | DXE-инициализация северного моста (зависит от модуля) |
| 0x70 | South Bridge DXE initialization is started | Начата DXE-инициализация южного моста |
| 0x71 | South Bridge DXE SMM initialization is started | Начата DXE SMM-инициализация южного моста |
| 0x72 | South Bridge devices initialization | Инициализация устройств южного моста |
| 0x73 | South Bridge DXE Initialization (South Bridge module specific) | DXE-инициализация южного моста (зависит от модуля) |
| 0x74 | South Bridge DXE Initialization (South Bridge module specific) | DXE-инициализация южного моста (зависит от модуля) |
| 0x75 | South Bridge DXE Initialization (South Bridge module specific) | DXE-инициализация южного моста (зависит от модуля) |
| 0x76 | South Bridge DXE Initialization (South Bridge module specific) | DXE-инициализация южного моста (зависит от модуля) |
| 0x77 | South Bridge DXE Initialization (South Bridge module specific) | DXE-инициализация южного моста (зависит от модуля) |
| 0x78 | ACPI module initialization | Инициализация модуля ACPI |
| 0x79 | CSM initialization | Инициализация CSM |
| 0x7A–0x7F | Reserved for future AMI DXE codes | Зарезервировано для будущих DXE-кодов AMI |
| 0x80–0x8F | OEM DXE initialization codes | OEM-коды DXE-инициализации |

#### BDS — Progress Codes (0x90+)

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x90 | Boot Device Selection (BDS) phase is started | Начата фаза BDS (выбор загрузочного устройства) |
| 0x91 | Driver connecting is started | Начато подключение драйверов |
| 0x92 | PCI Bus initialization is started | Начата инициализация PCI-шины |
| 0x93 | PCI Bus Hot Plug Controller Initialization | Инициализация контроллера hot-plug PCI |
| 0x94 | PCI Bus Enumeration | Перечисление устройств PCI (enumeration) |
| 0x95 | PCI Bus Request Resources | Запрос ресурсов для PCI |
| 0x96 | PCI Bus Assign Resources | Назначение ресурсов PCI |
| 0x97 | Console Output devices connect | Подключение устройств вывода консоли |
| 0x98 | Console input devices connect | Подключение устройств ввода консоли |
| 0x99 | Super IO Initialization | Инициализация Super I/O |
| 0x9A | USB initialization is started | Начата инициализация USB |
| 0x9B | USB Reset | Сброс USB |
| 0x9C | USB Detect | Обнаружение USB-устройств |
| 0x9D | USB Enable | Включение USB |
| 0x9E–0x9F | Reserved for future AMI codes | Зарезервировано для будущих кодов AMI |
| 0xA0 | IDE initialization is started | Начата инициализация IDE |
| 0xA1 | IDE Reset | Сброс IDE |
| 0xA2 | IDE Detect | Обнаружение IDE |
| 0xA3 | IDE Enable | Включение IDE |
| 0xA4 | SCSI initialization is started | Начата инициализация SCSI |
| 0xA5 | SCSI Reset | Сброс SCSI |
| 0xA6 | SCSI Detect | Обнаружение SCSI |
| 0xA7 | SCSI Enable | Включение SCSI |
| 0xA8 | Setup Verifying Password | Setup: проверка пароля |
| 0xA9 | Start of Setup | Начало Setup (вход в настройки BIOS) |
| 0xAA | Reserved for ASL (see ASL Status Codes section below) | Зарезервировано для ASL (см. раздел ASL) |
| 0xAB | Setup Input Wait | Setup: ожидание ввода |
| 0xAC | Reserved for ASL (see ASL Status Codes section below) | Зарезервировано для ASL (см. раздел ASL) |
| 0xAD | Ready To Boot event | Событие Ready To Boot |
| 0xAE | Legacy Boot event | Событие Legacy Boot |
| 0xAF | Exit Boot Services event | Событие Exit Boot Services |
| 0xB0 | Runtime Set Virtual Address MAP Begin | Runtime: начало установки карты виртуальных адресов |
| 0xB1 | Runtime Set Virtual Address MAP End | Runtime: завершение установки карты виртуальных адресов |
| 0xB2 | Legacy Option ROM Initialization | Инициализация Legacy Option ROM |
| 0xB3 | System Reset | Системный сброс |
| 0xB4 | USB hot plug | Hot-plug USB |
| 0xB5 | PCI bus hot plug | Hot-plug PCI |
| 0xB6 | Clean-up of NVRAM | Очистка/уборка NVRAM |
| 0xB7 | Configuration Reset (reset of NVRAM settings) | Сброс конфигурации (сброс настроек NVRAM) |
| 0xB8–0xBF | Reserved for future AMI codes | Зарезервировано для будущих кодов AMI |
| 0xC0–0xCF | OEM BDS initialization codes | OEM-коды инициализации BDS |

---

### DXE Error Codes

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0xD0 | CPU initialization error | Ошибка инициализации CPU |
| 0xD1 | North Bridge initialization error | Ошибка инициализации северного моста |
| 0xD2 | South Bridge initialization error | Ошибка инициализации южного моста |
| 0xD3 | Some of the Architectural Protocols are not available | Некоторые архитектурные протоколы недоступны |
| 0xD4 | PCI resource allocation error. Out of Resources | Ошибка распределения ресурсов PCI. Недостаточно ресурсов |
| 0xD5 | No Space for Legacy Option ROM | Нет места для Legacy Option ROM |
| 0xD6 | No Console Output Devices are found | Устройства вывода консоли не найдены |
| 0xD7 | No Console Input Devices are found | Устройства ввода консоли не найдены |
| 0xD8 | Invalid password | Неверный пароль |
| 0xD9 | Error loading Boot Option (LoadImage returned error) | Ошибка загрузки варианта загрузки (LoadImage вернул ошибку) |
| 0xDA | Boot Option is failed (StartImage returned error) | Запуск варианта загрузки не удался (StartImage вернул ошибку) |
| 0xDB | Flash update is failed | Обновление прошивки (flash) не удалось |
| 0xDC | Reset protocol is not available | Протокол сброса (Reset protocol) недоступен |

---

### DXE Beep Codes

| Кол-во сигналов | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 1 | Invalid password | Неверный пароль |
| 4 | Some of the Architectural Protocols are not available | Некоторые архитектурные протоколы недоступны |
| 5 | No Console Output Devices are found | Устройства вывода консоли не найдены |
| 5 | No Console Input Devices are found | Устройства ввода консоли не найдены |
| 6 | Flash update is failed | Обновление прошивки (flash) не удалось |
| 7 | Reset protocol is not available | Протокол сброса недоступен |
| 8 | Platform PCI resource requirements cannot be met | Невозможно удовлетворить требования платформы по PCI-ресурсам |

---

### ACPI/ASL Checkpoints

| Код | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x01 | System is entering S1 sleep state | Система входит в сон S1 |
| 0x02 | System is entering S2 sleep state | Система входит в сон S2 |
| 0x03 | System is entering S3 sleep state | Система входит в сон S3 |
| 0x04 | System is entering S4 sleep state | Система входит в сон S4 |
| 0x05 | System is entering S5 sleep state | Система входит в состояние S5 (выключение) |
| 0x10 | System is waking up from the S1 sleep state | Система выходит из сна S1 |
| 0x20 | System is waking up from the S2 sleep state | Система выходит из сна S2 |
| 0x30 | System is waking up from the S3 sleep state | Система выходит из сна S3 |
| 0x40 | System is waking up from the S4 sleep state | Система выходит из сна S4 |
| 0xAC | System has transitioned into ACPI mode. Interrupt controller is in PIC mode. | Система перешла в режим ACPI. Контроллер прерываний в режиме PIC. |
| 0xAA | System has transitioned into ACPI mode. Interrupt controller is in APIC mode. | Система перешла в режим ACPI. Контроллер прерываний в режиме APIC. |

---

### OEM-Reserved Checkpoint Ranges

| Код/диапазон | Описание (EN) | Перевод (RU) |
|---:|---|---|
| 0x05 | OEM SEC initialization before microcode loading | OEM SEC-инициализация до загрузки микрокода |
| 0x0A | OEM SEC initialization after microcode loading | OEM SEC-инициализация после загрузки микрокода |
| 0x1D–0x2A | OEM pre-memory initialization codes | OEM-коды пред-памятной инициализации |
| 0x3F–0x4E | OEM PEI post memory initialization codes | OEM-коды пост-памятной инициализации PEI |
| 0x80–0x8F | OEM DXE initialization codes | OEM-коды DXE-инициализации |
| 0xC0–0xCF | OEM BDS initialization codes | OEM-коды BDS-инициализации |

# Таблица пост-кодов от Huananzhi и Kllisre

Небольшую подсказку по наиболее часто встречающимся пост-кодам сделали и производители китайских плат Huananzhi и Kllisre. 
Это более наглядный и быстрый способ узнать, что же пошло не так при запуске, однако не стоит доверять данным табличкам на все 100%.

<img width="595" height="842" alt="image" src="https://github.com/user-attachments/assets/7049d5e9-92e8-4e52-9e4a-6f29c6e0e79c" />

<img width="1777" height="464" alt="image" src="https://github.com/user-attachments/assets/67b6b0db-18bd-4633-933c-1fc1a94f2ccb" />

<img width="1079" height="712" alt="image" src="https://github.com/user-attachments/assets/a0e56390-1501-485a-9086-33b942462b90" />
