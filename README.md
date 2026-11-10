# 🌤️ WeatherBuddy

A lightweight command-line tool that shows the weather forecast for any city in seconds.

![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.9%2B-blue)

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Configuration](#configuration)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Features
- Current weather and 5-day forecast for any city
- Temperature in Celsius or Fahrenheit
- Works offline using cached data from the last request
- Colorful, easy-to-read terminal output

## Installation

**Requirements:** Python 3.9 or newer and a free API key from [OpenWeather](https://openweathermap.org/api).

```bash
git clone https://github.com/your-username/weatherbuddy.git
cd weatherbuddy
pip install -r requirements.txt
```

## Quick Start

```bash
export WEATHER_API_KEY="your_api_key_here"
python weatherbuddy.py Almaty
```

Example output:

```
📍 Almaty, KZ
Now: 12°C, partly cloudy
Tomorrow: 14°C, sunny
```

## Usage

| Command | Description |
|---|---|
| `python weatherbuddy.py <city>` | Current weather |
| `python weatherbuddy.py <city> --forecast` | 5-day forecast |
| `python weatherbuddy.py <city> --units imperial` | Use Fahrenheit |
| `python weatherbuddy.py --help` | Show all options |

## Configuration

| Variable | Required | Default | Description |
|---|---|---|---|
| `WEATHER_API_KEY` | Yes | none | Your OpenWeather API key |
| `WEATHER_UNITS` | No | `metric` | `metric` or `imperial` |
| `WEATHER_CACHE_TTL` | No | `600` | Cache lifetime in seconds |

## Project Structure

```
weatherbuddy/
├── weatherbuddy.py   # Entry point
├── api.py            # Requests to the weather API
├── cache.py          # Local caching logic
├── tests/            # Unit tests
└── requirements.txt
```

## Contributing

1. Fork the repository
2. Create a branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m "Add my feature"`
4. Push and open a Pull Request

Please link your PR to an issue (e.g., `Closes #12`) and make sure tests pass:

```bash
pytest
```

## License

Distributed under the MIT License. See `LICENSE` for details.
