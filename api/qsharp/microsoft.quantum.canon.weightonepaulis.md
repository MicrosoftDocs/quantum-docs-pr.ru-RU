---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Функция Веигхтонепаулис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715201"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="71dea-102">Функция Веигхтонепаулис</span><span class="sxs-lookup"><span data-stu-id="71dea-102">WeightOnePaulis function</span></span>

<span data-ttu-id="71dea-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="71dea-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="71dea-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="71dea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="71dea-105">Возвращает массив всех операторов Паули веса-1 для заданного числа Кубитс.</span><span class="sxs-lookup"><span data-stu-id="71dea-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="71dea-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="71dea-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="71dea-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="71dea-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="71dea-108">Число Кубитс, для которых определены возвращаемые операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="71dea-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="71dea-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="71dea-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="71dea-110">Массив операторов кубит Паули, каждый из которых представлен в виде массива с длиной `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="71dea-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>