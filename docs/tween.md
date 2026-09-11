# tween
## easeType
```lua
easeType = {
    "linear",
    "ease_in",
    "ease_out",
    "ease_in_out",
    "quad_in",
    "quad_out",
    "quad_in_out",
    "sine_in",
    "sine_out",
    "sine_in_out",
    "exp_in",
    "exp_out",
    "exp_in_out",
    "back_in",
    "back_out",
    "back_in_out",
    "bounce_in",
    "bounce_out",
    "bounce_in_out",
    "elastic_in",
    "elastic_out",
    "elastic_in_out"
}
```

## tween(GameObject,string key,number duration,number endValue,easeType,listener())
Функция для плавного изменения ключа объекта.
```lua
local a = display:rect(0, 0, 50, 50)
tween(a, "x", 1, 200, "ease_out",function() end)
```