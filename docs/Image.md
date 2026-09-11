# GameObject/Image
Изображение.
Свойства:
```lua
local a = display:image("path/to/image",0,0,100,100)
a.x = 0 --позиция x
a.y = 0 --позиция y
a.width = 100 --ширина отображаемого изображения
a.height = 100 --высота отображаемого изображения
--== Остальные свойства унаследованы от GameObject --==
``` 
Методы: 
## setTexture(string path)
Устанавливает новую текстуру для текущего изображения.
```lua
local a = display:image("dog.png",0,0,100,100)
a:setTexture("cat.png")
```

## setFilter(int type)
Устанавливает фильтр отображения изображения, 1 - linear, 0 - nearest
```lua
local a = display:image("myPixelSprite.png",0,0,100,100)
a:setFilter(0)
```