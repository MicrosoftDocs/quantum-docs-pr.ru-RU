---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Функция Буларрайаспаули
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c5ef71322dae248fc2c6b1db3adf891de7d72488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713605"
---
# <a name="boolarrayaspauli-function"></a>Функция Буларрайаспаули

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


При наличии битовой строки возвращает оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Оператор Паули для применения к Кубитс, где `bitsApply == bits[idx]` .


### <a name="bitapply--bool"></a>Битаппли: [bool](xref:microsoft.quantum.lang-ref.bool)

применить Паули, если бит — это значение.


### <a name="bits--bool"></a>Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Логический массив.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]



## <a name="remarks"></a>Remarks

Логический массив и регистр такта должны иметь одинаковую длину.