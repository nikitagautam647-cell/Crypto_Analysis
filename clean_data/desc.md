This file includes the measures and DAX formulas used during the project.

Examples
========

Momentum Score
--------------

```dax
Momentum Score =
VAR M = [Growth Momentum]
RETURN
SWITCH(
    TRUE(),
    ISBLANK(M), BLANK(),
    M >= 0.50, 100,
    M >= 0.20, 80,
    M >= 0.00, 60,
    M >= -0.20, 40,
    M >= -0.50, 20,
    10
)
```

Momentum Rating
---------------

```dax
Momentum Rating =
VAR M = [Growth Momentum]
RETURN
SWITCH(
    TRUE(),
    ISBLANK(M), "No Data",
    M >= 0.50, "Strong Uptrend",
    M >= 0.20, "Moderate Uptrend",
    M >= 0.00, "Sideways/Stable",
    M >= -0.20, "Weak Downtrend",
    "Strong Downtrend / Reversal Risk"
)
```

Forecast Price
--------------

```dax
forecast price =
VAR day = SELECTEDVALUE(FORECASTDATE[LABEL])
RETURN
SWITCH(
    day,
    "7 day ago", [PAST PROCE 7D],
    "today", SELECTEDVALUE(CRIPTO[current_price]),
    "7 days ahead", [FUTURE PRICE 7D],
    BLANK()
)
```