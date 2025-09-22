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
| `notifySound` | `string` | Название звука появления виджета | 
| `layoutPath` | `string` | Путь к виджету если вы хотите сделать свой. По умолчанию есть 3 виджета.| 
| `radiusToCheck` | `number` | Радиус в метрах для взаимодействия с точкой |
| `position` | `array[3]` | Координаты точки в формате [X, Y, Z] |

### Доступные виджеты для layoutPath
| Параметр | Превью | 
|----------|-----|
| `relife_LocationInfo/layout/LocNotificationDanger.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/93e6f5f7-27ed-4482-bc51-3ed939b763ab" />|
| `relife_LocationInfo/layout/LocNotificationSafe.layout` |  <img width="250"  alt="image" src="https://github.com/user-attachments/assets/38e3f808-4be7-414d-ac2e-d5b003bc8a3b" />|
| `relife_LocationInfo/layout/LocNotification.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/f3f58713-1363-4d17-9f88-21c79d8a6a48" /> |

## Пример использования

```json
{
    "itemInInvetory": [],
    "infoPoints": [
        {
            "name": "Станция Переработки Отходов 1",
            "iconPath": "relife_LocationInfo/images/nearIcon.edds",
            "radiusToCheck": 50,
            "position": [
                9477.14, 7.74701, 1916.17
            ]
        },
        {
            "name": "Лагерь Кумырна",
            "iconPath": "relife_LocationInfo/images/nearIcon.edds",
            "radiusToCheck": 10,
            "stayVisible": 1,
            "notifySound": "locShowNotifySafe_SoundSet",
            "layoutPath": "relife_LocationInfo/layout/LocNotificationSafe.layout",
            "position": [
                9490.71, 7.989, 1916.28
            ]
        },
        {
            "name": "Дом с призраками",
            "iconPath": "relife_LocationInfo/images/nearIcon.edds",
            "radiusToCheck": 15,
            "stayVisible": 1,
            "notifySound": "locShowNotifyDanger_SoundSet",
            "layoutPath": "relife_LocationInfo/layout/LocNotificationDanger.layout",
            "position": [
                9489.77, 8.17192, 1860.17
            ]
        }
    ]
}
```
