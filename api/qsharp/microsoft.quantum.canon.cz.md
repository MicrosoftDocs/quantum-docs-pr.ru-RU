---
uid: Microsoft.Quantum.Canon.CZ
title: Операция CZ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 419082dbf8f96a9fe2dfabeab77e1823cb59a8f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207213"
---
# <a name="cz-operation"></a><span data-ttu-id="f7870-102">Операция CZ</span><span class="sxs-lookup"><span data-stu-id="f7870-102">CZ operation</span></span>

<span data-ttu-id="f7870-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f7870-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f7870-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7870-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f7870-105">Применяет шлюз с управляемым Z (CZ) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="f7870-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="f7870-106">$ $ \бегин{алигн} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 0 & 0 &-1 \енд{алигн}, $ $ где строки и столбцы упорядочены как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="f7870-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f7870-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f7870-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="f7870-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f7870-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f7870-109">Управление кубит для шлюза CZ.</span><span class="sxs-lookup"><span data-stu-id="f7870-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f7870-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f7870-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f7870-111">Целевой кубит для шлюза CZ.</span><span class="sxs-lookup"><span data-stu-id="f7870-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7870-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7870-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f7870-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7870-113">Remarks</span></span>

<span data-ttu-id="f7870-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="f7870-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```