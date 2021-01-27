---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Функция Буларрайаспаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834245"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="c92d2-102">Функция Буларрайаспаули</span><span class="sxs-lookup"><span data-stu-id="c92d2-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="c92d2-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="c92d2-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="c92d2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c92d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c92d2-105">При наличии битовой строки возвращает оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="c92d2-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="c92d2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c92d2-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="c92d2-107">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="c92d2-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="c92d2-108">Оператор Паули для применения к Кубитс, где `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="c92d2-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="c92d2-109">Битаппли: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c92d2-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c92d2-110">применить Паули, если бит — это значение.</span><span class="sxs-lookup"><span data-stu-id="c92d2-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="c92d2-111">Разрядность: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c92d2-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c92d2-112">Логический массив.</span><span class="sxs-lookup"><span data-stu-id="c92d2-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="c92d2-113">Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="c92d2-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="c92d2-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="c92d2-114">Remarks</span></span>

<span data-ttu-id="c92d2-115">Логический массив и регистр такта должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="c92d2-115">The Boolean array and the quantum register must be of equal length.</span></span>