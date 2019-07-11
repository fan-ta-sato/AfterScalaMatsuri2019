### Shrinking

- 具体的に

```scala
forAll{(x: Float, y: Float, z: Float) =>
   (x * y) * z == x * (y * z)
}.check 
! Falsified after 0 passed tests.
> ARG_0: 0.0                        // <- Shrink
> ARG_0_ORIGINAL: -4.3700225E23
> ARG_1: -369.42963                 // <- Shrink
> ARG_1_ORIGINAL: -3.8368965E-26
> ARG_2: 1.0031137E36               // <- Shrink
> ARG_2_ORIGINAL: 5.2317635E12
```
