---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Операция InjectPi4YRotation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 8558767050c317661dfb490143fa3c8f4ea009e2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712318"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="6464c-102">Операция InjectPi4YRotation</span><span class="sxs-lookup"><span data-stu-id="6464c-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="6464c-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="6464c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="6464c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6464c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6464c-105">Поворачивает один кубит в π/4 о оси Y.</span><span class="sxs-lookup"><span data-stu-id="6464c-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="6464c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6464c-106">Description</span></span>

<span data-ttu-id="6464c-107">Выполняет поворот π/4 о `Y` .</span><span class="sxs-lookup"><span data-stu-id="6464c-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="6464c-108">Поворот выполняется путем использования волшебного состояния; то есть копия State $ $ \бегин{алигн} \кос\фрак{\пи} {8} \кет {0} + \син \фрак{\пи} {8} \кет {1} .</span><span class="sxs-lookup"><span data-stu-id="6464c-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="6464c-109">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="6464c-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="6464c-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6464c-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="6464c-111">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6464c-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6464c-112">Объект кубит, повернутый около $Y $ by $ \пи/$4.</span><span class="sxs-lookup"><span data-stu-id="6464c-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="6464c-113">волшебность: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6464c-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6464c-114">Кубит изначально находится в состоянии Magic.</span><span class="sxs-lookup"><span data-stu-id="6464c-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="6464c-115">После применения этой операции возвращается в `magic` состояние $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="6464c-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6464c-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6464c-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6464c-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="6464c-117">Remarks</span></span>

<span data-ttu-id="6464c-118">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="6464c-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="6464c-119">и</span><span class="sxs-lookup"><span data-stu-id="6464c-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="6464c-120">Эта операция поддерживает `Adjoint` функтор, в этом случае используется одно и то же магическое состояние, но воздействие на кубит данных — это вращение $-\ PI/4 $ $Y $-.</span><span class="sxs-lookup"><span data-stu-id="6464c-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>