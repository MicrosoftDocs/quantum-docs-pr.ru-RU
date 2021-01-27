---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Операция Книллдистилл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 4eff99eebb1e271d240513f827c6e93973ef79a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853103"
---
# <a name="knilldistill-operation"></a><span data-ttu-id="c2bae-102">Операция Книллдистилл</span><span class="sxs-lookup"><span data-stu-id="c2bae-102">KnillDistill operation</span></span>

<span data-ttu-id="c2bae-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c2bae-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c2bae-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2bae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2bae-105">Реализует алгоритм Книлл "волшебного" состояния Magic.</span><span class="sxs-lookup"><span data-stu-id="c2bae-105">Implements the Knill magic state distillation algorithm.</span></span>

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a><span data-ttu-id="c2bae-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c2bae-106">Description</span></span>

<span data-ttu-id="c2bae-107">Учитывая 15 приблизительных копий волшебного состояния $ $ \бегин{алигн} \кос\фрак{\пи} {8} \кет {0} + \син \фрак{\пи} {8} \кет {1} \енд{алигн}, $ $ дает одну копию более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="c2bae-107">Given 15 approximate copies of a magic state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1} \end{align}, $$ yields one higher-quality copy.</span></span>

## <a name="input"></a><span data-ttu-id="c2bae-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c2bae-108">Input</span></span>

### <a name="roughmagic--qubit"></a><span data-ttu-id="c2bae-109">Раугхмагик: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c2bae-109">roughMagic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c2bae-110">Регистр пятнадцать Кубитс, содержащий приблизительные копии волшебного состояния.</span><span class="sxs-lookup"><span data-stu-id="c2bae-110">A register of fifteen qubits containing approximate copies of a magic state.</span></span> <span data-ttu-id="c2bae-111">После применения этой процедуры `roughMagic[0]` перенастройки будет содержаться одна копия высокого качества, а оставшаяся часть регистра вернется к состоянию $ \ket{00\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="c2bae-111">Following application of this distillation procedure, `roughMagic[0]` will contain one higher-quality copy, and the rest of the register will be reset to the $\ket{00\cdots 0}$ state.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c2bae-112">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c2bae-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c2bae-113">Если `true` значение равно, то процедура прошла удачно и будет принята копия более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="c2bae-113">If `true`, then the procedure succeeded and the higher-quality copy should be accepted.</span></span> <span data-ttu-id="c2bae-114">Если `false` значение равно, то процедура завершилась ошибкой, а состояние регистра должно считаться неопределенным.</span><span class="sxs-lookup"><span data-stu-id="c2bae-114">If `false`, the procedure failed, and the state of the register should be considered undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2bae-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="c2bae-115">Remarks</span></span>

<span data-ttu-id="c2bae-116">Мы будем следовать алгоритму Книлл.</span><span class="sxs-lookup"><span data-stu-id="c2bae-116">We follow the algorithm of Knill.</span></span>
<span data-ttu-id="c2bae-117">Однако представленная реализация далеко не является оптимальной, так как она использует слишком много Кубитс.</span><span class="sxs-lookup"><span data-stu-id="c2bae-117">However, the present implementation is far from being optimal, as it uses too many qubits.</span></span>
<span data-ttu-id="c2bae-118">В этой подпрограммы добавлены волшебные состояния, в которых есть более эффективные протоколы.</span><span class="sxs-lookup"><span data-stu-id="c2bae-118">The magic states are injected in this routine, in which case there are better protocols.</span></span>

## <a name="references"></a><span data-ttu-id="c2bae-119">Ссылки</span><span class="sxs-lookup"><span data-stu-id="c2bae-119">References</span></span>

- [<span data-ttu-id="c2bae-120">книлл</span><span class="sxs-lookup"><span data-stu-id="c2bae-120">Knill</span></span>](https://arxiv.org/abs/quant-ph/0402171)