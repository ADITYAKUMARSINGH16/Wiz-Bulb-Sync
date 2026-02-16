# WiZ Bulb Sync - Ambient Light Control

This application synchronizes your computer screen's colors with your WiZ smart bulb in real-time, creating an immersive ambient lighting experience for movies, games, and videos.

## Features
-   **Real-Time Sync**: Updates your bulb 10 times per second to match on-screen action.
-   **Smart Color Match**: Uses "Dominant" color logic to ignore boring gray/black backgrounds and find the *real* color.
-   **Silky Smooth Mode**: Advanced smoothing to prevent flickering and stuttering.
-   **Vibrant Mode**: Optional toggle to boost saturation for a "neon" look.
-   **Area Selection**: Sync to a specific part of your screen (e.g., just the minimap or health bar).
-   **Brightness Control**: Master slider to dim the effect without changing your monitor brightness.

---

## Setup

### 1. Prerequisites
-   **Python 3.10+** installed on your system.
-   A **WiZ Smart Bulb** connected to the same Wi-Fi network as your PC.
-   To find your Bulb's IP:
    1.  Open the **WiZ App** on your phone.
    2.  Tap on the bulb -> **Settings**.
    3.  Scroll down to see the **IP Address** (e.g., `192.168.1.15`).

### 2. Installation
1.  Open a terminal in this folder.
2.  Install the required libraries:
    ```bash
    pip install -r requirement.txt
    ```
    *(Note: If you are using the included `run.bat`, it may handle the virtual environment for you).*

---

## How to Run

Simply double-click **`run.bat`** or **'.\run.bat'** to start the application.

Or, run via command line:
```bash
python main.py
```

---

## Usage Guide

1.  **Bulb IP**: Enter the IP address of your bulb (from the WiZ app).
2.  **Color Logic**:
    -   **Dominant (Recommended)**: Finds the most frequent "colorful" pixel. great for games and movies with dark backgrounds.
    -   **Average**: Mixes all colors together. Good for soft, uniform lighting.
3.  **Silky Smooth Mode**:
    -   **ON**: Colors fade gently into each other. Best for movies.
    -   **OFF**: Instant updates. Best for fast-paced competitive games.
4.  **Vibrant Colors**:
    -   **ON**: Boosts saturation (Red becomes *Red*).
    -   **OFF**: Accurate colors (Red might look like clay/brown depending on the screen).
5.  **Master Brightness**: Controls the maximum brightness of the bulb.
6.  **Select Screen Area**:
    -   Click the button.
    -   Drag a box over the part of the screen you want to capture.
    -   Only that area will be used to control the light.
    -   Click "Reset" to go back to full screen.

## Troubleshooting

-   **"Light isn't changing"**:
    -   Check if the **IP Address** is correct.
    -   Make sure your PC and Bulb are on the **same Wi-Fi**.
    -   Check if "Allow Local Communication" is enabled in the WiZ App settings (under Integration).

-   **"Light is stuttering / lagging"**:
    -   Turn **ON** "Silky Smooth Mode".
    -   Ensure your Wi-Fi signal is strong near the bulb.

-   **"Colors don't match"**:
    -   Try switching between **Dominant** and **Average** mode.
    -   Toggle **Vibrant Mode** on or off to see which you prefer.
