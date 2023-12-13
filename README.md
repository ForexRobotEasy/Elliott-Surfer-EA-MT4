# Elliott Surfer EA MT4

This code is for the Elliott Surfer EA (Expert Advisor) for the MetaTrader 4 platform. The EA is designed to automatically trade the forex market based on the Elliott Wave theory.

## Developer's Site

Forex Robot Easy Team is the development team behind this EA. For detailed reviews and trading results of this product, please visit the [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/elliott-surfer-ea-mt4-review-black-friday-special/) website.

## Functionality

The Elliott Surfer EA uses the following libraries:

- Trade.mqh: This library provides functions for opening, modifying, and closing trades.
- PositionInfo.mqh: This library provides functions for retrieving information about open positions.

The EA has the following configurable parameters:

- StopLoss: The stop loss value in pips.
- TakeProfit: The take profit value in pips.
- RiskPercentage: The risk percentage per trade.
- MagicNumber: A unique identifier for trades.

The trade object is initialized using the CTrade class.

The EA's main logic is implemented in the OnTick() function, which is called on each tick of the market. The function checks if there are any open positions using the PositionInfo.Total() function. If there are no open positions, the EA proceeds to place a new trade.

The EA first retrieves the current market price using SymbolInfo.Double() and calculates the lot size based on the risk percentage and available margin. It then calculates the stop loss and take profit levels based on the current price and the configured stop loss and take profit values.

Finally, the EA places a new trade using the trade.Buy() function, specifying the lot size, symbol, stop loss level, take profit level, and magic number.

The EA also includes an OnInit() function that returns INIT_SUCCEEDED to indicate successful initialization, and an OnDeinit() function that is called when the EA is removed from the chart. The OnDeinit() function closes any open positions using the trade.CloseAll() function.

Please note that Forex Robot Easy is not the official developer of this product. We are only providing a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.
