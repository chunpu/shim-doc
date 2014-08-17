_
---

_(value)

`_` is callable, `_(value)` will create a table wraps the given value

```lua
_({1, 0, 2, 4}):sort()
-- → {0, 1, 2, 4}
```

tips:  `a:b(args)` is sugar for `a.b(self, args)`, `self` is a


chain
---

_(value):chain()

make the wrapped table chainable, remember to use `:value()` to get the value you need

```lua
_({1, 0, 2, 4})
    :chain()
    :sort()
    :map(function(x) return x * 2 end)
    :filter(function(x) return x < 6 end)
    :value()
-- → {0, 2, 4}
```