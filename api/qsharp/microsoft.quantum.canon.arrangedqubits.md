---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Функция Арранжедкубитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f3bc4dff73d5ad6393294fc3770b8d36e6094fb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217073"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="58879-102">Функция Арранжедкубитс</span><span class="sxs-lookup"><span data-stu-id="58879-102">ArrangedQubits function</span></span>

<span data-ttu-id="58879-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="58879-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="58879-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="58879-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="58879-105">Размещение элементов управления, целевых объектов и вспомогательных Кубитс в соответствии с индексом</span><span class="sxs-lookup"><span data-stu-id="58879-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="58879-106">Описание</span><span class="sxs-lookup"><span data-stu-id="58879-106">Description</span></span>

<span data-ttu-id="58879-107">Возвращает массив кубит с целевым объектом с индексом 0 и элементом управления i в индексе 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="58879-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="58879-108">Вспомогательные Кубитс вставляются во все остальные позиции в массиве.</span><span class="sxs-lookup"><span data-stu-id="58879-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="58879-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="58879-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="58879-110">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="58879-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="58879-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="58879-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="58879-112">Helper: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="58879-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="58879-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="58879-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

