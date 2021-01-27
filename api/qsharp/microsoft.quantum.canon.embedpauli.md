---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Функция Ембедпаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: 0e6a93e22ee495abcc44bdf522e7c72c0981308b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840540"
---
# <a name="embedpauli-function"></a>Функция Ембедпаули

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Пример

Чтобы получить массив, `[PauliI, PauliI, PauliX, PauliI]` сделайте следующее:

```qsharp
EmbedPauli(PauliX, 2, 3);
```