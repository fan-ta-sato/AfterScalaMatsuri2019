### What is Eff?

- __モナドの実行順序を自由に決められる__

```scala
def foo[A, R:_option:_io](a: A) =
  for {
     op <- fromOption(Option(a))
     io <- fromIO(IO(op))
  } yield io

foo(a)
  .runOption
  .runAsync
  .run
```

runIO, runOptionを入れ替えると、実行順序が変更される
