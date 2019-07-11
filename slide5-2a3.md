### What is Eff?

- __様々なモナドを表現/金剛できる__

- 独自に定義したい時はこんな感じにする

```scala
type EitherString[A] = Either[String, A]
type _err[R] = EitherString |= R

type WriterString[A] = Writer[String, A]
type _log[R] = WriterString |= R

type StateInt[A]     = State[Int, A]
trype _count[R] = StateInt |= R
```

- `type _err[R] = EitherString |= R` で"RにEither[String, A]が含まれる"事を示す
   - [MemberImplicits](http://atnos-org.github.io/eff/org.atnos.site.MemberImplicits.html)
