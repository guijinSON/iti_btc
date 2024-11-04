# iti_btc

## Dataset Guidelines
### Available datasets.
1. [BTCUSDT_spot_2017_2024_trades](https://huggingface.co/datasets/amphora/iti-btc) : every `trade` data, total . Collected via `/api/v3/historicalTrades` API endpoint. Including columns: `trade Id, price, qty, quoteQty, time, isBuyerMaker, isBestMatch `
2. [BTCUSDT_spot_2017_2024_1s_klines](https://huggingface.co/datasets/amphora/iti-btc) : `kline` data with 1s interval. Collected via `/api/v3/klines` API endpoint. Including columns: `Open time, Open, High, Low, Close, Volume, Close time, Quote asset volume, Number of trades, Taker buy base asset volume, Taker buy quote asset volume, Ignore`

### How to download
```
from huggingface_hub import snapshot_download
snapshot_download('amphora/iti-btc',local_dir='data')
```
