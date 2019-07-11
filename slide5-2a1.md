### What is Eff?

- __様々なモナドを表現/混合できる__

- 例えばOptionとIOを組み合わせたモナドが簡単に定義できる

- こんな感じでimportして

```scala
import cats._, data._
import cats.effect.IO
import cats.implicits._
import org.atnos.eff._
import org.atnos.eff.all._
import org.atnos.eff.syntax.all._
import org.atnos.eff.addon.cats.effect._
import org.atnos.eff.syntax.addon.cats.effect._
import org.atnos.eff.addon.cats.effect.IOEffect._
```
