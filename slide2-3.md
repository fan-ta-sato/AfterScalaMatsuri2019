### Shrinking

- もっと具体的に

```scala
forAll(Gen.listOfN(5, Gen.choose(0, 10))){ls =>
 ls == ls.reverse
}.check
! Falsified after 0 passed tests.
> ARG_0: List("0", "1")                      // <- Shrink
> ARG_0_ORIGINAL: List("2", "10", "9", "5", "7")
```
