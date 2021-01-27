---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: Функция Мултиплексерфромженератор
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: b86238debe66747ba23c3b41164813594f80b27c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852550"
---
# <a name="multiplexerfromgenerator-function"></a><span data-ttu-id="ae8e0-102">Функция Мултиплексерфромженератор</span><span class="sxs-lookup"><span data-stu-id="ae8e0-102">MultiplexerFromGenerator function</span></span>

<span data-ttu-id="ae8e0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ae8e0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ae8e0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae8e0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae8e0-105">Возвращает операцию, зависящую от умножения, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="ae8e0-105">Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="ae8e0-106">$U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.</span><span class="sxs-lookup"><span data-stu-id="ae8e0-106">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="ae8e0-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ae8e0-107">Input</span></span>

### <a name="unitarygenerator--intint---qubit--unit--is-adj--ctl"></a><span data-ttu-id="ae8e0-108">унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL")</span><span class="sxs-lookup"><span data-stu-id="ae8e0-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="ae8e0-109">Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.</span><span class="sxs-lookup"><span data-stu-id="ae8e0-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>



## <a name="output--littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="ae8e0-110">Выходные данные: ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="ae8e0-110">Output : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ae8e0-111">Операция, зависящая от умножения, $U $, которая применяет унитариес, описанную в `unitaryGenerator` .</span><span class="sxs-lookup"><span data-stu-id="ae8e0-111">A multiply-controlled unitary operation $U$ that applies unitaries described by `unitaryGenerator`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae8e0-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="ae8e0-112">See Also</span></span>

- [<span data-ttu-id="ae8e0-113">Microsoft. тактов. Canon. Мултиплексоператионсфромженератор</span><span class="sxs-lookup"><span data-stu-id="ae8e0-113">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)