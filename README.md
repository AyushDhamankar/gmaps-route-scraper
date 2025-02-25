# 🚦 gmaps-route-scraper

A **lightweight Node.js package** that scrapes **travel duration & distance** from **Google Maps**.  
Simply call the function with a **source, destination, and mode**, and get the travel details in JSON format.  

![gmaps-route-scraper](https://github.com/user-attachments/assets/45e7bc6f-cd1f-44e2-8d64-e550e66edef6)

---

## Installation 🔌

Install via npm:

```bash
npm install gmaps-route-scraper
```

Or via yarn:

```bash
yarn add gmaps-route-scraper
```

---

## Usage 🕹️

Simply import the package and call the `getRouteDetails` function:

```javascript
const { getRouteDetails } = require("gmaps-route-scraper");

(async () => {
  try {
    const route = await getRouteDetails("Virar East", "Olympus-A", "Driving");
    console.log(route);
  } catch (error) {
    console.error("Error:", error.message);
  }
})();
```

---

## Available Travel Modes 🚗 🚲 🚶‍♂️

| Mode           | Description                 |
|--------------|-----------------------------|
| `"Driving"`    | Travel by **car**           |
| `"Two-wheeler"` | Travel by **bike/scooter** |

---

## Output 📲

The function returns a JSON object with travel details:

```json
{
  "mode": "Driving",
  "time": "42 min",
  "distance": "18 km"
}
```

If no route is found, it returns:

```json
{
  "message": "No Driving route found"
}
```

---

## Notes ⚠️

- Google Maps UI may **change**, affecting the scraping.
- Puppeteer may require **extra setup** on some servers.
- **Use responsibly**—excessive requests may get blocked by Google.

---

## License 📜

This project is **MIT Licensed**.