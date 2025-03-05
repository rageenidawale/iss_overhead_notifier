# 🌍 ISS Overhead Notifier – Look Up! 🚀

This Python script **tracks the International Space Station (ISS)** and **sends an email notification** when the ISS is overhead at your location **during nighttime**.

---

## ✨ Features
- Uses **API requests** to fetch **real-time ISS location**.
- Determines whether it is **nighttime** at your location.
- Sends an **email notification** when the ISS is visible.
- Runs continuously, **checking every 60 seconds**.

---

## 🛠 Setup Instructions

### 1️⃣ Install Dependencies

Ensure you have Python installed, then install the required package:

```bash
pip install requests
```

---

### 2️⃣ Configure Your Location

Modify these variables in the script to your **latitude** and **longitude**:

```python
MY_LAT = 18.520430   # Your latitude
MY_LONG = 73.856743  # Your longitude
```

You can find your **latitude** and **longitude** using [Google Maps](https://www.google.com/maps).

---

### 3️⃣ Set Up Email Credentials

Update these fields with your email details:

```python
MY_EMAIL = "your_email@example.com"
MY_PASSWORD = "your_password"
```

⚠️ **Important:** If using Gmail, you may need to enable ["Less Secure Apps"](https://myaccount.google.com/lesssecureapps) or generate an [App Password](https://myaccount.google.com/apppasswords).

---

### 4️⃣ Run the Script

Execute the script:

```bash
python iss_tracker.py
```

The script will check every **60 seconds** if the ISS is overhead and send an email if it is **nighttime**.

---

## 🔬 How It Works

1. **Fetches ISS location** from the [Open Notify API](http://api.open-notify.org/iss-now.json).
2. **Checks if ISS is near** your coordinates (±5°).
3. **Determines local sunrise/sunset** using [Sunrise-Sunset API](https://sunrise-sunset.org/api).
4. **If ISS is overhead & it's nighttime**, sends an **email alert**.
5. **Repeats every 60 seconds**.
