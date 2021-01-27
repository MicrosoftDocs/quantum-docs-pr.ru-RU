---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Функция Веигхтонепаулис
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 8aeea795ef5409339e8a1b39c3ffcfaf29d675b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851968"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="e9418-102">Функция Веигхтонепаулис</span><span class="sxs-lookup"><span data-stu-id="e9418-102">WeightOnePaulis function</span></span>

<span data-ttu-id="e9418-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e9418-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e9418-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e9418-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e9418-105">Возвращает массив всех операторов Паули веса-1 для заданного числа Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e9418-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="e9418-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e9418-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="e9418-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e9418-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e9418-108">Число Кубитс, для которых определены возвращаемые операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="e9418-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="e9418-109">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="e9418-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="e9418-110">Массив операторов кубит Паули, каждый из которых представлен в виде массива с длиной `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="e9418-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>