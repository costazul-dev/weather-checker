# Weather-Checker

Weather-Checker is a Python script designed to run on a Raspberry Pi with a display. The script fetches weather forecasts for specific locations and displays them, helping you plan your day more effectively.

## Inspiration

The project was inspired by the significant temperature difference between my home and workplace, often ranging between 20-30 degrees. This discrepancy makes it challenging to dress appropriately in the morning, so I created Weather-Checker to provide real-time weather updates for multiple locations.

## Features

- **Multi-Location Weather Forecasts**: Get weather updates for multiple locations.
- **Customizable Display**: Compatible with various display types connected to the Raspberry Pi.
- **Automated Updates**: Scheduled to run via `crontab` for regular weather updates.

## Requirements

- Raspberry Pi (with internet connection)
- A display connected to the Raspberry Pi
- Python 3.x
- Required Python libraries (listed in `requirements.txt`)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/costazul-dev/weatherDisplay.git
   cd weatherDisplay
   ```

2. **Install the required libraries**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your API key**:
   - Sign up for a weather API service (e.g., OpenWeatherMap, Weatherstack).
   - Create a `.env` file in the project directory and add your API key:
     ```
     WEATHER_API_KEY=your_api_key_here
     ```

4. **Configure the script**:
   - Edit the `config.py` file to add your locations and display settings.

## Usage

1. **Run the script manually**:
   ```bash
   python weather_checker.py
   ```

2. **Schedule the script using `crontab`**:
   - Open the crontab editor:
     ```bash
     crontab -e
     ```
   - Add the following line to schedule the script (e.g., every hour):
     ```bash
     0 * * * * /usr/bin/python3 /path/to/weather_checker.py
     ```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [OpenWeatherMap](https://openweathermap.org/) for their weather API.
- Raspberry Pi community for their support and resources.

## Contact

For any inquiries or issues, please contact me at [costazul.dev+weather-checker@example.com](mailto:your-email@example.com).