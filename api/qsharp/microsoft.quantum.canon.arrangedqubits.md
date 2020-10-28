---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Функция Арранжедкубитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716742"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="426dc-102">Функция Арранжедкубитс</span><span class="sxs-lookup"><span data-stu-id="426dc-102">ArrangedQubits function</span></span>

<span data-ttu-id="426dc-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="426dc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="426dc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="426dc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="426dc-105">Размещение элементов управления, целевых объектов и вспомогательных Кубитс в соответствии с индексом</span><span class="sxs-lookup"><span data-stu-id="426dc-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="426dc-106">Описание</span><span class="sxs-lookup"><span data-stu-id="426dc-106">Description</span></span>

<span data-ttu-id="426dc-107">Возвращает массив кубит с целевым объектом с индексом 0 и элементом управления i в индексе 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="426dc-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="426dc-108">Вспомогательные Кубитс вставляются во все остальные позиции в массиве.</span><span class="sxs-lookup"><span data-stu-id="426dc-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="426dc-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="426dc-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="426dc-110">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="426dc-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="426dc-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="426dc-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="426dc-112">Helper: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="426dc-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="426dc-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="426dc-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

