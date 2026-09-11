# mouse 
Класс доступный в глобальном пространстве любой сцены.

Методы:
## mouse:getX() -> number
Возвращает позицию мыши x.
```lua
print(mouse:getX())
```

## mouse:getY() -> number
Возвращает позицию мыши Y.
```lua
print(mouse:getY())
```

## mouse:setPosition(number x, number y)
Устанавливает позицию мыши в окне.
```lua
mouse:setPosition(200,200)
```

## mouse:hide()
Метод скрывающий мышь.
```lua
mouse:hide()
```

## mouse:show()
Метод показывающий мышь.
```lua
mouse:show()
```

## mouse:isHidden() -> boolean
Метод возвращающий состояние мыши(видима, невидима)
```lua
print(mouse:isHidden())
```


