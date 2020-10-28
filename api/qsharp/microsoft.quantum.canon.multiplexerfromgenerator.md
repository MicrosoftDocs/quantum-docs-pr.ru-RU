---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: Функция Мултиплексерфромженератор
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 327d995d3870732887f880778eb289c3aad1f030
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715888"
---
# <a name="multiplexerfromgenerator-function"></a><span data-ttu-id="1cb16-102">Функция Мултиплексерфромженератор</span><span class="sxs-lookup"><span data-stu-id="1cb16-102">MultiplexerFromGenerator function</span></span>

<span data-ttu-id="1cb16-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1cb16-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1cb16-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1cb16-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1cb16-105">Возвращает операцию, зависящую от умножения, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="1cb16-105">Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="1cb16-106">$U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.</span><span class="sxs-lookup"><span data-stu-id="1cb16-106">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="1cb16-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1cb16-107">Input</span></span>

### <a name="unitarygenerator--intint---qubit--unit-adj--ctl"></a><span data-ttu-id="1cb16-108">унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL)</span><span class="sxs-lookup"><span data-stu-id="1cb16-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="1cb16-109">Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.</span><span class="sxs-lookup"><span data-stu-id="1cb16-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>



## <a name="output--littleendianqubit--unit-adj--ctl"></a><span data-ttu-id="1cb16-110">Выходные данные: ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия</span><span class="sxs-lookup"><span data-stu-id="1cb16-110">Output : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="1cb16-111">Операция, зависящая от умножения, $U $, которая применяет унитариес, описанную в `unitaryGenerator` .</span><span class="sxs-lookup"><span data-stu-id="1cb16-111">A multiply-controlled unitary operation $U$ that applies unitaries described by `unitaryGenerator`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cb16-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="1cb16-112">See Also</span></span>

- [<span data-ttu-id="1cb16-113">Microsoft. тактов. Canon. Мултиплексоператионсфромженератор</span><span class="sxs-lookup"><span data-stu-id="1cb16-113">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)