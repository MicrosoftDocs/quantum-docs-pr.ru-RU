---
uid: Microsoft.Quantum.Canon.CZ
title: Операция CZ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: bc38cd43a0dcaf7aea735ef6468a394e91c85593
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716349"
---
# <a name="cz-operation"></a><span data-ttu-id="39e9c-102">Операция CZ</span><span class="sxs-lookup"><span data-stu-id="39e9c-102">CZ operation</span></span>

<span data-ttu-id="39e9c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="39e9c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="39e9c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39e9c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39e9c-105">Применяет шлюз с управляемым Z (CZ) к паре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="39e9c-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="39e9c-106">$ $ \бегин{алигн} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 0 & 0 &-1 \енд{алигн}, $ $ где строки и столбцы упорядочены как в разделе "Основные понятия о такте".</span><span class="sxs-lookup"><span data-stu-id="39e9c-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="39e9c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="39e9c-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="39e9c-108">элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="39e9c-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="39e9c-109">Управление кубит для шлюза CZ.</span><span class="sxs-lookup"><span data-stu-id="39e9c-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="39e9c-110">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="39e9c-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="39e9c-111">Целевой кубит для шлюза CZ.</span><span class="sxs-lookup"><span data-stu-id="39e9c-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39e9c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39e9c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="39e9c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="39e9c-113">Remarks</span></span>

<span data-ttu-id="39e9c-114">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="39e9c-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```