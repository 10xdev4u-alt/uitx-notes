---
title: "Unit II: Geolocation API"
id: unit2-topic7-geolocation-api
tags:
  - unit-2
  - html5
  - geolocation
  - javascript
  - api
  - location-services
aliases:
  - "HTML5 Geolocation"
links:
  - "[[UITx/Unit_02_Topic_06_Drag_and_Drop_API.md|Drag and Drop API]]"
  - "[[UITx/Unit_02_Topic_08_Web_Storage.md|Web Storage]]"
---

# Unit II, Topic 7: Geolocation API

> [!quote] The web is not an isolated realm; it is deeply connected to our physical world. The Geolocation API acts as a bridge, allowing web applications to understand a user's physical location, enabling a new class of location-aware services. Let us explore this powerful, yet sensitive, capability.

## 1. What is the Geolocation API?

The **HTML5 Geolocation API** provides a standard way for web applications to access a user's geographical location. It is a JavaScript API that, with the user's explicit permission, can determine the user's position using various methods like GPS, Wi-Fi, cellular networks, or IP address.

This API is crucial for location-based services such as:
-   Mapping and navigation applications.
-   Local search (e.g., "restaurants near me").
-   Weather services.
-   Social media check-ins.
-   Augmented reality games.

## 2. Privacy and Security: A Core Consideration

Accessing a user's location is a significant privacy concern. Therefore, the Geolocation API is designed with a strong emphasis on user consent.

-   **Explicit Permission:** A web application cannot access a user's location without first asking for and receiving their explicit permission through a browser-native prompt.
-   **Secure Contexts:** Modern browsers require that pages using the Geolocation API be served over a secure context (HTTPS).

> [!warning] **Handle with Care**
> Always handle location data responsibly. Inform users why you are requesting their location and how you will use it. Never store or share location data without clear consent.

## 3. Using the Geolocation API

The API is accessed through the `navigator.geolocation` object.

### a) Checking for Support
Before using the API, it's good practice to check if the user's browser supports it.

```javascript
if ("geolocation" in navigator) {
  // Geolocation is available
} else {
  // Geolocation is not available
  console.log("Geolocation is not supported by this browser.");
}
```

### b) Getting the Current Position
The `getCurrentPosition()` method is used to get the user's current location one time. It is an asynchronous operation.

`navigator.geolocation.getCurrentPosition(successCallback, errorCallback, options);`

-   **`successCallback`**: A function that is executed when the location is successfully retrieved. It receives a `Position` object as its argument.
-   **`errorCallback`**: (Optional) A function that is executed if an error occurs while trying to get the location. It receives an `Error` object.
-   **`options`**: (Optional) An object to configure the location request (e.g., accuracy, timeout).

#### The `Position` Object
The `successCallback` function receives a `Position` object, which contains:
-   `coords`: A `Coordinates` object with the location data.
    -   `coords.latitude`: The latitude as a decimal number.
    -   `coords.longitude`: The longitude as a decimal number.
    -   `coords.accuracy`: The accuracy of the position in meters.
    -   `coords.altitude`: The altitude in meters above the mean sea level (if available).
    -   `coords.speed`: The speed in meters per second (if available).
    -   `coords.heading`: The direction of travel in degrees (if available).
-   `timestamp`: The date/time when the location was retrieved.

### c) Example: Getting Current Position

#### HTML:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Geolocation Example</title>
</head>
<body>
    <h1>Geolocation API</h1>
    <button id="find-me">Show my location</button>
    <div id="location-info"></div>
    <script src="geo.js"></script>
</body>
</html>
```

#### JavaScript (`geo.js`):
```javascript
const findMeButton = document.getElementById('find-me');
const locationInfo = document.getElementById('location-info');

findMeButton.addEventListener('click', () => {
    if ("geolocation" in navigator) {
        locationInfo.textContent = "Locating...";
        
        // Define success and error callbacks
        const success = (position) => {
            const latitude = position.coords.latitude;
            const longitude = position.coords.longitude;
            
            locationInfo.innerHTML = `
                <p>Latitude: ${latitude}°</p>
                <p>Longitude: ${longitude}°</p>
                <p>Accuracy: ${position.coords.accuracy} meters</p>
                <a href="https://www.openstreetmap.org/#map=18/${latitude}/${longitude}" target="_blank">Show on map</a>
            `;
        };
        
        const error = (error) => {
            locationInfo.textContent = `Error: ${error.message} (Code: ${error.code})`;
        };
        
        // Request the user's location
        navigator.geolocation.getCurrentPosition(success, error);
        
    } else {
        locationInfo.textContent = "Geolocation is not supported by your browser.";
    }
});
```

### d) Watching the Position
The `watchPosition()` method is used to continuously monitor the user's location. It works similarly to `getCurrentPosition()`, but it repeatedly retrieves the user's position and calls the `successCallback` function every time the position changes.

`const watchId = navigator.geolocation.watchPosition(successCallback, errorCallback, options);`

-   It returns a `watchId` which can be used with `navigator.geolocation.clearWatch(watchId)` to stop monitoring the location.

## 4. Exam-Oriented Insights

Geolocation is a key API for modern web applications.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is the primary purpose of the HTML5 Geolocation API?**
>     *Answer:* The Geolocation API provides a standard way for web applications to access a user's geographical location, with their explicit permission.
> 2.  **Why is user permission a critical aspect of the Geolocation API?**
>     *Answer:* Accessing a user's location is a significant privacy concern. Requiring explicit permission ensures that users have control over their private data and protects them from unauthorized tracking.
> 3.  **Which JavaScript object is the entry point for the Geolocation API?**
>     *Answer:* The `navigator.geolocation` object.
> 4.  **Differentiate between `getCurrentPosition()` and `watchPosition()`.**
>     *Answer:* `getCurrentPosition()` retrieves the user's location once, while `watchPosition()` continuously monitors the user's location and reports updates as the position changes.

> [!tip] **For Higher Mark Questions:**
> Be prepared to write a complete HTML and JavaScript code snippet to get a user's current location and display the latitude and longitude. Explain the asynchronous nature of the API and the roles of the success and error callback functions. Discuss the privacy implications and the importance of secure contexts (HTTPS) when using this API.
