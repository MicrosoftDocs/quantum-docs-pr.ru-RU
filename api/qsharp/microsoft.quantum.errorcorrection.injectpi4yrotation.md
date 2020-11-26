---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Операция InjectPi4YRotation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 4ff0abe67a6d18204e417a45f8d8f1d092d02b88
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200804"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="402ca-102">Операция InjectPi4YRotation</span><span class="sxs-lookup"><span data-stu-id="402ca-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="402ca-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="402ca-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="402ca-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="402ca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="402ca-105">Поворачивает один кубит в π/4 о оси Y.</span><span class="sxs-lookup"><span data-stu-id="402ca-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="402ca-106">Описание</span><span class="sxs-lookup"><span data-stu-id="402ca-106">Description</span></span>

<span data-ttu-id="402ca-107">Выполняет поворот π/4 о `Y` .</span><span class="sxs-lookup"><span data-stu-id="402ca-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="402ca-108">Поворот выполняется путем использования волшебного состояния; то есть копия State $ $ \бегин{алигн} \кос\фрак{\пи} {8} \кет {0} + \син \фрак{\пи} {8} \кет {1} .</span><span class="sxs-lookup"><span data-stu-id="402ca-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="402ca-109">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="402ca-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="402ca-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="402ca-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="402ca-111">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="402ca-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="402ca-112">Объект кубит, повернутый около $Y $ by $ \пи/$4.</span><span class="sxs-lookup"><span data-stu-id="402ca-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="402ca-113">волшебность: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="402ca-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="402ca-114">Кубит изначально находится в состоянии Magic.</span><span class="sxs-lookup"><span data-stu-id="402ca-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="402ca-115">После применения этой операции возвращается в `magic` состояние $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="402ca-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="402ca-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="402ca-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="402ca-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="402ca-117">Remarks</span></span>

<span data-ttu-id="402ca-118">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="402ca-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="402ca-119">и</span><span class="sxs-lookup"><span data-stu-id="402ca-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="402ca-120">Эта операция поддерживает `Adjoint` функтор, в этом случае используется одно и то же магическое состояние, но воздействие на кубит данных — это вращение $-\ PI/4 $ $Y $-.</span><span class="sxs-lookup"><span data-stu-id="402ca-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>