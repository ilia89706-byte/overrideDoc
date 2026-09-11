# events

## events:call(string event)
Вызывает ивент прикреплённый к чему либо.
```lua
local a = display:circle(0, 0, 50)
a:on("test", function()
	a:remove()
end)
events:call("test")
```