---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Функция Иснотзеро
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204068"
---
# <a name="isnotzero-function"></a>Функция Иснотзеро

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Проверяет `Double` , не равен ли число приблизительно нулю.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="number--double"></a>число: [Double](xref:microsoft.quantum.lang-ref.double)

Число для проверки



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

Возвращает значение true `number` , если имеет абсолютное значение больше `1e-15` .