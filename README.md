# API-INTEGRATION
COMPANY: CODTECH IT SOLUTIONS
NAME: M.SURIYA PRABHA
INTERN ID: CTISO483
DOMAIN: FULL STACK WEB DEVELOPMENT
DURATION: 4 WEEKS
MENTOR: NEELA SANTHOSH


**🌦️ WEATHER APPLICATION  – API INTEGRATION**

**📌 Overview**

This Weather Application is a responsive web-based project that allows users to search for real-time weather information for any city, village, or PIN code in India.
The application integrates free and reliable public APIs to fetch geolocation and live weather data without requiring an API key.



**🔗 APIs Used**

1️⃣ OpenStreetMap Nominatim API (Geocoding)

Used to convert user-entered location names (city/village/PIN code) into geographical coordinates (latitude & longitude).

Endpoint:

https://nominatim.openstreetmap.org/search

Request Parameters:

format=json – Response format

q – Location entered by the user (appended with India)


Example Request:

https://nominatim.openstreetmap.org/search?format=json&q=Delhi, India

Response Data Used:

lat – Latitude

lon – Longitude

display_name – Full location name





2️⃣ Open-Meteo Weather API (Live Weather Data)

Used to fetch current weather conditions using latitude and longitude obtained from the geocoding API.

Endpoint:

https://api.open-meteo.com/v1/forecast

Request Parameters:

latitude

longitude

current_weather=true


Example Request:

https://api.open-meteo.com/v1/forecast?latitude=28.61&longitude=77.23&current_weather=true

Response Data Used:

temperature – Current temperature (°C)

windspeed – Wind speed (km/h)

weathercode – Weather condition code



---

🔄 API Workflow

1. User enters location (City / Village / PIN Code)


2. App sends request to Nominatim API


3. Latitude & longitude are extracted


4. Coordinates are passed to Open-Meteo API


5. Live weather data is fetched


6. Weather information is displayed on the UI with animations




---

⚙️ JavaScript Integration Example

const geoRes = await fetch(
  `https://nominatim.openstreetmap.org/search?format=json&q=${place}, India`
);
const geoData = await geoRes.json();

const weatherRes = await fetch(
  `https://api.open-meteo.com/v1/forecast?latitude=${lat}&longitude=${lon}&current_weather=true`
);
const data = await weatherRes.json();


---

🚀 Features Enabled by API Integration

🌍 Location-based weather search

⚡ Fast response without API keys

🌦️ Live temperature & wind speed

🧭 Supports cities, villages & PIN codes

🔄 Loader animation during API calls

🎨 Smooth UI transitions



---

🔐 API Notes

No authentication or API key required

Uses public, open-source APIs

Subject to fair-use limits of respective providers

Internet connection required for live data



---

📌 Conclusion

This project demonstrates real-world API integration using modern JavaScript (fetch, async/await) and provides accurate, real-time weather data with a clean and user-friendly interface.


---

If you want, I can also:

Add weather condition text/icons

Create a flow diagram

Convert this into a college project README

Improve API error handling


Just tell me 👍
