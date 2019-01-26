# Dziban

**THIS IS A WORK IN PROGRESS**

## How it works

There are two ways of using Dziban.

1. Recommendations
2. Strict Specification

### Recommendations

```
r = Rec().encoding({ x: { field: 'Horsepower' }, y: { field: 'Acceleration' } }).build()
```

This will perform the following steps.

1) Generate a Draco specification from the information provided by this partial spec.

```
encoding(e0).
:- not field(e0, 'Horsepower').

encoding(e1).
:- not field(e1, 'Acceleration').
```

2) Run Draco on the query and converting the result into a VegaLite specification

3) Render the result

### Strict Specification
