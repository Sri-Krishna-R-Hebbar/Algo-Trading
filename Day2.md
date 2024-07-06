# Display Settings and Visual Options:

```plaintext
SetChartOptions(flags, addoptions)
```

- **flags:** This parameter sets the primary options for the chart. It is usually set to 0 when no primary flags are needed.
- **addoptions:** This parameter sets additional options for the chart. Multiple options can be combined using the bitwise OR operator (`|`).

## Common Flags and Options

Here are some of the common flags and options that can be used with `SetChartOptions`:

- `chartShowArrows`: Display buy/sell arrows on the chart.
- `chartShowDates`: Display date labels on the X-axis of the chart.
- `chartShowVolume`: Display volume bars on the chart.
- `chartShowGrid`: Display gridlines on the chart.
- `chartShowPrice`: Display price labels on the Y-axis of the chart.
- `chartLogScale`: Use a logarithmic scale for the Y-axis.
- `chartShowInfoPanel`: Display an information panel on the chart.
- `chartShowOHLC`: Display Open, High, Low, and Close values on the chart.

# Formatting Values:

```plaintext
WriteVal(value, format = 1.2, width = 1, maxdigits = -1)
```

`WriteVal` is a function in Amibroker Formula Language (AFL) that converts a numeric value into a formatted string. This function is particularly useful for displaying numerical values on a chart or in the title bar, where you might want to control the number of decimal places, add units, or include other formatting details.

- **value:** The numeric value to be converted into a string.
- **format:** A string specifying the format of the value. It follows the format specification used by the `sprintf` function in C. The default format is "1.2", which means one digit before the decimal point and two digits after the decimal point.
- **width:** The minimum width of the resulting string. If the converted value is shorter than this width, it will be padded with spaces. The default is 1.
- **maxdigits:** The maximum number of significant digits. The default is -1, which means no limit.

# User-Defined Parameters:

```plaintext
Param("name", default_value, min_value, max_value, step)
```

`Param()` is a function in Amibroker Formula Language (AFL) used to create user-defined parameters that can be adjusted via the Parameters window in Amibroker. This allows users to interactively change the values of parameters and see the effect on the chart without modifying the AFL code directly.

- **name:** A string representing the name of the parameter. This name will appear in the Parameters window.
- **default_value:** The default value of the parameter.
- **min_value:** The minimum value of the parameter (optional).
- **max_value:** The maximum value of the parameter (optional).
- **step:** The increment step for the parameter (optional).

# Encoding Colors:
```plaintext
EncodeColor(color)
```

Encoding colors in AFL can be done using predefined constants for common colors or by using the `ColorRGB` and `ColorHSB` functions to create custom colors.

# Ticker Symbol:

```plaintext
Name()
```

`Name()` is a function in Amibroker Formula Language (AFL) that returns the ticker symbol of the security or instrument currently being analyzed. This function is particularly useful for creating custom titles, labels, or annotations on your charts that include the ticker symbol.

# Current Date:

```plaintext
Date()
```

`Date()` is a function in Amibroker Formula Language (AFL) that returns the current date in `YYYYMMDD` format as an integer. This can be useful for displaying the date on your charts or for performing date-based calculations and comparisons.

# Chart Timeframe:

```plaintext
Interval()
```

`Interval()` is a function in AFL that returns the chart's timeframe or interval as a string. This can be useful for adding context to your chart titles or annotations, indicating the timeframe of the data being displayed.