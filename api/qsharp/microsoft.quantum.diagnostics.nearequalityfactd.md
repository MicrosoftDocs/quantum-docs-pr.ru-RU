---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: Функция Неарекуалитифактд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: d632a7a12c9ebbebfbc7939f2b8a24de8ae1ba2a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827897"
---
# <a name="nearequalityfactd-function"></a>Функция Неарекуалитифактд

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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