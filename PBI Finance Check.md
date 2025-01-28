---
Class: All
aliases: 
tags: 
created: 2024-01-25T09:12
updated: 2024-11-10T16:13
---
# PBI Finance Check

```
EBIT Total % = 
IF(
    DIVIDE(
        [EBIT Total],
        [PAF Total],
        0
    ) < 0,
    0,
    DIVIDE(
    [EBIT Total],
    [PAF Total],
    0
    )
)
```

```
EBIT Total = 
'3SS'[EBIT 3SS] + '3SS'[EBIT Smartsoft]
```

```
EBIT 3SS = 
CALCULATE(
    '3SS'[3SS Total],
    '3SS All'[Category] = "EBIT 3SS"
)
```

```
EBIT Smartsoft = 
CALCULATE(
    [3SS Total],
    '3SS All'[Category] = "EBIT Smartsoft"
)
```

```
3SS Total = 
SUM('3SS All'[Value])
```

```
PAF Total = 
SUM('PAF All'[Value])
```

