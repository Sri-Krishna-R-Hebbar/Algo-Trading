## MA Buy and Sell Strategy

```plaintext
_SECTION_BEGIN("MA Buy and Sell Strategy");

shortPeriod = 50;
longPeriod = 200;

shortMA = MA(Close, shortPeriod);
longMA = MA(Close, longPeriod);

Plot(shortMA, "Short MA", colorBlue, styleLine);
Plot(longMA, "Long MA", colorRed, styleLine);

buySignal = Cross(shortMA, longMA);
sellSignal = Cross(longMA, shortMA);
Buy = buySignal;
Sell = sellSignal;

PlotShapes(IIf(Buy, shapeSmallUpTriangle, shapeNone), colorYellow, layer = 0, yposition = Low, offset = -30);
PlotShapes(IIf(Sell, shapeSmallDownTriangle, shapeNone), colorAqua, layer = 0, yposition = Low, offset = -30);

_SECTION_END();
```

**Explanation:**
- **shortPeriod**: The period for the short moving average (set to 50).
- **longPeriod**: The period for the long moving average (set to 200).
- **shortMA**: Calculates the short moving average based on the close prices and the short period.
- **longMA**: Calculates the long moving average based on the close prices and the long period.
- **Plot(shortMA, "Short MA", colorBlue, styleLine)**: Plots the short moving average as a blue line.
- **Plot(longMA, "Long MA", colorRed, styleLine)**: Plots the long moving average as a red line.
- **buySignal**: Generates a buy signal when the short moving average crosses above the long moving average.
- **sellSignal**: Generates a sell signal when the short moving average crosses below the long moving average.
- **Buy**: Sets the buy condition to the buy signal.
- **Sell**: Sets the sell condition to the sell signal.
- **PlotShapes(IIf(Buy, shapeSmallUpTriangle, shapeNone), colorYellow, layer = 0, yposition = Low, offset = -30)**: Plots a small yellow up triangle at the low price when a buy signal is generated.
- **PlotShapes(IIf(Sell, shapeSmallDownTriangle, shapeNone), colorAqua, layer = 0, yposition = Low, offset = -30)**: Plots a small aqua down triangle at the low price when a sell signal is generated.

---