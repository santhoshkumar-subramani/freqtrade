# Setup

Freqtrade is a free and open source crypto trading bot written in Python. It is designed to support all major exchanges and be controlled via Telegram or webUI. It contains backtesting, plotting and money management tools as well as strategy optimization by machine learning.

## Get the latest code

```
git clone https://github.com/santhoshkumar-subramani/freqtrade.git

cd freqtrade

./setup.sh -i

source .env/bin/activate

```

To verify freqtrade installed
```
freqtrade --help
```

## Set the configuration environment

**Step 1:** Initialize the user folder
```
freqtrade create-userdir --userdir user_data
```

**Step 2:** Create new configuration file
```
freqtrade new-config --config config.json
```


## Download data from exchange
Add two symbols in config file and then execute the below command to download the data from exchange

```
"pair_whitelist": [
            "BTC/USDT",
            "THT/USDT"
        ],
```

```
freqtrade download-data --config config.json --days 999 -t 5m

-t support following values: 5m, 15m, 30m, 1h, 2h, 4h, 1d, 1w
```

Downaloded data stored in folder 

```
ls user_data/data
binance
(.env) ubuntu@UT-LTP-1162:~/workspace/freqtrade$ ls user_data/data/binance/futures

```

## Minor tweak in config.json for backtesting

![freqtrade](https://raw.githubusercontent.com/freqtrade/freqtrade/quickstart/pairlist_changes.png)
