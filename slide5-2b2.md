### What is Eff?

- __モナドの合成が高速__

- こんな感じで合成できる

```scala
// 意味のない関数だ・・・
def foo[A, R:_option:_io](a: A) =
  for {
     op <- fromOption(Option(a))
     io <- fromIO(IO(op))
  } yield io
```
