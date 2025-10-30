# Weather-Api-Integrated---BI-Dashboard
# 🌤️ Build a Weather Dashboard with Power BI & WeatherAPI

Create a live weather dashboard that updates in real-time! This guide shows you exactly how to connect WeatherAPI to Power BI and visualize weather data beautifully.

## 🎯 Why WeatherAPI?

WeatherAPI gives you live weather data in a format Power BI loves. It's simple, reliable, and perfect for building weather dashboards.

## ✅ What You Need

- 🔑 Free account on WeatherAPI.com
- 💻 Power BI Desktop installed
- 📊 Basic Power BI knowledge

---

## 🚀 Step 1: Get Your API Key

1. Sign up at WeatherAPI.com
2. Copy your API key from the dashboard
3. Keep it handy—you'll need it next!

---

## 🔗 Step 2: Create Your API URL

Build your URL like this:

```
https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=CITY_NAME
```

Just replace `YOUR_API_KEY` and `CITY_NAME` with your details.

---

## 🔌 Step 3: Connect Power BI to WeatherAPI

1. Open Power BI Desktop
2. Click **Get Data** → **Web**
3. Paste your WeatherAPI URL
4. Hit **OK**

Power BI will fetch your weather data!

---

## 🔧 Step 4: Clean Up Your Data

In the Power Query Editor:

- ✅ Expand the current record
- ✅ Expand condition and air_quality fields
- ✅ Rename columns to make sense
- ✅ Click **Close & Apply**

Now your data is ready to use!

---

## 📊 Step 5: Build Your Visuals

Add these visualizations:

- 🌡️ **Cards** for temperature and humidity
- 💨 **Gauges** for wind speed
- 📈 **Charts** for daily trends
- 🎚️ **Slicers** to switch between cities

---

## 🎨 Step 6: Make It Look Amazing

- ☀️ Add weather icons
- 🗺️ Show cities on a map
- 🖱️ Let users select different cities

---

## 💡 Step 7: Add Air Quality Index (AQI)

Use this simple DAX formula:

```dax
AQI Status = 
SWITCH(
    TRUE(),
    [current.air_quality] <= 50, "Good",
    [current.air_quality] <= 100, "Moderate",
    [current.air_quality] <= 150, "Unhealthy",
    "Very Unhealthy"
)
```

This shows if the air quality is good or bad!

---

## 🎉 You're Done!

You now have a working weather dashboard with live data! Perfect for tracking weather conditions across multiple cities in real-time.

**Pro tip:** You can expand this with forecasts, historical data, or weather alerts! ⚡
