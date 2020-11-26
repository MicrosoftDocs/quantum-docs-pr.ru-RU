---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Функция Буларрайаспаули
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: 8e7088ec3918165d7b2afb1056a8319c6fb17796
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214285"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="c120b-102">Функция Буларрайаспаули</span><span class="sxs-lookup"><span data-stu-id="c120b-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="c120b-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="c120b-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="c120b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c120b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c120b-105">При наличии битовой строки возвращает оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="c120b-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="c120b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c120b-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="c120b-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="c120b-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="c120b-108">Оператор Паули для применения к Кубитс, где `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="c120b-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="c120b-109">Битаппли: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c120b-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c120b-110">применить Паули, если бит — это значение.</span><span class="sxs-lookup"><span data-stu-id="c120b-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="c120b-111">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c120b-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c120b-112">Логический массив.</span><span class="sxs-lookup"><span data-stu-id="c120b-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="c120b-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="c120b-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="c120b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c120b-114">Remarks</span></span>

<span data-ttu-id="c120b-115">Логический массив и регистр такта должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="c120b-115">The Boolean array and the quantum register must be of equal length.</span></span>