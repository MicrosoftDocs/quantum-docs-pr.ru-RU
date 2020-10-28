---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Операция Книллдистилл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 1135db83cf750918347df10c6f1301b636aaee0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712276"
---
# <a name="knilldistill-operation"></a><span data-ttu-id="83b87-102">Операция Книллдистилл</span><span class="sxs-lookup"><span data-stu-id="83b87-102">KnillDistill operation</span></span>

<span data-ttu-id="83b87-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="83b87-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="83b87-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="83b87-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="83b87-105">Реализует алгоритм Книлл "волшебного" состояния Magic.</span><span class="sxs-lookup"><span data-stu-id="83b87-105">Implements the Knill magic state distillation algorithm.</span></span>

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a><span data-ttu-id="83b87-106">Описание</span><span class="sxs-lookup"><span data-stu-id="83b87-106">Description</span></span>

<span data-ttu-id="83b87-107">Учитывая 15 приблизительных копий волшебного состояния $ $ \бегин{алигн} \кос\фрак{\пи} {8} \кет {0} + \син \фрак{\пи} {8} \кет {1} \енд{алигн}, $ $ дает одну копию более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="83b87-107">Given 15 approximate copies of a magic state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1} \end{align}, $$ yields one higher-quality copy.</span></span>

## <a name="input"></a><span data-ttu-id="83b87-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="83b87-108">Input</span></span>

### <a name="roughmagic--qubit"></a><span data-ttu-id="83b87-109">Раугхмагик: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="83b87-109">roughMagic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="83b87-110">Регистр пятнадцать Кубитс, содержащий приблизительные копии волшебного состояния.</span><span class="sxs-lookup"><span data-stu-id="83b87-110">A register of fifteen qubits containing approximate copies of a magic state.</span></span> <span data-ttu-id="83b87-111">После применения этой процедуры `roughMagic[0]` перенастройки будет содержаться одна копия высокого качества, а оставшаяся часть регистра вернется к состоянию $ \ket{00\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="83b87-111">Following application of this distillation procedure, `roughMagic[0]` will contain one higher-quality copy, and the rest of the register will be reset to the $\ket{00\cdots 0}$ state.</span></span>



## <a name="output--bool"></a><span data-ttu-id="83b87-112">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="83b87-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="83b87-113">Если `true` значение равно, то процедура прошла удачно и будет принята копия более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="83b87-113">If `true`, then the procedure succeeded and the higher-quality copy should be accepted.</span></span> <span data-ttu-id="83b87-114">Если `false` значение равно, то процедура завершилась ошибкой, а состояние регистра должно считаться неопределенным.</span><span class="sxs-lookup"><span data-stu-id="83b87-114">If `false`, the procedure failed, and the state of the register should be considered undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="83b87-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="83b87-115">Remarks</span></span>

<span data-ttu-id="83b87-116">Мы будем следовать алгоритму Книлл.</span><span class="sxs-lookup"><span data-stu-id="83b87-116">We follow the algorithm of Knill.</span></span>
<span data-ttu-id="83b87-117">Однако представленная реализация далеко не является оптимальной, так как она использует слишком много Кубитс.</span><span class="sxs-lookup"><span data-stu-id="83b87-117">However, the present implementation is far from being optimal, as it uses too many qubits.</span></span>
<span data-ttu-id="83b87-118">В этой подпрограммы добавлены волшебные состояния, в которых есть более эффективные протоколы.</span><span class="sxs-lookup"><span data-stu-id="83b87-118">The magic states are injected in this routine, in which case there are better protocols.</span></span>

## <a name="references"></a><span data-ttu-id="83b87-119">Ссылки</span><span class="sxs-lookup"><span data-stu-id="83b87-119">References</span></span>

- [<span data-ttu-id="83b87-120">книлл</span><span class="sxs-lookup"><span data-stu-id="83b87-120">Knill</span></span>](https://arxiv.org/abs/quant-ph/0402171)