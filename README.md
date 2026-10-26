# 📱 VS Code Mobile

WebView-обёртка вокруг [vscode.dev](https://vscode.dev) — официальная веб-версия VS Code от Microsoft, адаптированная для Android.

## ✨ Возможности

- 📱 Полноценный VS Code на телефоне
- 🔗 Открытие репозиториев с GitHub
- 📂 Работа с файлами через файловую систему
- 🎨 Поддержка тем и расширений
- 📴 Полноэкранный режим
- 🔄 Автоматическая сборка APK через GitHub Actions

## 📥 Скачать APK

APK автоматически собирается при каждом обновлении кода:

1. Перейди в **Actions** → выбери последний workflow run
2. Скачай артефакт **app-debug** (внизу страницы)
3. Установи APK на телефон

## 🛠 Сборка локально

```bash
# Клонируй репозиторий
git clone https://github.com/aartem2409a-pixel/vscode-mobile.git
cd vscode-mobile

# Собери debug APK
./gradlew assembleDebug

# APK будет в: app/build/outputs/apk/debug/app-debug.apk
```

## 🏗 Автоматическая сборка (GitHub Actions)

При каждом push в `main` автоматически:
1. Устанавливается JDK 17
2. Запускается сборка Gradle
3. APK загружается как артефакт

## 📖 Как это работает

Приложение использует Android WebView для отображения vscode.dev с оптимизацией под мобильные устройства:
- Полноэкранный режим без адресной строки
- Поддержка JavaScript и DOM Storage
- Кэширование для быстрой загрузки
- Обработка навигации внутри WebView

## 📄 Лицензия

MIT

## 👨‍💻 Автор

Создано с помощью Mira AI
