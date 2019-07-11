### Cogen

- もっと使ってみる

```scala
import org.scalacheck.ScalacheckShapeless._
import org.scalacheck.Arbitrary.arbitrary

final case class Foo(i: Int, s: String)

arbitrary[Foo].sample
// res0: Option[Foo] = Some(Foo(2147483647,鼟阞龞嬂惇艻㙃尬欦ᮈጪྺﮡЗ諕駵岩⍮緕ᩥ))

final case class Bar(i: Int, foo: Foo)

arbitrary[Bar].sample
// res1: Option[Bar] = Some(Bar(-1735390285,Foo(-670293152,櫌뺘욥郄鼜骇뀔皐ᣩ퉯౒랴蠳둝벆ﾟ䁡⁀崸)))
```
