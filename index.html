<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Transport Cost Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      max-width: 500px;
      margin: auto;
      background: #f8f8f8;
      color: #333;
    }
    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
    }
    input, button {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 16px;
    }
    button {
      background-color: #007bff;
      color: #fff;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h2>Trip Cost Calculator</h2>

  <label for="start">Pickup Address:</label>
  <input type="text" id="start" placeholder="Enter pickup location">

  <label for="end">Drop-off Address:</label>
  <input type="text" id="end" placeholder="Enter drop-off location">

  <label for="pricePerMile">Price per Mile:</label>
  <input type="number" id="pricePerMile" value="2.00" step="0.01">

  <button onclick="calculateDistance()">Calculate Cost</button>

  <div id="result"></div>

  <script>
    let startAutocomplete, endAutocomplete;

    // Initialize autocomplete for both address fields
    function initAutocomplete() {
      startAutocomplete = new google.maps.places.Autocomplete(
        document.getElementById("start"),
        { types: ["geocode"] }
      );
      endAutocomplete = new google.maps.places.Autocomplete(
        document.getElementById("end"),
        { types: ["geocode"] }
      );
    }

    function calculateDistance() {
      const start = document.getElementById("start").value;
      const end = document.getElementById("end").value;
      const pricePerMile = parseFloat(document.getElementById("pricePerMile").value);

      if (!start || !end) {
        alert("Please enter both pickup and drop-off addresses.");
        return;
      }

      const service = new google.maps.DistanceMatrixService();
      service.getDistanceMatrix(
        {
          origins: [start],
          destinations: [end],
          travelMode: "DRIVING",
          unitSystem: google.maps.UnitSystem.IMPERIAL,
        },
        (response, status) => {
          if (status !== "OK") {
            alert("Error: " + status);
          } else {
            const distanceText = response.rows[0].elements[0].distance.text; // e.g. "12.3 mi"
            const distanceMiles = parseFloat(distanceText.replace(" mi", ""));
            const cost = (distanceMiles * pricePerMile).toFixed(2);

            document.getElementById("result").innerText =
              `Distance: ${distanceMiles} miles\nEstimated Cost: $${cost}`;

            // Send results back to parent form (like JotForm)
            window.parent.postMessage({ distance: distanceMiles, cost: cost }, "*");
          }
        }
      );
    }
  </script>

  <!-- Load Google Maps API with Places library -->
  <script async defer
    src="https://maps.googleapis.com/maps/api/js?key=AIzaSyB3ABn5E6cUKrZ3nsrlzzrJ5azousw83-I&libraries=places&callback=initAutocomplete">
  </script>
</body>
</html>
