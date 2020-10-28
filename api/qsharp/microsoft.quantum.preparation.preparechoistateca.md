---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateCA
title: Операция Препаречоистатека
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateCA
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.
ms.openlocfilehash: b9d2cdaea1ebc957719d92bf12901c54a55a56aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709447"
---
# <a name="preparechoistateca-operation"></a><span data-ttu-id="ea837-102">Операция Препаречоистатека</span><span class="sxs-lookup"><span data-stu-id="ea837-102">PrepareChoiStateCA operation</span></span>

<span data-ttu-id="ea837-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="ea837-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="ea837-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ea837-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ea837-105">Подготавливает состояние Чои – Жамиłковски для заданной операции с управляемыми и соседними вариантами на заданный эталонный и целевой регистры.</span><span class="sxs-lookup"><span data-stu-id="ea837-105">Prepares the Choi–Jamiłkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiStateCA (op : (Qubit[] => Unit is Adj + Ctl), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="ea837-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ea837-106">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="ea837-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="ea837-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="reference--qubit"></a><span data-ttu-id="ea837-108">Ссылка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ea837-108">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="ea837-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ea837-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="ea837-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ea837-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ea837-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="ea837-111">See Also</span></span>

- [<span data-ttu-id="ea837-112">Microsoft. тактов. подготовка. Препаречоистате</span><span class="sxs-lookup"><span data-stu-id="ea837-112">Microsoft.Quantum.Preparation.PrepareChoiState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiState)