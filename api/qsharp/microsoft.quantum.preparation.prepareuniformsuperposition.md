---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Операция Препареуниформсуперпоситион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: 9b9f182ed7c1ea24ae74b8a2321a309042a17c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230095"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="3ac9f-102">Операция Препареуниформсуперпоситион</span><span class="sxs-lookup"><span data-stu-id="3ac9f-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="3ac9f-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="3ac9f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="3ac9f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3ac9f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3ac9f-105">Создает равномерное перестановку по состояниям, закодированным с 0 по `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="3ac9f-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="3ac9f-106">То есть, это единое $U $ создает равномерное перестановку для всех состояний $0 $ в $M-$1, учитывая входное состояние $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="3ac9f-107">Иными словами, $ $ \бегин{алигн} У\кет {0} = \фрак {1} {\скрт{м}}\ sum_ {j = 0} ^ {M-1} \кет{ж}.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="3ac9f-108">\енд{алигн} $ $.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3ac9f-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3ac9f-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="3ac9f-110">Ниндицес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ac9f-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ac9f-111">Требуемое число Штатов $M $ в равномерном положении.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="3ac9f-112">Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ac9f-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3ac9f-113">Регистр кубит, в котором хранятся числовые состояния в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="3ac9f-114">Этот регистр должен иметь возможность хранить число $M-$1, а предполагается, что оно инициализировано в состоянии $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ac9f-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ac9f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ac9f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ac9f-116">Remarks</span></span>

<span data-ttu-id="3ac9f-117">Операция является аджоинтабле, но требует, чтобы `indexRegister` она наглядела в равномерном положении на первом `nIndices` уровне в этом случае.</span><span class="sxs-lookup"><span data-stu-id="3ac9f-117">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>