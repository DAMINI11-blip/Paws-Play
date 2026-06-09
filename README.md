# 🐾 Paws & Play

A **Virtual pet game** built with pure HTML, CSS, and JavaScript — no frameworks, no backend. Adopt a digital companion, keep it happy, and watch it come alive with expressive animations and real-time reactions.

---

## ✨ Features

### 🎨 Expressive Canvas Pets
Each pet is hand-drawn on an HTML5 Canvas with species-specific detail:
- **Cat** — pointy ears, rosy cheeks, white whiskers
- **Dog** — floppy droopy ears, warm brown tones
- **Parrot** — colorful feather crest, yellow beak
- **Lion** — spiky orange mane with radial gradient texture

### 😊 Live Blinking Eyes
The pet blinks naturally at random intervals using a smooth 60fps draw loop — making it feel genuinely alive between interactions.

### 😤 5 Dynamic Moods
Mood changes automatically based on the pet's stats:

| Mood | Trigger | Face | Animation |
|------|---------|------|-----------|
| Happy | All stats healthy | Grin + teeth + tongue | Idle bounce |
| Hungry | Hunger < 30 | Big round pleading eyes + open mouth | Angry shake |
| Sleepy | Energy < 30 | Heavy drooping eyelids + ZZZ | Slow sway |
| Sick | Health < 35 | ✕ swirly eyes + green spirals | Slow sway |
| Angry | Happiness < 30 | Furrowed brows + grimace + anger vein | Shake |

### 🎮 Interactions
- **Click** → pet reacts with a random species catchphrase, happiness increases, floating heart/star particles appear
- **Double-click** → triggers a special spin flip animation, earns bonus coins
- **Feed** → restores hunger (+28), small energy boost
- **Play** → boosts happiness (+28), costs energy (-15)
- **Sleep** → restores energy (+42)
- **Heal** → restores health (+32)

### ⏱️ Real-time Decay (every 5 seconds)
- Hunger: −7
- Happiness: −5
- Energy: −6
- Health degrades if multiple stats are critically low; regenerates passively when well-fed and rested

### 🪙 Progression System (ready for expansion)
- **Coins** — earned via double-click tricks
- **XP + Levels** — gained by petting; level up at `level × 60 XP`

---

## 🚀 Getting Started

No installation needed. It's a single HTML file.

```bash
# Clone or download
git clone https://github.com/DAMINI11-blip/virtual-pet-world.git

# Open in browser
open virtual-pet-world.html
```

Or just drag `virtual-pet-world.html` into any browser window.

---

## 🗂️ Project Structure

```
virtual-pet-world.html
│
├── <style>          — All CSS (tokens, layout, animations, responsive)
│
└── <script>
    ├── State         — Single pet state object
    ├── Storage       — localStorage save/load
    ├── Tick Engine   — 5s decay loop
    ├── Mood Engine   — Priority-based mood calculator
    ├── Draw Engine   — 60fps canvas renderer + blink system
    ├── Animation     — CSS class-based animation controller
    ├── Interactions  — Click, double-click, action buttons
    ├── Particles     — Floating emoji particle system
    └── Audio         — Web Audio API synthesizer (per-species pitch)

```

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, keyframe animations) |
| Logic | Vanilla JavaScript (ES6+) |
| Drawing | HTML5 Canvas 2D API |
| Audio | Web Audio API (oscillator synthesis) |
| Storage | localStorage |

---

## 📸 Preview

> Setup screen → choose pet type + enter name → full game dashboard with live animated pet, stat bars, mood strip, and action buttons.

---

## 👩‍💻 Author

**Damini** — [@DAMINI11-blip](https://github.com/DAMINI11-blip)

Built as a frontend portfolio project exploring canvas animation, game loop architecture, and interactive UI design.

---

## 📄 License

MIT — free to use, modify, and share.
