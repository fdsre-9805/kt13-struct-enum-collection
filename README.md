# КТ №13 — Коллекция структур и перечисления

**Вариант 2 — RPG-предмет**

Структура `Item`, объединяющая два перечисления (`ItemRarity`, `ItemSlot`), с переопределённым `ToString()`.
Демонстрация value-семантики при чтении элемента массива в локальную переменную и разбор строки через `Enum.TryParse`.

## Файлы

- `Item.cs` — перечисления `ItemRarity`, `ItemSlot` и структура `Item`
- `Program.cs` — точка входа и демонстрация

## Запуск

```
dotnet run
```

## Проверочные ключи

| Действие | Ожидаемый результат |
|---|---|
| `items[0]` (до изменения копии) | `Daedalus (Legendary, Weapon)` |
| копия `items[0]`, `Rarity` копии изменена на `Common` | копия — `Daedalus (Common, Weapon)`, `items[0]` — без изменений |
| `Enum.TryParse<ItemRarity>("Epic", out var r)` | `true`, `r == ItemRarity.Epic` |
| `Enum.TryParse<ItemRarity>("Mythic", out var r)` | `false`, без исключения |
