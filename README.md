# ⏰ Clockify Time Tracker

A simple, elegant web application to automatically schedule and upload your work hours to Clockify. Perfect for organizing your daily tasks, meetings, and tracking your 8-hour workday.

![Clockify Time Tracker](https://img.shields.io/badge/Clockify-API-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 📸 Screenshot

![App Preview](screenshot.png)

## ✨ Features

- **🔒 Secure Configuration**: Your API key is stored securely in your browser's localStorage
- **📅 Smart Scheduling**: Automatically distributes tasks around your meetings
- **🕐 Meeting Management**: Configure recurring meetings with customizable times and durations
- **📊 Hour Tracking**: Real-time counter showing total hours (with 8-hour goal indicator)
- **💾 Auto-Save Cache**: Remembers your meetings and tasks for future use
- **🔄 Auto-Complete**: Suggests previously used meeting and task names
- **🌍 Bilingual**: Full support for English and Spanish
- **🍽️ Lunch Break**: Automatically includes a 1-hour lunch break at 1:00 PM
- **✅ Validation**: Warns you if your hours don't add up to 8 hours

## 🚀 Quick Start

### Option 1: Direct Use (Recommended)
1. Download the `index.html` file
2. Open it directly in your web browser (Chrome, Firefox, Safari, Edge)
3. That's it! No installation or server required

## 🔑 Configuration

### First Time Setup

1. **Open the application** - A configuration modal will appear
2. **Get your Clockify API Key**:
   - Go to [Clockify Preferences](https://app.clockify.me/manage-api-keys)
   - Navigate to: `Preferences → Advanced → API`
   - Generate or copy your API key
3. **Paste your API Key** in the configuration modal
4. **(Optional)** Enter your default Project ID
5. Click **Save Configuration**

### Finding Your Project ID

To use a default project:
1. Open your Clockify workspace
2. Go to any project
3. Copy the ID from the URL: `https://app.clockify.me/projects/{PROJECT_ID}`
4. Or leave it blank and select from the dropdown each time

## 📖 How to Use

### 1. Configure Your Day
- **Work Date**: Select the date you want to log hours for
- **Start Time**: When do you start working? (e.g., 09:00)
- **Project**: Select your Clockify project from the dropdown

### 2. Add Scheduled Meetings
- **Meeting Name**: Daily Standup, Team Meeting, etc.
- **Start Time**: When does it start? (HH:MM format)
- **Duration**: How long? (HH:MM format)
- Click **Add Meeting** to add more

### 3. Add Your Tasks
- **Task Description**: What did you work on?
- **Duration**: How long? (HH:MM format)
- Add as many tasks as you need

### 4. Review Total Hours
The app will show you in real-time:
- ✅ Green: Exactly 8 hours
- ⚠️ Yellow: Less than 8 hours (shows missing time)
- ⚠️ Red: More than 8 hours (shows extra time)

### 5. Generate and Upload
Click **Generate Schedule and Upload to Clockify**
- The app will:
  - Validate your total hours
  - Show you the complete schedule
  - Automatically upload all entries to Clockify

## ⌨️ Time Format

All duration and time fields use **HH:MM** format:
- `00:15` = 15 minutes
- `01:30` = 1 hour 30 minutes
- `07:45` = 7 hours 45 minutes

**Pro Tip**: You can also type just numbers (e.g., `435` minutes) and it will auto-convert to `07:15`

## 🎯 How It Works

1. **Sorts your meetings** by time (earliest to latest)
2. **Adds fixed lunch break** at 1:00 PM (1 hour)
3. **Fills gaps between meetings** with your tasks
4. **Distributes remaining tasks** after your last meeting
5. **Uploads everything** to Clockify in chronological order

### Example Schedule:
```
09:00 - 09:30  → Task: Code Review
09:30 - 09:45  → Daily Standup
09:45 - 13:00  → Task: API Development
13:00 - 14:00  → 🍽️ Lunch
14:00 - 14:30  → Task: Bug Fixes
14:30 - 15:00  → Team Meeting
15:00 - 18:00  → Task: Documentation
```

## 💾 Local Storage

The app stores the following in your browser:
- **API Configuration**: Your API key and default project
- **Task History**: Last 10 task descriptions used
- **Meeting History**: Last 10 meeting names used
- **Cache**: Your last configured meetings and tasks
- **Language Preference**: English or Spanish

To clear all data: Click **🗑️ Clear Cache**

## 🌍 Language Support

- **English** (default)
- **Español**

The app automatically detects your browser language and can be changed anytime using the language selector in the top-right corner.

## 🔒 Privacy & Security

- ✅ Everything runs locally in your browser
- ✅ No data is sent to any server except Clockify API
- ✅ Your API key is stored only in your browser
- ✅ Open source - you can audit the code
- ⚠️ Keep your API key private
- ⚠️ Don't share your `index.html` if you've entered your API key

## 🛠️ Troubleshooting

### API Key Invalid
- Double-check your API key in Clockify settings
- Make sure you copied the entire key
- Try generating a new key

### Projects Not Loading
- Verify your API key is correct
- Check your internet connection
- Open browser console (F12) for error details

### Entries Not Appearing in Clockify
- Check if you selected the correct date
- Verify the correct project was selected
- Look in Clockify under the specific date
- Check your workspace matches your API key

### Reset Everything
- Click **Clear Cache** button
- Refresh the page
- Reconfigure your API key

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Development
```bash
git clone https://github.com/yourusername/clockify-time-tracker.git
cd clockify-time-tracker
# Open index.html in your browser
```

## 📝 License

MIT License - feel free to use this for personal or commercial projects.

## 🙏 Acknowledgments

- Built with ❤️ for productivity enthusiasts
- Uses [Clockify API](https://clockify.me/developers-api)
- Inspired by the need for better time tracking automation

## 📞 Support

If you find this useful, please ⭐️ star the repository!

For issues or questions:
- Open an issue on GitHub
- Check existing issues for solutions

## 🔮 Future Features

- [ ] Multiple workspace support
- [ ] Custom break times
- [ ] Weekly/monthly templates
- [ ] Export schedule as CSV
- [ ] Dark mode
- [ ] Mobile-responsive design improvements

---

**Made with 💜 for better time management**

