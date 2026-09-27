# Simulation Results

## Endpoint Verification

### Rs = 250 Ω

| Quantity | Hand calculation | PSpice simulation | Difference |
| --- | ---: | ---: | ---: |
| Vo1 | -0.375 V | -0.37505 V | 0.00005 V |
| Vo2 | -8.000 V | -7.996 V | 0.004 V |

### Rs = 800 Ω

| Quantity | Hand calculation | PSpice simulation | Difference |
| --- | ---: | ---: | ---: |
| Vo1 | -1.200 V | -1.200 V | 0.000 V |
| Vo2 | +8.000 V | +8.002 V | 0.002 V |

## Interpretation

The simulated values are very close to the analytically calculated values.

The small differences are negligible for this design and confirm that the selected resistor values produce the intended resistance-to-voltage conversion at the specified endpoints.

## DC Sweep

The original PSpice analysis file includes a linear DC sweep of the parameter `RS`:

```text
.DC LIN PARAM RS 1 3000 100
```

This allows the output response to be observed as the variable resistance changes.
