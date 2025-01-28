# 🌤️ Java Weather Backend HTTP Server

A simple Java-based HTTP server that fetches weather data using the [OpenWeatherMap API](https://openweathermap.org/api). This server is built with Java's `HttpServer` and handles requests to provide weather information for a specified city.

---

## 🚀 Features

- Fetches current weather data for any city 🌍
- Handles invalid or missing query parameters with meaningful error messages ❌
- Connects to the OpenWeatherMap API and returns JSON responses 📡

---

## 🛠️ Requirements

- Java 8 or higher ☕
- OpenWeatherMap API key 🔑

---

## 🏗️ Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/martinrosik/WeatherAppBackend.git
   cd WeatherAppBackend
   ```

2. Replace the `apiKey` variable in the `HTTPServer` class with your OpenWeatherMap API key:

   ```java
   String apiKey = "your_api_key_here";
   ```

3. Compile the Java program:

   ```bash
   javac HTTPServer.java
   ```

4. Run the server:

   ```bash
   java HTTPServer
   ```

---

## 📋 Usage

1. Start the server. It will run on port `8080` by default.
2. Use an HTTP client (like Postman, Curl, or a browser) to make a GET request to:

   ```
   http://localhost:8080/weather?city={city_name}
   ```

   Replace `{city_name}` with the desired city (e.g., `London`).

### Example Request:

```bash
curl http://localhost:8080/weather?city=London
```

### Example Response:

```json
{
  "coord": { "lon": -0.13, "lat": 51.51 },
  "weather": [
    { "id": 300, "main": "Drizzle", "description": "light intensity drizzle", "icon": "09d" }
  ],
  "main": { "temp": 280.32, "pressure": 1012, "humidity": 81 },
  "name": "London"
}
```

---

## 🌟 Error Handling

- **Missing city parameter:**
  ```json
  {"error":"'city' query parameter is required."}
  ```

- **City not found:**
  ```json
  {"error":"City not found."}
  ```

- **Server issues:**
  ```json
  {"error":"Unable to fetch weather data."}
  ```

---

## 🧑‍💻 Development

Feel free to contribute! Fork the repository and submit a pull request. Contributions are welcome! 🙌

---

## 📜 License

This project is licensed under the MIT License. 📝

---

## 💡 Acknowledgments

- [OpenWeatherMap](https://openweathermap.org/) for providing the API 🌐
- Java `HttpServer` documentation 📖

---

## 📂 Directory Structure

```
java-weather-backend/
├── HTTPServer.java  # Main server file
├── README.md        # Project documentation
```

---

## 🔗 Links

- OpenWeatherMap API: [https://openweathermap.org/api](https://openweathermap.org/api)
- GitHub Repository: [https://github.com/martinrosik/WeatherAppBackend](https://github.com/martinrosik/WeatherAppBackend)
