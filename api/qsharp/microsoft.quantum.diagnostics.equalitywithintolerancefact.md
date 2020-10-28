---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: Функция Екуалитивисинтолеранцефакт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712751"
---
# <a name="equalitywithintolerancefact-function"></a>Функция Екуалитивисинтолеранцефакт

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Представляет утверждение, что классическое значение с плавающей запятой имеет ожидаемое значение вплоть до заданного абсолютного допуска.

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a>Входные данные

### <a name="actual--double"></a>фактический: [Double](xref:microsoft.quantum.lang-ref.double)

Число для проверки.


### <a name="expected--double"></a>ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)

Ожидаемое значение.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Абсолютная погрешность разности между фактическим и ожидаемым.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

