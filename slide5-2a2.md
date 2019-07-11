### What is Eff?

- __様々なモナドを表現/混合できる__

```scala
def foo[A, R:_option:_io](...
```

- こんな感じで書けば`R`はOptionとIOを統合したモナドとして扱える
