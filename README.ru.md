<h1 align="center">🎣 Terraria Auto Fishing</h1>
<div align="center">

[English](./README.md) | Русский

Автоматический бот для рыбалки в **Terraria** на базе YOLOv11. Определяет поплавок на экране, отслеживает его движение и автоматически подсекает — можно AFK-фармить рыбу весь день.

[![GitHub License](https://img.shields.io/github/license/Decursusss/Terraria-Auto-Fishing?style=for-the-badge&labelColor=1c1917&color=7dc4e4&logo=data:image/svg%2bxml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48IS0tIFVwbG9hZGVkIHRvOiBTVkcgUmVwbywgd3d3LnN2Z3JlcG8uY29tLCBHZW5lcmF0b3I6IFNWRyBSZXBvIE1peGVyIFRvb2xzIC0tPg0KPHN2ZyB3aWR0aD0iODAwcHgiIGhlaWdodD0iODAwcHgiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4NCjxwYXRoIGQ9Ik0xOSAzSDlWM0M3LjExNDM4IDMgNi4xNzE1NyAzIDUuNTg1NzkgMy41ODU3OUM1IDQuMTcxNTcgNSA1LjExNDM4IDUgN1YxMC41VjE3IiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+DQo8cGF0aCBkPSJNMTQgMTdWMTlDMTQgMjAuMTA0NiAxNC44OTU0IDIxIDE2IDIxVjIxQzE3LjEwNDYgMjEgMTggMjAuMTA0NiAxOCAxOVY5VjQuNUMxOCAzLjY3MTU3IDE4LjY3MTYgMyAxOS41IDNWM0MyMC4zMjg0IDMgMjEgMy42NzE1NyAyMSA0LjVWNC41QzIxIDUuMzI4NDMgMjAuMzI4NCA2IDE5LjUgNkgxOC41IiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+DQo8cGF0aCBkPSJNMTYgMjFINUMzLjg5NTQzIDIxIDMgMjAuMTA0NiAzIDE5VjE5QzMgMTcuODk1NCAzLjg5NTQzIDE3IDUgMTdIMTQiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4NCjxwYXRoIGQ9Ik01IDdIMTQiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4NCjxwYXRoIGQ9Ik05IDExSDE0IiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+DQo8L3N2Zz4=)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/Decursusss/Terraria-Auto-Fishing?style=for-the-badge&labelColor=1c1917&color=f59e0b&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSIjZjU5ZTBiIiBzdHJva2U9Im5vbmUiPjxwb2x5Z29uIHBvaW50cz0iMTIgMiAxNS4wOSA4LjI2IDIyIDkuMjcgMTcgMTQuMTQgMTguMTggMjEuMDIgMTIgMTcuNzcgNS44MiAyMS4wMiA3IDE0LjE0IDIgOS4yNyA4LjkxIDguMjYgMTIgMiIvPjwvc3ZnPg==)](https://github.com/Decursusss/Terraria-Auto-Fishing/stargazers)
[![YOLO](https://img.shields.io/badge/YOLOv11-ultralytics-00FFFF?style=for-the-badge&labelColor=1c1917&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSIjMDBGRkZGIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIvPjwvc3ZnPg==)](https://docs.ultralytics.com/)

</div>

## ✨ Как это работает

1. 📸 **Захват экрана** — захватывает окно Terraria в реальном времени через `mss`
2. 🤖 **Детекция YOLO** — кастомная модель YOLOv11 определяет поплавок на каждом кадре
3. 📊 **Отслеживание движения** — сравнивает позицию поплавка между кадрами для обнаружения клёва
4. 🖱️ **Авто-клик** — имитирует клик левой кнопкой для подсечки при обнаружении движения, затем перезабрасывает

## 🧠 Модель YOLO

Модель обучена распознавать **2 класса**:

| Класс        | Описание                                        |
| :----------- | :---------------------------------------------- |
| `bobber`     | Поплавок (рыбацкий) в воде                      |
| `bobberHead` | Верхняя часть поплавка для точного отслеживания |

Датасет включает размеченные скриншоты из Terraria.

## 🚀 Быстрый старт

### Требования

- **Windows** (используется Win32 API для захвата окна и управления мышью)
- **Python 3.10+**
- **Terraria** в оконном режиме

### Установка

```bash
# Клонировать репозиторий
git clone https://github.com/Decursusss/Terraria-Auto-Fishing.git
cd Terraria-Auto-Fishing

# Создать виртуальное окружение
python -m venv .venv
.venv\Scripts\activate

# Установить зависимости
pip install -r requirements.txt
```

### Использование

```bash
python main.py
```

| Горячая клавиша | Действие                            |
| :-------------- | :---------------------------------- |
| `F1`            | Переключить авто-рыбалку ВКЛ / ВЫКЛ |
| `Q`             | Выход (закрыть окно превью)         |

> **Примечание:** Убедитесь, что Terraria запущена в **оконном режиме** перед запуском бота. Скрипт автоматически найдёт и активирует окно Terraria.

## 🛠️ Обучение своей модели

Если хотите переучить YOLO модель на своих скриншотах:

1. Добавьте размеченные изображения в `DataSet/train/images` и `DataSet/train/labels`
2. Отредактируйте `data.yaml`, если меняете классы
3. Запустите скрипт обучения:

```bash
python learn.py
```

Обучение использует `yolo11n.pt` как базовую модель и тренируется 150 эпох.

## 🤝 Контрибьюция

Вклады приветствуются! Вы можете:

1. Сделать Fork репозитория
2. Создать ветку для новой функции (`git checkout -b feature/amazing-feature`)
3. Закоммитить изменения (`git commit -m 'Add amazing feature'`)
4. Запушить в ветку (`git push origin feature/amazing-feature`)
5. Открыть Pull Request

## ©️ Лицензия

MIT License — смотрите [LICENSE](./LICENSE) для подробностей.

<div align="center">

---

Создано [Decursusss](https://github.com/Decursusss) с ❤️

<b>⭐ Поставь звезду моему проекту!</b> <br>
![star](https://github.com/user-attachments/assets/cc66e612-3b0f-4232-9467-e246d2d30f90)<br>

</div>
