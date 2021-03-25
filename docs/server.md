# Описание возращаемого JSON объекта

Результат представляется с помощью параметров:

- energyIn - содержит информацию о полученные калориях
- energyOut - содержит информацию о потраченных калориях
- heartRate - содержит информацию о пульсе человека
- steps - содержит информацию о количестве шагов
- pfcInfo - содержит информацию о полученных белках, жирах и углеводах
- weight - содержит информацию о весе пользователя
- standard - содержит значения норм по различным параметрам для пользователя
- user - содержит информацию о пользователе


## Описание параметров возвращаемого объекта
**x**  - номер дня, **y** - значение параметра за день, description -  содержит в себе информацию о времени подсчете параметра и значение параметра в определенное время. Например, в **energyIn** **y** отвечает за количество усвоенных каллорий за день, а **description** хранит какое количество каллорий усвоилось в определенный момент времени .
_____
```json
"energyIn": {
      number:
      [{"x": number, "y":number, "description": [EnergyInDescription]}]
}
```
```json
 EnergyInDescription: {
      "x": number, "y":number, "pulse":number
}
```
```json
"energyOut": {
      number:
      ["x": number, "y":number, "description":[energyInDescription]}]
}
```
```json
energyInDescription : {
      "x": number, "y":number, "pulse":number
}
```
```json
"heartRate": {
      number:
      [{"x": number, "y":number, "description": [heartRateDescription]}]
}
```
```json
heartRateDescription : {
      "x": number, "y":number
}
```
```json
 "pfcInfo": {
      number:
      [{"x": number, "y":number, "description":  [pfcInfoDescription]}]
}
```
```json
pfcInfoDescription : {
      "x": number, "proteinIn": number, "cbhIn": number, "fatIn": number
}
```
```json
"weight": {
      number:
      [{"x": number, "y":number, "description":  any]
}
```
```json
"user": {
      "height": number, "birthdayDay": number, "birthdayMonth": number, "birthdayYear": number,  "stepLenght": number, "sex": bool
}
```


# Описание методов, получающих необходимые данные
| Метод | Описание |  
| ------ | ------ |
|parseShortSummary| Метод считает количество потраченных и усвоенных каллорий, пульс и количество шагов из short_summary |
| parseFullSummary| Метод считает количество усвоенных белков, жиров и углеводов |
| parseWeight | Метод считывает вес пользователя |
| parseUserInfo | Метод считывает информацию о пользователе |
