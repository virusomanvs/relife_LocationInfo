# Параметры конфигурации локаций

## Описание параметров

| Параметр | Тип | Описание | 
|----------|-----|----------|
| `timeNotifyShow` | `int` | Время в секундах на сколько будед показано уведомление | 
| `itemInInvetory` | `array` | Массив предметов, которые должны быть в инвентаре игрока для активации информационных точек |

### Параметры объекта `infoPoint`

| Параметр | Тип | Описание |
|----------|-----|----------|
| `name` | `string` | Название локации или точки интереса | 
| `iconPath` | `string` | Путь к файлу иконки, отображаемой на карте |
| `stayVisible` | `bool` | Включить постоянно отображение виджета пока вы находитесь в радиусе действия. Подойдет для сейф зон. | 
| `notifySound` | `string` | Название звука появления виджета. Если написать None то звук не будет воспроизводиться | 
| `layoutPath` | `string` | Путь к виджету если вы хотите сделать свой.| 
| `radiusToCheck` | `number` | Радиус в метрах для взаимодействия с точкой |
| `position` | `array[3]` | Координаты точки в формате [X, Y, Z] |
| `polygonPoints` | `array[ vector ]` | Массив координат фигруы по порядку, без замыкания|

### Параметры объекта `markersList`
| Параметр | Тип | Описание |
|----------|-----|----------|
| `markerTitle` | `string` | Название маркера | 
| `iconPath` | `string` | Путь к файлу иконки, отображаемой на карте |
| `layoutPath` | `string` | Путь к виджету если вы хотите сделать свой.| 
| `markerPosition` | `array[3]` | Координаты точки в формате [X, Y, Z] |
| `distanceMinToHide` | float | Если дистанция игрока до метки меньше чем указано, метка будет скрыта |
| `distanceToShow` | float | Растояние при достижении которого метка будет показана |

"distanceMinToHide": 2,
 "distanceToShow": 0,
                    
### Доступные виджеты для layoutPath у уведомления
| Параметр | Превью | 
|----------|-----|
| `relife_LocationInfo/layout/LocNotificationDanger.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/93e6f5f7-27ed-4482-bc51-3ed939b763ab" />|
| `relife_LocationInfo/layout/LocNotificationSafe.layout` |  <img width="250"  alt="image" src="https://github.com/user-attachments/assets/38e3f808-4be7-414d-ac2e-d5b003bc8a3b" />|
| `relife_LocationInfo/layout/LocNotification.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/f3f58713-1363-4d17-9f88-21c79d8a6a48" /> |
| `relife_LocationInfo/layout/LocNotificationStalkerOld.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/6c882557-1292-482d-a4bd-395a2b5876f4" /> |

