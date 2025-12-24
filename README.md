# API-INTEGRATION

COMPANY: CODTECH IT SOLUTIONS

NAME: M.SURIYA PRABHA

INTERN ID: CTISO483

DOMAIN: FULL STACK WEB DEVELOPMENT

DURATION: 4 WEEKS

MENTOR: NEELA SANTHOSH


**WEATHER APPLICATION  – API INTEGRATION**

**Overview**

This Weather Application is a responsive web-based project that allows users to search for real-time weather information for any city, village, or PIN code in India.
The application integrates free and reliable public APIs to fetch geolocation and live weather data without requiring an API key.

**Objectives**
To fetch real-time weather data using APIs
To demonstrate API integration using JavaScript
To build a clean, responsive, and animated user interface
To deploy a frontend project using GitHub Pages

**Tools & Technologies Used**
Programming Languages:
HTML5 – Structure of the web pages
CSS3 – Styling, layout, animations, and responsiveness
JavaScript (ES6) – Logic, API integration, and DOM manipulation

**Development Tools**
Visual Studio Code (VS Code) – Code editor
Git – Version control system
GitHub – Repository hosting and collaboration

**Application Architecture**
Frontend-only application
No backend or database required
Uses fetch() API with async/await
Fully runs in the browser

**APIs Used**

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


**API Workflow**

1. User enters location (City / Village / PIN Code)


2. App sends request to Nominatim API


3. Latitude & longitude are extracted


4. Coordinates are passed to Open-Meteo API


5. Live weather data is fetched


6. Weather information is displayed on the UI with animations




 **JavaScript Integration Example**
 
const geoRes = await fetch(
  `https://nominatim.openstreetmap.org/search?format=json&q=${place}, India`
);
const geoData = await geoRes.json();

const weatherRes = await fetch(
  `https://api.open-meteo.com/v1/forecast?latitude=${lat}&longitude=${lon}&current_weather=true`
);
const data = await weatherRes.json();


 **Features Enabled by API Integration**

1. Location-based weather search

2. Fast response without API keys

3. Live temperature & wind speed

4. Supports cities, villages & PIN codes

5. Loader animation during API calls

6. Smooth UI transitions


**API Notes**

1.No authentication or API key required

2.Uses public, open-source APIs

3.Subject to fair-use limits of respective providers

4.Internet connection required for live data


**Conclusion**

This project demonstrates real-world API integration using modern JavaScript (fetch, async/await) and provides accurate, real-time weather data with a clean and user-friendly interface.


**OUTPUT**

<img width="1918" height="1006" alt="Image" src="https://github.com/user-attachments/assets/bfebac4b-759a-461e-87c7-6f0c0eb359e7" />

<img width="1919" height="1012" alt="Image" src="https://github.com/user-attachments/assets/d1c6b2e7-b94b-493e-a94a-17a5eeb6ae04" />

<img width="1919" height="1003" alt="Image" src="https://github.com/user-attachments/assets/79e480d0-abb0-41d7-b948-c601848711b2" />




