---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Функция Буларрайаспаули
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c5ef71322dae248fc2c6b1db3adf891de7d72488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713605"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="42b52-102">Функция Буларрайаспаули</span><span class="sxs-lookup"><span data-stu-id="42b52-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="42b52-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="42b52-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="42b52-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="42b52-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="42b52-105">При наличии битовой строки возвращает оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="42b52-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="42b52-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="42b52-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="42b52-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="42b52-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="42b52-108">Оператор Паули для применения к Кубитс, где `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="42b52-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="42b52-109">Битаппли: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="42b52-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="42b52-110">применить Паули, если бит — это значение.</span><span class="sxs-lookup"><span data-stu-id="42b52-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="42b52-111">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="42b52-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="42b52-112">Логический массив.</span><span class="sxs-lookup"><span data-stu-id="42b52-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="42b52-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="42b52-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="42b52-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="42b52-114">Remarks</span></span>

<span data-ttu-id="42b52-115">Логический массив и регистр такта должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="42b52-115">The Boolean array and the quantum register must be of equal length.</span></span>