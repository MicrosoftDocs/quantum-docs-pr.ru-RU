---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Функция Арранжедкубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841081"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="ef5a5-102">Функция Арранжедкубитс</span><span class="sxs-lookup"><span data-stu-id="ef5a5-102">ArrangedQubits function</span></span>

<span data-ttu-id="ef5a5-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ef5a5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef5a5-105">Размещение элементов управления, целевых объектов и вспомогательных Кубитс в соответствии с индексом</span><span class="sxs-lookup"><span data-stu-id="ef5a5-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="ef5a5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ef5a5-106">Description</span></span>

<span data-ttu-id="ef5a5-107">Возвращает массив кубит с целевым объектом с индексом 0 и элементом управления i в индексе 2 ^ i.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="ef5a5-108">Вспомогательные Кубитс вставляются во все остальные позиции в массиве.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="ef5a5-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ef5a5-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="ef5a5-110">элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ef5a5-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="ef5a5-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="ef5a5-112">Helper: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ef5a5-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="ef5a5-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ef5a5-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

