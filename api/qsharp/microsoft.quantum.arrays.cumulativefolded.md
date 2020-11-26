---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Функция Кумулативефолдед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: ffb934d06f6be06cbc35a523c90d2c54e0a51353
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210035"
---
# <a name="cumulativefolded-function"></a>Функция Кумулативефолдед

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Объединяет сопоставленные и объединенные в одну функцию

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a>Описание

Эта функция выполняет итерацию `fn` функции через массив, начиная с начального состояния `state` и возвращающего все промежуточные значения, не включая начальное состояние.

## <a name="input"></a>Входные данные

### <a name="fn--statet---state"></a>FN: (' State, t)-> ' State

Функция, которая должна быть свернута в массиве


### <a name="state--state"></a>состояние: "состояние

Начальное состояние, которое должно быть сведено


### <a name="array--t"></a>массив: 'T []

Массив значений для свертывания



## <a name="output--state"></a>Выходные данные: "State []

Все промежуточные состояния, включая конечное состояние, но не начальное состояние.
Длина выходного массива равна длине `array` .

## <a name="type-parameters"></a>Параметры типа

### <a name="state"></a>"State

Тип состояний, `fn` в которых работает функция, т. е. принимает в качестве первого входа и возвращает.
### <a name="t"></a>Е

Тип `array` элементов.