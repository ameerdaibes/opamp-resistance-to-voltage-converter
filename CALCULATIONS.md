# Hand Calculations

## Given Design Targets

```text
Vs1 = 1.5 V
Vs2 = 5 V
Rs(min) = 250 Ω
Rs(max) = 800 Ω
Vo2(min) = -8 V
Vo2(max) = +8 V
```

## Stage 1

The first stage is an inverting amplifier.

```text
Vo1 = -(Rf / Ri) Vs1
```

where:

```text
Rf = Rs
Ri = 1 kΩ
```

Therefore:

```text
Vo1 = -(Rs / 1 kΩ)(1.5 V)
```

### At Rs = 250 Ω

```text
Vo1 = -(250 / 1000)(1.5)
Vo1 = -0.375 V
```

### At Rs = 800 Ω

```text
Vo1 = -(800 / 1000)(1.5)
Vo1 = -1.200 V
```

## Stage 2

The second stage is an inverting summing amplifier with a 10 kΩ feedback resistor.

```text
Vo2 = -[(10 kΩ / R1)Vo1 + (10 kΩ / R2)Vs2]
```

### Condition 1

For:

```text
Rs = 250 Ω
Vo1 = -0.375 V
Vo2 = -8 V
```

the equation becomes:

```text
8 × 10^-4 = -0.375/R1 + 5/R2
```

### Condition 2

For:

```text
Rs = 800 Ω
Vo1 = -1.200 V
Vo2 = +8 V
```

the equation becomes:

```text
8 × 10^-4 = 1.2/R1 - 5/R2
```

Adding the two equations:

```text
1.6 × 10^-3 = 0.825/R1
```

so:

```text
R1 = 515.625 Ω
```

Substituting back gives:

```text
R2 ≈ 3273.8 Ω
```

## Final Design Values

```text
R1 = 515.625 Ω
R2 ≈ 3.274 kΩ
Feedback resistor of stage 2 = 10 kΩ
```
