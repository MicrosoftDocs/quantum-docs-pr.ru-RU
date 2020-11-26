---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Функция Веигхтонепаулис
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 904c606393131d51eaa44d464ad52bec509eaf72
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204544"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="19912-102">Функция Веигхтонепаулис</span><span class="sxs-lookup"><span data-stu-id="19912-102">WeightOnePaulis function</span></span>

<span data-ttu-id="19912-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="19912-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="19912-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="19912-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="19912-105">Возвращает массив всех операторов Паули веса-1 для заданного числа Кубитс.</span><span class="sxs-lookup"><span data-stu-id="19912-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="19912-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="19912-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="19912-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="19912-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="19912-108">Число Кубитс, для которых определены возвращаемые операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="19912-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="19912-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="19912-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="19912-110">Массив операторов кубит Паули, каждый из которых представлен в виде массива с длиной `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="19912-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>