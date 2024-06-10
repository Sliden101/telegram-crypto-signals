# Telegram Crypto Signals

Telegram Crypto Signals is a command line tool that automates your crypto currency Technical Analysis (TA).

It is based on [Crypto Signals] https://github.com/CryptoSignal/crypto-signal , so I recommend you to take a look in that proyect to known what is it.

Main differences vs original Crypto Signals:
- Focused 100% to interact with a Telegram Bot
- Using your Telegram Bot you can change the initial configuration. You can add/remove market pairs, enable/disable indicators at a specific period, and you can set the timeout which the analysis are executed.
- It creates candle bar charts with MAs, RSI and MACD. Those images are sending as part of the Telegram notification.

## Installing And Running
The commands listed below are intended to be run in a terminal.

1. Clone this repo

1. Create a config.yml file and put it into "app" folder.

1. Build your own image, for example `docker build -t sliden/telegram-crypto-signals:latest .`

1. For testing and debugging run `docker run --rm -ti -v  $PWD/app:/app sliden/telegram-crypto-signals:latest`

1. For production run in daemon mode `docker run --rm -di -v  $PWD/app:/app sliden/telegram-crypto-signals:latest`

## Interacting with Telegram Bot
From your chat bot you can use the following commands. The most important is "/timeout" to set the update interval. Value is given in seconds.

To run analysis every 10 minutes. <br />
`/timeout 600` <br />

Basic help to know available commands <br />
`/help` <br />

Disable or re-enable any indicators initially registered in config.yml <br />
`/indicators` <br />
`/indicator rsi disable 15m` <br />
`/indicator rsi enable 15m` <br />

### Configuring config.yml

For a list of all possible options for config.yml and some example configurations look [here](docs/config.md)

# FAQ and Common Questions

Refer to original [Crypto Signals]https://github.com/CryptoSignal/crypto-signal

# Liability
I am not your financial adviser, nor is this tool. Use this program as an educational tool, and nothing more. None of the contributors to this project are liable for any losses you may incur. Be wise and always do your own research.
