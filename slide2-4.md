### Shrinking

- Shrinkする場合は、テスト回数は余計に実行される。  
深くネストしたり、再起データはメモリ食いつぶしたり、時間がかかるので 
以下のようにShrinkさせない手もある

```scala
forAllNoShrink(Gen.listOfN(5, Gen.choose(0, 10))){ls =>
  ls == ls.reverse
}.check
! Falsified after 0 passed tests.
> ARG_0: List("0", "9", "7", "4", "5")
```
