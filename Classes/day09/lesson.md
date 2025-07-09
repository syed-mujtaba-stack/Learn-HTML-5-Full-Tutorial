# Day 9: Geolocation API

## HTML5 Geolocation
The Geolocation API allows you to access the user's location.

### Basic Usage
```javascript
// Get current position
navigator.geolocation.getCurrentPosition(
    function(position) {
        console.log('Latitude: ' + position.coords.latitude);
        console.log('Longitude: ' + position.coords.longitude);
    },
    function(error) {
        console.error('Error: ' + error.message);
    }
);

// Watch position changes
const watchId = navigator.geolocation.watchPosition(
    function(position) {
        // Update position
    },
    function(error) {
        // Handle error
    }
);

// Clear watch
navigator.geolocation.clearWatch(watchId);
```

### Geolocation Properties
- `coords.latitude`: Latitude
- `coords.longitude`: Longitude
- `coords.accuracy`: Accuracy in meters
- `coords.altitude`: Altitude
- `coords.speed`: Speed in meters/second
- `coords.heading`: Direction of travel
- `timestamp`: Time when position was obtained

## Exercise
Create a location-based application that:
1. Shows user's current location on a map
2. Calculates distance between two points
3. Shows nearby points of interest
4. Implements error handling for location access
5. Uses geolocation data to provide relevant information

Save your work as `exercise.html` in this folder.
