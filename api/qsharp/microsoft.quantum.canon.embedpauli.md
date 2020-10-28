---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Функция Ембедпаули
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: c78406aa4557834ac2bb40cf1847696d075e5135
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716196"
---
# <a name="embedpauli-function"></a>Функция Ембедпаули

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии однокубитного оператора Паули и индекса кубит возвращает оператор Multi-кубит Паули с заданным оператором Single-кубит в этом индексе и `PauliI` в каждом другом индексе.

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Оператор кубит Паули, помещаемый в заданное место.


### <a name="location--int"></a>Расположение: [int](xref:microsoft.quantum.lang-ref.int)

Индекс `output[location] == pauli` , где `output` — это выходные данные этой функции.


### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Длина возвращаемого массива.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

