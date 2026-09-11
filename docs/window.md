# window
Класс доступный в глобальном пространстве любой сцены для управления параметрами окна приложения.

Методы:

## window:setWidth(number width)
Устанавливает ширину окна в пикселях.

```lua
window:setWidth(1280)
```

## window:setHeight(number height)
Устанавливает высоту окна в пикселях.

```lua
window:setHeight(720)
```

## window:setSize(number width, number height)
Устанавливает ширину и высоту окна одновременно.

```lua
window:setSize(1920, 1080)
```

## window:getWidth() -> number
Возвращает текущую ширину окна.

```lua
local w = window:getWidth()
```

## window:getHeight() -> number
Возвращает текущую высоту окна.

```lua
local h = window:getHeight()
```

## window:setPosition(number x, number y)
Устанавливает позицию окна на экране монитора по координатам X и Y.

```lua
window:setPosition(100, 100)
```

## window:close()
Закрывает окно приложения.

```lua
window:close()
```