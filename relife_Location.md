# Параметры конфигурации локаций

## Структура файла

```json
{
    "itemInInvetory": [
        "map"
    ],
    "infoPoints": [
        {
            "name": "Название какого-то места",
            "iconPath": "relife_LocationInfo/images/nearIcon.edds",
            "radiusToCheck": 50,
            "position": [9477.38, 7.79762, 1912.24]
        }
    ]
}
```

## Описание параметров

| Параметр | Тип | Описание | 
|----------|-----|----------|
| `timeNotifyShow` | `int` | Время в секундах на сколько будед показано уведомление | 
| `itemInInvetory` | `array` | Массив предметов, которые должны быть в инвентаре игрока для активации информационных точек |

### Параметры объекта `infoPoint`

| Параметр | Тип | Описание | Пример | Примечания |
|----------|-----|----------|---------|------------|
| `name` | `string` | Название локации или точки интереса | `"Заправочная станция"` | Должно быть уникальным |
| `iconPath` | `string` | Путь к файлу иконки, отображаемой на карте | `"relife_LocationInfo/images/militaryIcon.edds"` | Формат `.edds`, размер 64x64 или 128x128 пикселей |
| `iconPath` | `string` | Путь к файлу иконки, отображаемой на карте | `"relife_LocationInfo/images/militaryIcon.edds"` | Формат `.edds`, размер 64x64 или 128x128 пикселей |
| `iconPath` | `string` | Путь к файлу иконки, отображаемой на карте | `"relife_LocationInfo/images/militaryIcon.edds"` | Формат `.edds`, размер 64x64 или 128x128 пикселей |
| `radiusToCheck` | `number` | Радиус в метрах для взаимодействия с точкой | `50` | 25-50 (малые), 50-100 (средние), 100-200 (большие) |
| `position` | `array[3]` | Координаты точки в формате [X, Y, Z] | `[9477.38, 7.79762, 1912.24]` | X,Z - горизонтальные координаты, Y - высота |

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
