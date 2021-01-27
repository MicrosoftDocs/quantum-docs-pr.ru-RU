---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Функция Буларрайаспаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834245"
---
# <a name="boolarrayaspauli-function"></a>Функция Буларрайаспаули

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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