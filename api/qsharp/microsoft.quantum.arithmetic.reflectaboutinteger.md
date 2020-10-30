---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Операция Рефлектабаутинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730577"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="34419-102">Операция Рефлектабаутинтежер</span><span class="sxs-lookup"><span data-stu-id="34419-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="34419-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="34419-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="34419-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34419-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34419-105">Отражает тактовый регистр относительно заданного классического целого числа.</span><span class="sxs-lookup"><span data-stu-id="34419-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="34419-106">Описание</span><span class="sxs-lookup"><span data-stu-id="34419-106">Description</span></span>

<span data-ttu-id="34419-107">С учетом регистра такта изначально находится в состоянии $ \ sum_i \ alpha_i \кет{и} $, где каждый $ \кет{и} $ является исходным состоянием, представляющим целое число $i $, отражает состояние регистра относительно базового состояния для заданного целого числа $ \кет{ж} $, $ $ \ sum_i (-1) ^ {\ delta_ {ИЖ}} \ alpha_i \кет{и} $ $</span><span class="sxs-lookup"><span data-stu-id="34419-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="34419-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34419-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="34419-109">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="34419-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="34419-110">Классическое целое число, которое индексирует состояние основания, относительно которого будет отражаться.</span><span class="sxs-lookup"><span data-stu-id="34419-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="34419-111">reg: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="34419-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="34419-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34419-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="34419-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="34419-113">Remarks</span></span>

<span data-ttu-id="34419-114">Эта операция реализуется на месте без явного выделения дополнительных вспомогательных Кубитс.</span><span class="sxs-lookup"><span data-stu-id="34419-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>