# Tibber Energy Price Monitoring with Emergency Mode

This project provides a script that monitors electricity prices using the Tibber API. It introduces an emergency mode that automatically activates when electricity prices exceed a set threshold consecutively.

## Features
- **Real-Time Monitoring:** Check electricity prices in real-time using the Tibber API.
- **Emergency Mode:** Activate emergency mode to reduce energy usage during high price periods.
- **Configurable Thresholds:** Set price thresholds and monitoring intervals.

## Requirements
- A Tibber account and API token.
- A Shelly device to run the script.
- Access to the device's settings for script configuration.

## Setup and Configuration

1. **API Setup:** Obtain your API token from the Tibber dashboard and note down the endpoint.
   
2. **Script Configuration:**
   - Update the `TIBBER_CONFIG` object in the script with your Tibber API details, threshold values, and the checking interval.

   ```javascript
   const TIBBER_CONFIG = {
     apiEndpoint: "https://api.tibber.com/v1-beta/gql",
     accessToken: "YOUR_TIBBER_API_TOKEN",
     maxEnergyPrice: 0.65,
     checkInterval: 60 * 10000 // Check every 10 minutes
   };
