# Zern Class Documentation


## Usage

```python
from zern import Trader
trader = Trader(user_name=YOUR_USERNAME,password=YOUR_PASSWORD,totp_key=YOUR_TOTP_KEY)
```

The `Trader` class is used to initiate the trading process and interact with the trading platform. It provides various methods to retrieve data, manage orders, and access trading information.

Check above in requirements if you need to get the totp key

### Methods

#### `historical_data(instrument_token, start_date, end_date, interval='5minute')`

Retrieves historical data for a specific instrument within a specified time range.

- `instrument_token` (int): The unique identifier of the instrument.
- `start_date` (str or datetime.datetime): The start date of the historical data (format: 'YYYY-MM-DD').
- `end_date` (str or datetime.datetime): The end date of the historical data (format: 'YYYY-MM-DD').
- `interval` (str, optional): The interval for data (default: '5minute').


`get_orders()` - Retrieves the list of orders placed by the trader.

#### `get_positions()`

Retrieves the current positions held by the trader.

#### `get_holdings()`

Retrieves the holdings (securities owned) by the trader.

#### `get_margins()`

Retrieves the margin details for the trader's account.

#### `get_profile()`

Retrieves the trader's profile information.

#### `check_app_sessions()`

Checks the active sessions for the trading application.

#### `place_order(symbol, exchange, transaction_type, quantity)`

Places an order for a specific security.

- `symbol` (str): The symbol of the security.
- `exchange` (str): The exchange where the security is listed.
- `transaction_type` (str): The type of transaction (e.g., 'BUY', 'SELL').
- `quantity` (int): The quantity of securities to transact.

#### `startTicker()`

Starts the ticker for real-time data updates.

#### `get_bnf_expiries()`

Retrieves the expiry dates for Bank Nifty derivatives.

#### `get_expiries(derivative_name)`

Retrieves the expiry dates for a specific derivative.

- `derivative_name` (str): The name of the derivative.

#### `get_derivatives_list()`

Retrieves the list of available derivatives.

#### `get_current_expiries(derivative_name)`

Retrieves the current expiry dates for a specific derivative.

- `derivative_name` (str): The name of the derivative.

