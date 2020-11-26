---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Функция Ембедпаули
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: e9042ca9eac4b8791057037dc5698eb14deadd31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207043"
---
# <a name="embedpauli-function"></a><span data-ttu-id="72da4-102">Функция Ембедпаули</span><span class="sxs-lookup"><span data-stu-id="72da4-102">EmbedPauli function</span></span>

<span data-ttu-id="72da4-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="72da4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="72da4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72da4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72da4-105">При наличии однокубитного оператора Паули и индекса кубит возвращает оператор Multi-кубит Паули с заданным оператором Single-кубит в этом индексе и `PauliI` в каждом другом индексе.</span><span class="sxs-lookup"><span data-stu-id="72da4-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="72da4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="72da4-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="72da4-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="72da4-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="72da4-108">Оператор кубит Паули, помещаемый в заданное место.</span><span class="sxs-lookup"><span data-stu-id="72da4-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="72da4-109">Расположение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="72da4-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="72da4-110">Индекс `output[location] == pauli` , где `output` — это выходные данные этой функции.</span><span class="sxs-lookup"><span data-stu-id="72da4-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="72da4-111">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="72da4-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="72da4-112">Длина возвращаемого массива.</span><span class="sxs-lookup"><span data-stu-id="72da4-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="72da4-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="72da4-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

