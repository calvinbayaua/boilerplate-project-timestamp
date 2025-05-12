# 🕒 Timestamp Microservice

The **Timestamp Microservice** is a simple API that parses dates and returns them in JSON format. Users can query the `/api/` endpoint with a date string or Unix timestamp and receive both the UTC and Unix time representations.

## 📖 Learning Journey
This project was built while following [freeCodeCamp's Back End Development and APIs Course](https://www.freecodecamp.org/learn/back-end-development-and-apis).

## 🛠️ Tech Stack
- **Frontend:** HTML, CSS
- **Backend:** Node.js (Express.js)

## 🎯 Features
- Accepts a date string or Unix timestamp via the `/api/:date` route.
- Returns a JSON response with:
  - `unix`: Unix time in milliseconds.
  - `utc`: Date in GMT/UTC string format.
- Returns the current date/time if no date is provided.
- Handles invalid dates with a helpful error message.

## 🚀 Usage Examples

### Request: Valid Date
GET /api/2025-01-01
**Response:**
```json
{
  "unix": 1735689600000,
  "utc": "Wed, 01 Jan 2025 00:00:00 GMT"
}
```

### Request: Unix Timestamp
GET /api/1735689600000
```json
{
  "unix": 1735689600000,
  "utc": "Wed, 01 Jan 2025 00:00:00 GMT"
}
```

### Request: Invalid Date
GET /api/invalid-date
```json
{
  "error": "Invalid Date"
}
```
## 📦 Installation & Setup
1. **Clone the repository:**
  ```sh
  git clone https://github.com/calvinbayaua/boilerplate-project-timestamp.git
  cd boilerplate-project-timestamp
  ```
2. **Install dependencies:**
  ```sh
  npm i
  ```
3. **Start the server**
  ```sh
  npm run start
  ```
