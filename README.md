<h1 align="center">🎣 Terraria Auto Fishing</h1>
<div align="center">

English | [Русский](./README.ru.md)

Automated fishing bot for **Terraria** powered by YOLOv11 object detection. Detects the bobber on screen, tracks its motion, and reels in automatically — so you can AFK fish all day.

[![GitHub License](https://img.shields.io/github/license/Decursusss/Terraria-Auto-Fishing?style=for-the-badge&labelColor=1c1917&color=7dc4e4&logo=data:image/svg%2bxml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48IS0tIFVwbG9hZGVkIHRvOiBTVkcgUmVwbywgd3d3LnN2Z3JlcG8uY29tLCBHZW5lcmF0b3I6IFNWRyBSZXBvIE1peGVyIFRvb2xzIC0tPg0KPHN2ZyB3aWR0aD0iODAwcHgiIGhlaWdodD0iODAwcHgiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4NCjxwYXRoIGQ9Ik0xOSAzSDlWM0M3LjExNDM4IDMgNi4xNzE1NyAzIDUuNTg1NzkgMy41ODU3OUM1IDQuMTcxNTcgNSA1LjExNDM4IDUgN1YxMC41VjE3IiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+DQo8cGF0aCBkPSJNMTQgMTdWMTlDMTQgMjAuMTA0NiAxNC44OTU0IDIxIDE2IDIxVjIxQzE3LjEwNDYgMjEgMTggMjAuMTA0NiAxOCAxOVY5VjQuNUMxOCAzLjY3MTU3IDE4LjY3MTYgMyAxOS41IDNWM0MyMC4zMjg0IDMgMjEgMy42NzE1NyAyMSA0LjVWNC41QzIxIDUuMzI4NDMgMjAuMzI4NCA2IDE5LjUgNkgxOC41IiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+DQo8cGF0aCBkPSJNMTYgMjFINUMzLjg5NTQzIDIxIDMgMjAuMTA0NiAzIDE5VjE5QzMgMTcuODk1NCAzLjg5NTQzIDE3IDUgMTdIMTQiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4NCjxwYXRoIGQ9Ik01IDdIMTQiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4NCjxwYXRoIGQ9Ik05IDExSDE0IiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+DQo8L3N2Zz4=)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/Decursusss/Terraria-Auto-Fishing?style=for-the-badge&labelColor=1c1917&color=f59e0b&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSIjZjU5ZTBiIiBzdHJva2U9Im5vbmUiPjxwb2x5Z29uIHBvaW50cz0iMTIgMiAxNS4wOSA4LjI2IDIyIDkuMjcgMTcgMTQuMTQgMTguMTggMjEuMDIgMTIgMTcuNzcgNS44MiAyMS4wMiA3IDE0LjE0IDIgOS4yNyA4LjkxIDguMjYgMTIgMiIvPjwvc3ZnPg==)](https://github.com/Decursusss/Terraria-Auto-Fishing/stargazers)
[![YOLO](https://img.shields.io/badge/YOLOv11-ultralytics-00FFFF?style=for-the-badge&labelColor=1c1917&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSIjMDBGRkZGIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIvPjwvc3ZnPg==)](https://docs.ultralytics.com/)

</div>

## ✨ How It Works

1. 📸 **Screen Capture** — captures the Terraria window in real time using `mss`
2. 🤖 **YOLO Detection** — a custom-trained YOLOv11 model detects the bobber on every frame
3. 📊 **Motion Tracking** — compares bobber position between frames to detect fish bites
4. 🖱️ **Auto Click** — simulates a left click to reel in when motion is detected, then re-casts

## 🧠 YOLO Model

The model is trained to detect **2 classes**:

| Class        | Description                                     |
| :----------- | :---------------------------------------------- |
| `bobber`     | The fishing bobber (float) in the water         |
| `bobberHead` | The top part of the bobber for precise tracking |

The dataset includes labeled screenshots from Terraria captured with [Roboflow](https://roboflow.com/) / manual annotation.

## 🚀 Quick Start

### Prerequisites

- **Windows** (uses Win32 API for window capture & mouse control)
- **Python 3.10+**
- **Terraria** running in windowed mode

### Installation

```bash
# Clone the repo
git clone https://github.com/Decursusss/Terraria-Auto-Fishing.git
cd Terraria-Auto-Fishing

# Create virtual environment
python -m venv .venv
.venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Usage

```bash
python main.py
```

| Hotkey | Action                               |
| :----- | :----------------------------------- |
| `F1`   | Toggle auto-fishing ON / OFF         |
| `Q`    | Quit (close the live preview window) |

> **Note:** Make sure Terraria is running in **windowed mode** before starting the bot. The script will automatically find and focus the Terraria window.

## 🛠️ Training Your Own Model

If you want to retrain the YOLO model with your own screenshots:

1. Add labeled images to `DataSet/train/images` and `DataSet/train/labels`
2. Edit `data.yaml` if you change the class definitions
3. Run the training script:

```bash
python learn.py
```

The training uses `yolo11n.pt` as the base model and trains for 150 epochs.

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## ©️ License

MIT License — see [LICENSE](./LICENSE) for details.

<div align="center">

---

Created by [Decursusss](https://github.com/Decursusss) with ❤️

<b>⭐ Add a star to my project!</b> <br>
![star](https://github.com/user-attachments/assets/cc66e612-3b0f-4232-9467-e246d2d30f90)<br>

</div>
