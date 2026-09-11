# sound
Класс доступный в глобальном пространстве любой сцены.

Методы:
## sound:setMasterVolume(number volume(0-1))
Устанавливает громкость звука всей сцены.
```lua
sound:setMasterVolume(0.7)
```

## sound:stopAll()
Останавливает все звуки на сцене.
```lua
sound:stopAll()
```

## sound:closeAll()
Останавливает и выгружает все звуки из памяти.
```lua
sound:closeAll()
```

## sound:create() -> SoundObj
Создаёт и возвращает объект звука для управления.
```lua
local mySound = sound:create()
```

# SoundObj
Класс для управления конкректным звуком.
Свойства: 
```lua
local mySound = sound:create()
mySound.volume = 1 --громкость звука, указывается в диапазоне от 0 до 1
mySound.pitch = 1 --...
```

## SoundObj:load(string pathToSound, boolean isStream)
Загружает звук в оперативную память для последующей работы, если звук короткий `isStream` должен быть `false`, для добавления музыки лучше ставить `true`.
```lua
mySound:load("music.mp3",true)
```

## SoundObj:unload()
Выгружает звук из памяти освобождая место для следующего.
```lua
mySound:unload()
```

## SoundObj:play()
Запускает звук, ВАЖНО:для запуска звук должен быть загружен методом `load`.
```lua
mySound:play()
```

## SoundObj:stop()
Останавливает звук для возможности последующего продолжения проигрывания.
```lua
mySound:stop()
```

## SoundObj:resume()
Возобнавляет воспроизведение остановленного звука.
```lua
mySound:resume()
```

## SoundObj:isPlaying() -> boolean
Возвращает состояние звука, играет - `true` остановлен либо выгружен - `false`.
```lua
if mySound:isPlaying() then
print("great")
else
print("stopped")
end
```

## SoundObj:setVolume(number value(0-1))
Устанавливает громкость звука.
```lua
mySound:setVolume(1)
```


## SoundObj:pause()
Приостанавливает воспроизведение звука.

```lua
mySound:pause()
```
## SoundObj:setPitch(number value)
Устанавливает высоту тона (скорость) воспроизведения звука. Значение по умолчанию — 1.0.

```lua
mySound:setPitch(1.2)
```

## SoundObj:seek(number positionInSeconds)
Перематывает воспроизведение аудиопотока на указанное время в секундах (работает только если isStream равен true).

```lua
mySound:seek(15.5)
```

## SoundObj:getLength() -> number
Возвращает общую длительность аудиозаписи в секундах. Для обычных звуков (isStream = false) возвращает 0.0.

```lua
local totalTime = mySound:getLength()
print("Длительность: " .. totalTime)
```

## SoundObj:getTimePlayed() -> number
Возвращает текущее время воспроизведения в секундах. Для обычных звуков (isStream = false) возвращает 0.0.

```lua
local currentTime = mySound:getTimePlayed()
print("Проиграно: " .. currentTime)
```