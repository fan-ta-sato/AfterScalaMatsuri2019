### Cogen

- 具体的にどう使う？

```scala
import org.scalacheck.Arbitrary.arbitrary

arbitrary[String => Int].sample.get("a")
res31: Int = 0

arbitrary[String => Int].sample.get("a")
res32: Int = -766313279

arbitrary[String => Int].sample.get("a")
res33: Int = 250552836
```
