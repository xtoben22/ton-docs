# 注释
FunC 有单行注释，以 `;;`（双分号）开始。例如：
```func
int x = 1; ;; 给 x 赋值 1
```

它还有多行注释，以 `{-` 开始并以 `-}` 结束。请注意，与许多其他语言不同的是，FunC 的多行注释可以嵌套。例如：
```func
{- 这是一个多行注释
    {- 这是注释中的注释 -}
-}
```

此外，多行注释中可以有单行注释，且单行注释 `;;` 比多行注释 `{- -}`“更强”。换句话说，在以下示例中：

```func
{-
  注释开始

;; 这个注释的结束本身被注释掉了 -> -}

const a = 10;
;; 这个注释的开始本身被注释掉了 -> {-

  注释结束
-}
```

`const a = 10;` 在多行注释内，因此被注释掉了。