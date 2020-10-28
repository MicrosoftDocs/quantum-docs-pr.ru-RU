---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Функция Кумулативефолдед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: a09c2779c8f06d8f6b7b0902366f3cefbbca4525
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730368"
---
# <a name="cumulativefolded-function"></a>Функция Кумулативефолдед

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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