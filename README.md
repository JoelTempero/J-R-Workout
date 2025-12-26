# J&R Workout Tracker 💪✨

A couples workout tracking app for Joel and Rachel!

## Features

- 🔐 **PIN protected** (4-digit code: 3489)
- 👥 **Dual profiles** - Joel (purple) & Rachel (cyan)
- 📋 **Workout history** - View, edit, and delete past workouts
- 🐕 **Sidon Walk** - Track walks with your dog
- 👟 **Step Count** - Daily step tracking
- 💪 **Upper Body** - Pushups, Tricep Dips, Lat Pulldowns, etc.
- 🦵 **Lower Body** - Squats, Lunges, Deadlifts, etc.
- 🎯 **Core** - Planks, V-Sits, Mountain Climbers, etc.
- ⚡ **Custom Workout** - Mix and match any exercises
- ⚖️ **Body Weight** - Track weight progress
- 📅 **Calendar view** - Half-circle indicators for each workout type
- 📊 **Charts** - Track progress over time (weight, reps, sets, steps, etc.)
- 🏆 **Rewards** - Earn badges every 25 workouts and every kg gained
- ⚙️ **Base Settings** - Customize default values for each exercise
- 📱 **PWA** - Install on your phone's home screen

## Setup

### 1. Create your GitHub repo

Create a new repository called `J-R-Workout` on GitHub.

### 2. Upload these files

Upload all files from this folder to your repo:
- `index.html`
- `manifest.json`
- `data/workouts.json`
- `icon-192.png` (create or find a simple icon)
- `icon-512.png`

### 3. Enable GitHub Pages

1. Go to your repo → Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` (or `master`), folder: `/ (root)`
4. Save

Your site will be live at: `https://YOUR-USERNAME.github.io/J-R-Workout/`

### 4. Create a Personal Access Token (PAT)

1. GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens
2. Generate new token
3. Name: "Workout Tracker"
4. Repository access: Only select repositories → `J-R-Workout`
5. Permissions → Repository permissions → Contents: Read and write
6. Generate token
7. Copy the token (starts with `github_pat_`)

### 5. Configure the app

1. Open your app URL
2. Enter PIN: `3489`
3. Select your profile
4. Tap ⚙️ Settings
5. Paste your PAT
6. Save

### 6. Install on your phone

**iPhone:**
1. Open the URL in Safari
2. Tap Share → Add to Home Screen

**Android:**
1. Open in Chrome
2. Tap menu → Add to Home Screen

## Changing the PIN

Edit `index.html` and change this line:
```javascript
const CONFIG = {
    PIN: '3489',  // ← Change this
```

## Data Structure

All data is stored in `data/workouts.json`:

```json
{
  "workouts": [
    {
      "profile": "joel",
      "date": "2025-01-15",
      "time": "08:30",
      "types": ["upper", "core"],
      "timestamp": "2025-01-15T08:30:00.000Z"
    }
  ],
  "weights": {
    "joel": [
      {
        "date": "2025-01-15",
        "body": 75.5,
        "dumbbell": 12,
        "timestamp": "2025-01-15T08:30:00.000Z"
      }
    ],
    "rachel": []
  }
}
```

---

Built with 💜💙 for Joel & Rachel
