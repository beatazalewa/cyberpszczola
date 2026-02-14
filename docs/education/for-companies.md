# 💼 Dla Firm / For Companies

> 🌍 **Language / Język:** [🇵🇱 Polski](#-wersja-polska) | [🇬🇧 English](#-english-version)

---

## 🇵🇱 Wersja Polska

[To be added]

---

## 🇬🇧 English Version

[To be added]

import random import time import os # Prosty „szerszeń” jako tekst HORNET = r"><(((°>" # Rozmiar „pola” WIDTH = 80 HEIGHT = 24 NUM_HORNETS = 100 def clear(): os.system("cls" if os.name == "nt" else "clear") def random_position(): x = random.randint(0, WIDTH - len(HORNET)) y = random.randint(0, HEIGHT - 1) return x, y def draw_swarm(): # pusta „plansza” screen = [[" " for _ in range(WIDTH)] for _ in range(HEIGHT)] for _ in range(NUM_HORNETS): x, y = random_position() for i, ch in enumerate(HORNET): if 0 <= x + i < WIDTH: screen[y][x + i] = ch # wypisz całą planszę for row in screen: print("".join(row)) if __name__ == "__main__": while True: clear() draw_swarm() time.sleep(0.2)