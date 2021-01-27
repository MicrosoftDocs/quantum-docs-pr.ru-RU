---
uid: Microsoft.Quantum.Preparation.PrepareUniformSuperposition
title: Операция Препареуниформсуперпоситион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareUniformSuperposition
qsharp.summary: >-
  Creates a uniform superposition over states that encode 0 through `nIndices - 1`.

  That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$. In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}. \end{align} $$.
ms.openlocfilehash: dc9d4ce1638b397748cafaa757241ce78633c67c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854322"
---
# <a name="prepareuniformsuperposition-operation"></a><span data-ttu-id="f8f1b-102">Операция Препареуниформсуперпоситион</span><span class="sxs-lookup"><span data-stu-id="f8f1b-102">PrepareUniformSuperposition operation</span></span>

<span data-ttu-id="f8f1b-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="f8f1b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="f8f1b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f8f1b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f8f1b-105">Создает равномерное перестановку по состояниям, закодированным с 0 по `nIndices - 1` .</span><span class="sxs-lookup"><span data-stu-id="f8f1b-105">Creates a uniform superposition over states that encode 0 through `nIndices - 1`.</span></span>

<span data-ttu-id="f8f1b-106">То есть, это единое $U $ создает равномерное перестановку для всех состояний $0 $ в $M-$1, учитывая входное состояние $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-106">That is, this unitary $U$ creates a uniform superposition over all number states $0$ to $M-1$, given an input state $\ket{0\cdots 0}$.</span></span> <span data-ttu-id="f8f1b-107">Иными словами, $ $ \бегин{алигн} У\кет {0} = \фрак {1} {\скрт{м}}\ sum_ {j = 0} ^ {M-1} \кет{ж}.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-107">In other words, $$ \begin{align} U\ket{0}=\frac{1}{\sqrt{M}}\sum_{j=0}^{M-1}\ket{j}.</span></span>
<span data-ttu-id="f8f1b-108">\енд{алигн} $ $.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-108">\end{align} $$.</span></span>

```qsharp
operation PrepareUniformSuperposition (nIndices : Int, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f8f1b-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f8f1b-109">Input</span></span>

### <a name="nindices--int"></a><span data-ttu-id="f8f1b-110">Ниндицес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f8f1b-110">nIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f8f1b-111">Требуемое число Штатов $M $ в равномерном положении.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-111">The desired number of states $M$ in the uniform superposition.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="f8f1b-112">Индексрегистер: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f8f1b-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f8f1b-113">Регистр кубит, в котором хранятся числовые состояния в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-113">The qubit register that stores the number states in `LittleEndian` format.</span></span>
<span data-ttu-id="f8f1b-114">Этот регистр должен иметь возможность хранить число $M-$1, а предполагается, что оно инициализировано в состоянии $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-114">This register must be able to store the number $M-1$, and is assumed to be initialized in the state $\ket{0\cdots 0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f8f1b-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f8f1b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="f8f1b-116">Пример</span><span class="sxs-lookup"><span data-stu-id="f8f1b-116">Example</span></span>

<span data-ttu-id="f8f1b-117">В следующем примере выполняется подготовка состояния $ \фрак {1} {\скрт {6} } \ sum_ {j = 0} ^ {5} \кет{ж} $ on $3 $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-117">The following example prepares the state $\frac{1}{\sqrt{6}}\sum_{j=0}^{5}\ket{j}$ on $3$ qubits.</span></span>

```qsharp
let nIndices = 6;
using(indexRegister = Qubit[3]) {
    PrepareUniformSuperposition(nIndices, LittleEndian(indexRegister));
    // ...
}
```

## <a name="remarks"></a><span data-ttu-id="f8f1b-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="f8f1b-118">Remarks</span></span>

<span data-ttu-id="f8f1b-119">Операция является аджоинтабле, но требует, чтобы `indexRegister` она наглядела в равномерном положении на первом `nIndices` уровне в этом случае.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-119">The operation is adjointable, but requires that `indexRegister` is in a uniform superposition over the first `nIndices` basis states in that case.</span></span>