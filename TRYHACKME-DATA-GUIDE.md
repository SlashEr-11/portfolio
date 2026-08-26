# TryHackMe Portfolio Integration

## How to Update Your Real TryHackMe Data

Your portfolio now uses **real data** from the `tryhackme-data.json` file. Here's how to keep it updated:

### 🎯 What's Real-Time:

1. **TryHackMe Badge** - Shows your current rank automatically (updates when TryHackMe updates it)
   - URL: `https://tryhackme-badges.s3.amazonaws.com/YourUsername.png`
   - Replace `YourUsername` with your actual TryHackMe username in `modern.html`

### 📊 What You Need to Update Manually:

All stats are stored in `tryhackme-data.json` - Update this file with your real data:

#### Step 1: Update Your Stats

Go to your TryHackMe profile: `https://tryhackme.com/p/YourUsername`

Copy your current stats to `tryhackme-data.json`:

```json
{
  "username": "YourActualUsername",
  "lastUpdated": "2026-08-26",
  "stats": {
    "rank": "Top 2%",           // Your global rank percentage
    "globalRanking": 15234,     // Your exact rank number
    "roomsCompleted": 523,      // Total rooms completed
    "badgesEarned": 67,         // Total badges earned
    "currentStreak": 45,        // Current streak in days
    "longestStreak": 120        // Your longest streak
  },
  "activity": {
    // Your daily activity (see Step 2)
  }
}
```

#### Step 2: Update Your Daily Activity

Add your daily room completions in the format `"YYYY-MM-DD": number_of_rooms`:

```json
"activity": {
  "2026-08-26": 3,  // Completed 3 rooms on Aug 26
  "2026-08-25": 5,  // Completed 5 rooms on Aug 25
  "2026-08-24": 2,  // Completed 2 rooms on Aug 24
  // ... add more dates
}
```

**How to get your activity data:**
1. Go to your TryHackMe profile
2. Check your activity calendar/history
3. Note which days you completed rooms and how many
4. Add them to the JSON file

### 🔄 Update Schedule Recommendations:

- **Stats (rank, rooms, badges)**: Update weekly or monthly
- **Activity data**: Add entries when you complete rooms (or weekly batch update)
- **lastUpdated field**: Change to today's date when you update

### 🤖 Automation Options (Advanced):

If you want more automated updates, you can:

1. **GitHub Actions** (Recommended)
   - Create a script that scrapes your TryHackMe profile
   - Run it daily via GitHub Actions
   - Auto-commit updates to `tryhackme-data.json`

2. **Local Script**
   - Write a Python/Node.js script to scrape your profile
   - Run it manually when needed
   - Updates the JSON file

3. **Browser Extension**
   - Create a simple extension that exports your TryHackMe data
   - Generates the JSON format automatically

### 📝 Example: Full JSON File

```json
{
  "username": "john_doe",
  "lastUpdated": "2026-08-26",
  "stats": {
    "rank": "Top 1%",
    "globalRanking": 5432,
    "roomsCompleted": 687,
    "badgesEarned": 89,
    "currentStreak": 67,
    "longestStreak": 145
  },
  "activity": {
    "2026-01-01": 4,
    "2026-01-02": 3,
    "2026-01-05": 5,
    "2026-01-10": 2,
    "2026-02-01": 6,
    "2026-02-15": 4,
    "2026-03-10": 3,
    "2026-04-05": 5,
    "2026-05-12": 4,
    "2026-06-20": 3,
    "2026-07-15": 6,
    "2026-08-26": 2
  }
}
```

### ⚠️ Important Notes:

1. **Privacy**: Only include data you're comfortable sharing publicly
2. **Accuracy**: Keep your stats accurate for credibility
3. **Consistency**: Update regularly to show active learning
4. **Backup**: Keep a backup of your data file

### 🚀 Quick Setup:

1. Open `modern.html` and replace `YourUsername` with your actual TryHackMe username (2 places)
2. Open `tryhackme-data.json` and update with your real stats
3. Save both files
4. Open `modern.html` in your browser to see your real data!

### 🔗 Files to Update:

- `modern.html` - Line 679 & 847: Replace `YourUsername`
- `tryhackme-data.json` - Add your real stats and activity

---

**Note**: This is the closest you can get to "real-time" data without:
- TryHackMe providing a public API
- Running a backend server
- Violating TryHackMe's terms of service

The TryHackMe badge is the only truly "live" element that updates automatically!
