# KOTAK NEO PYTHON API

## Kotak Neo Class

### Initialize the class

```python-repl
data ={

    "username":"kotak_username",

    "consumer_key":"consumer key here",

    "consumer_secret":"consumer secret here",

    "mobile_number":"123456789",

    "password":"password here",

    "mpin":"123456"}

    kotak=KotakNeo(consumer_key=data["consumer_key"],consumer_secret=data["consumer_secret"],username=data['username'],mobile_number=data["mobile_number"],password=data["password"],mpin=data['mpin'])
```

### Get Tokens

```python-repl
kotak.get_tokens()
```

### Place Order

```python-repl
order_data = kotak.place_order(after_market="NO", dq="0", market_protection="0", position_square_off_flag="N",

    price="0", trigger_price="0",

    exchange_segment="nse_cm", product_code="NRML", quantity="1", order_duration="DAY",

    transacation_type="B", order_type="L", trading_symbol="TCS-EQ",sid=None, token=None, authorization=None)

```

### Modify Order

```python-repl
modify_order(order_no,price="0",validity="DAY",trading_symbol="TCS-EQ",transaction_type="B",     trigger_price="0",quantity="1",exchange="nse_cm",order_type="L",disclosed_quantity="0",product_code="NRML")
```

### Cancel Order

```python-repl
kotak.cancel_order(order_no,amo="NO",trading_symbol="")
```

### Order Book

```python-repl
kotak.order_book()
```

### Order History

```python-repl
kotak.order_history(order_no="")
```

### Trade Book

```python-repl
kotak.trade_book()
```

### Position

```python-repl
kotak.position()
```

### Limits

```python-repl
kotak.limits(segment="CASH",exchange="NSE",prod="ALL")
```

### Margin

```python-repl
kotak.margin(exchange="nse_cm",price="0",order_type="L",product_type="CNC",quantity='1',transaction_type="B")
```
