### What is Property Base Test?

```scala
forAll{(x: Float, y: Float, z: Float) =>
  (x * y) * z == x * (y * z)
}.check 
```
