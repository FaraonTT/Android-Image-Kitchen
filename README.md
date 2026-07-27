# 🍳 Android-Image-Kitchen

> **Automated scripts to unpack/repack Android kernel/recovery images + ramdisks**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![GitHub Issues](https://img.shields.io/github/issues/FaraonTT/Android-Image-Kitchen.svg)](https://github.com/FaraonTT/Android-Image-Kitchen/issues)
[![GitHub Stars](https://img.shields.io/github/stars/FaraonTT/Android-Image-Kitchen.svg)](https://github.com/FaraonTT/Android-Image-Kitchen/stargazers)

---

## 📋 Описание

**Android-Image-Kitchen** — это набор мощных автоматизированных скриптов для работы с образами Android устройств. Инструмент позволяет легко распаковывать, модифицировать и переупаковывать kernel, recovery и другие образы Android.

> **Это форк оригинального репозитория [osm0sis/Android-Image-Kitchen](https://github.com/osm0sis/Android-Image-Kitchen)**

### ✨ Основные возможности

- 🔓 **Распаковка образов** — легко извлекайте содержимое из kernel и recovery образов
- 📦 **Переупаковка образов** — переупаковывайте модифицированные образы обратно
- 🗂️ **Работа с Ramdisk** — полная поддержка распаковки/переупаковки ramdisk
- ⚡ **Автоматизация** — все процессы полностью автоматизированы
- 🛠️ **Простота использования** — интуитивные batch-скрипты для Windows
- 🔧 **Гибкость** — легко расширяемая архитектура

---

## 🚀 Быстрый старт

### Требования

- **Windows 7+** или другая ОС с поддержкой batch-файлов
- **Образ Android устройства** (kernel, recovery, boot.img, etc.)
- Базовое понимание структуры Android образов

### Использование

1. **Клонируйте репозиторий:**
   ```batch
   git clone https://github.com/FaraonTT/Android-Image-Kitchen.git
   cd Android-Image-Kitchen
   ```

2. **Поместите ваш образ:**
   - Скопируйте Android образ в директорию проекта или укажите путь к нему

3. **Запустите скрипт распаковки:**
   ```batch
   unpack.bat <путь_к_образу>
   ```

4. **Внесите изменения** (при необходимости):
   - Отредактируйте необходимые файлы в распакованной директории

5. **Переупакуйте образ:**
   ```batch
   repack.bat
   ```

6. **Готово!** ✅
   - Переупакованный образ находится в выходной директории

---

## 📁 Структура проекта

```
Android-Image-Kitchen/
├── unpack.bat              # Скрипт для распаковки образов
├── repack.bat              # Скрипт для переупаковки образов
├── tools/                  # Служебные утилиты
│   ├── mkbootimg/
│   ├── unbootimg/
│   └── ...
├── workspace/              # Рабочая директория
│   ├── extracted/          # Распакованные образы
│   └── ...
├── LICENSE                 # MIT License
└── README.md              # Документация
```

---

## 💡 Примеры использования

### Распаковка boot.img

```batch
unpack.bat D:\images\boot.img
```

### Распаковка recovery.img

```batch
unpack.bat D:\images\recovery.img
```

### Модификация и переупаковка

```batch
REM 1. Распаковать
unpack.bat device_boot.img

REM 2. Отредактировать файлы в workspace/extracted/

REM 3. Переупаковать
repack.bat
```

---

## 🔧 Технические детали

### Поддерживаемые форматы

- ✅ **boot.img** — загрузочный образ
- ✅ **recovery.img** — recovery раздел
- ✅ **kernel** — ядро Android
- ✅ **ramdisk** — корневая файловая система

### Внутренние утилиты

Проект использует следующие инструменты:
- `mkbootimg` — создание boot-образов
- `unbootimg` — распаковка boot-образов
- Специализированные утилиты для работы с ramdisk

---

## 📚 Документация

Для подробной информации о работе с каждым скриптом обратитесь к встроенной справке:

```batch
unpack.bat --help
repack.bat --help
```

---

## ⚠️ Важно

- **Резервная копия:** Всегда сохраняйте оригинальные образы перед модификацией
- **Совместимость:** Убедитесь, что вашу модификацию поддерживает целевое устройство
- **Тестирование:** Тщательно тестируйте переупакованные образы перед использованием на реальном устройстве
- **Ответственность:** Вы несете полную ответственность за использование этих инструментов

---

## 🤝 Вклад в проект

Контрибьюции приветствуются! Если у вас есть улучшения или исправления:

1. Fork репозитория
2. Создайте ветку для вашей функции (`git checkout -b feature/amazing-feature`)
3. Совершите ваши изменения (`git commit -m 'Add some amazing feature'`)
4. Push ветки (`git push origin feature/amazing-feature`)
5. Откройте Pull Request

---

## 📝 Лицензия

Этот проект лицензирован под [MIT License](LICENSE) — см. файл `LICENSE` для деталей.

Включает код и утилиты от:
- **osm0sis** и команды разработчиков
- Оригинальный проект: [osm0sis/Android-Image-Kitchen](https://github.com/osm0sis/Android-Image-Kitchen)

Полный список авторов и источников смотрите в файле [LICENSE](LICENSE).

---

## 👤 Авторы

### Форк
**FaraonTT** — текущий мейнтейнер форка

- 🔗 GitHub: [@FaraonTT](https://github.com/FaraonTT)
- 📧 Свяжитесь через Issues в репозитории

### Оригинальный проект
**osm0sis** и контрибьюторы сообщества XDA Developers

---

## 🙏 Благодарности

Спасибо:
- **osm0sis** за оригинальный проект
- Всем контрибьюторам и авторам инструментов, упомянутым в [LICENSE](LICENSE)
- Сообществу XDA Developers за знания и методы
- Всем, кто использует этот инструмент и помогает его улучшать!

---

## ❓ Часто задаваемые вопросы

**Q: Будет ли мой образ повреждён?**  
A: Инструмент работает с копией. Оригинальный образ остаётся в безопасности.

**Q: Какие версии Android поддерживаются?**  
A: Инструмент совместим с большинством версий Android благодаря работе на уровне образов.

**Q: Могу ли я использовать это для своего устройства?**  
A: Да, если образ в совместимом формате (boot.img, recovery.img и т.д.).

**Q: Что это за форк?**  
A: Это независимый форк оригинального проекта osm0sis. Полная история авторства сохранена в LICENSE.

---

## 🔗 Полезные ссылки

- [Оригинальный проект](https://github.com/osm0sis/Android-Image-Kitchen)
- [Android Boot Image Format](https://source.android.com/)
- [Android Development](https://developer.android.com/)
- [Kernel Source](https://android.googlesource.com/)
- [XDA Developers Forum](https://xdaforums.com/t/tool-android-image-kitchen-unpack-repack-kernel-ramdisk-win-android-linux-mac.2073775/)

---

<div align="center">

**Сделано с ❤️ для Android сообщества**

[⭐ Star on GitHub](https://github.com/FaraonTT/Android-Image-Kitchen) • [🐛 Report Issue](https://github.com/FaraonTT/Android-Image-Kitchen/issues) • [💬 Discussions](https://github.com/FaraonTT/Android-Image-Kitchen/discussions)

</div>
