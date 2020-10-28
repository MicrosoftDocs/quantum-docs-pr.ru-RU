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
# <a name="embedpauli-function"></a><span data-ttu-id="c6441-102">Функция Ембедпаули</span><span class="sxs-lookup"><span data-stu-id="c6441-102">EmbedPauli function</span></span>

<span data-ttu-id="c6441-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c6441-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c6441-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6441-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6441-105">При наличии однокубитного оператора Паули и индекса кубит возвращает оператор Multi-кубит Паули с заданным оператором Single-кубит в этом индексе и `PauliI` в каждом другом индексе.</span><span class="sxs-lookup"><span data-stu-id="c6441-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="c6441-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c6441-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="c6441-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="c6441-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="c6441-108">Оператор кубит Паули, помещаемый в заданное место.</span><span class="sxs-lookup"><span data-stu-id="c6441-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="c6441-109">Расположение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6441-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c6441-110">Индекс `output[location] == pauli` , где `output` — это выходные данные этой функции.</span><span class="sxs-lookup"><span data-stu-id="c6441-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="c6441-111">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6441-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c6441-112">Длина возвращаемого массива.</span><span class="sxs-lookup"><span data-stu-id="c6441-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="c6441-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="c6441-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

