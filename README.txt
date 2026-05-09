AI Quant Bot update

Что добавлено:
1. Каскад данных свечей: Binance -> Bybit -> MEXC.
2. Каскад futures context: funding, open interest, стакан/orderbook по Binance -> Bybit -> MEXC.
3. Реальный orderbook imbalance: bid/ask imbalance, notional imbalance, spread.
4. Long/Short ratio: Binance globalLongShortAccountRatio и Bybit account-ratio, если endpoint доступен.
5. Crowd/Squeeze analyzer: определяет перегруз толпы в LONG/SHORT, риск long squeeze / short squeeze и направление smart money/squeeze bias.
6. Walk-forward backtest: дополнительная проверка по последовательным окнам + stability.
7. News risk hook: можно поставить переменную NEWS_RISK=high перед CPI/FOMC/NFP/Fed, чтобы бот снижал confidence.
8. Отчёт теперь показывает источник свечей и источник контекста отдельно.
9. В отчёт добавлены Funding, Long/Short ratio, Smart money / squeeze bias.

Запуск:
export TELEGRAM_BOT_TOKEN='ВАШ_ТОКЕН'
python bot.py

Опционально перед важными новостями:
export NEWS_RISK=high
