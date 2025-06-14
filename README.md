```bash
  ______   _______   __      __  _______   ________  ______
 /      \ /       \ /  \    /  |/       \ /        |/      \
/$$$$$$  |$$$$$$$  |$$  \  /$$/ $$$$$$$  |$$$$$$$$//$$$$$$  |
$$ |  $$/ $$ |__$$ | $$  \/$$/  $$ |__$$ |   $$ |  $$ |  $$ |
$$ |      $$    $$<   $$  $$/   $$    $$/    $$ |  $$ |  $$ |
$$ |   __ $$$$$$$  |   $$$$/    $$$$$$$/     $$ |  $$ |  $$ |
$$ \__/  |$$ |  $$ |    $$ |    $$ |         $$ |  $$ \__$$ |
$$    $$/ $$ |  $$ |    $$ |    $$ |         $$ |  $$    $$/
 $$$$$$/  $$/   $$/     $$/     $$/          $$/    $$$$$$/
  ______   _______   ________  __    __
 /      \ /       \ /        |/  |  /  |
/$$$$$$  |$$$$$$$  |$$$$$$$$/ $$ |  $$ |
$$ |__$$ |$$ |__$$ |$$ |__    $$  \/$$/
$$    $$ |$$    $$/ $$    |    $$  $$<
$$$$$$$$ |$$$$$$$/  $$$$$/      $$$$  \
$$ |  $$ |$$ |      $$ |_____  $$ /$$  |
$$ |  $$ |$$ |      $$       |$$ |  $$ |
$$/   $$/ $$/       $$$$$$$$/ $$/   $$/
```

# Telegram RSI Bot

This project is a Python bot that scans a set list of coins and returns their 15-minute Relative Strength Index (RSI) using the Bybit API v5. The bot also monitors the RSI every 15 minutes and sends an alert if the RSI is below 30.

Telegram: https://t.me/vertexapex_hub

Discord: https://discord.gg/P265G7Ex

## Features

- Fetches 15-minute RSI values for a list of predefined coins.
- Monitors the RSI every 15 minutes.
- Sends an alert message to a specified Telegram thread if any coin's RSI is below 30.

## Requirementss

- Python 3.6+
- `python-telegram-bot` library
- `python-dotenv` library
- `requests` library
- `pandas` library
- `ta` library
- `schedule` library

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/CryptoApex23/rsi-signals.git
   cd rsi-signals
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv python_signals_env
   source python_signals_env/bin/activate  # On Windows, use `python_signals_env\Scripts\activate`
   ```

3. Install the required libraries:

   ```bash
   pip install python-telegram-bot python-dotenv requests pandas ta schedule
   ```

4. Create a `.env` file in the root of your project directory and add your bot token, Bybit API keys, and thread ID:

   ```plaintext
   BOT_TOKEN=your_telegram_bot_token_here
   BYBIT_API_KEY=your_bybit_api_key_here
   BYBIT_API_SECRET=your_bybit_api_secret_here
   THREAD_ID=your_thread_id_here
   ```

5. Create a `settings.json` file in the root of your project directory to configure the interval, coins to scan, and RSI threshold:

   ```json
   {
     "interval_minutes": 15,
     "coins": ["TONUSDT", "BTCUSDT", "ETHUSDT"],
     "rsi_threshold": 30,
     "check_interval": 15
   }
   ```

## Usage

To get an api key go to ByBit: (this is an affiliate link, it will help me and cost you nothing XD)

    ```bash
    https://www.bybit.com/invite?ref=QXQVLK
    ```

1. Replace `your_telegram_bot_token_here`, `your_bybit_api_key_here`, `your_bybit_api_secret_here` with your actual credentials in the `.env` file.
2. Run the script:

   ```bash
   python signals_main.py
   ```

3. It will run every 15 minutes and send a telegram message if the RSI value is below 30 (You can change that in signals_main.py)

## Project Structure

- `signals_main.py`: Main Entry point.
- `bot_sender.py`: Contains the function to send messages to a specific Telegram thread.
- `rsi_calculator.py`: Contains the logic to fetch RSI values for specified coins using the Bybit API.
- `.env`: File to store environment variables (not included in the repository).
- `settings.json`: Configuration file for setting the interval, coins to scan, and RSI threshold.

## License

This project is licensed under the MIT License.

## Contributing

Feel free to submit issues or pull requests if you have any improvements or bug fixes. Contributions are welcome!

## Donation

Help me keep the light on and maintane all the projects <3

BTC

```bash
bc1qxwlpy6fx33e968uqhw7pr030kvyr3pel0ptxt3
```

ETH

```bash
0x8a530A5eC57d7D7944E23Ffc5D85dA09c52C8eda
```

SOL

```bash
FCfyeS5LwsjjgGiJKAikYFwPoweBcVLYASjRstEhHaAs
```

## Author

Developed by [CryptoApex23](https://github.com/CryptoApex23).
