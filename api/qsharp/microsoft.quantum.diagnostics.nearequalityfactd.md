---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Функция Неарекуалитифактд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712653"
---
# <a name="nearequalityfactd-function"></a>Функция Неарекуалитифактд

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Утверждает, что классическое значение с плавающей запятой имеет ожидаемое значение вплоть до маленькой допустимой допускки 1E-10.

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a>Входные данные

### <a name="actual--double"></a>фактический: [Double](xref:microsoft.quantum.lang-ref.double)

Число для проверки.


### <a name="expected--double"></a>ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)

Ожидаемое значение.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Это эквивалентно <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> параметру с жестким отклонением $10 ^ {-10} $.