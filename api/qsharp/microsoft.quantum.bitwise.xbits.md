---
uid: Microsoft.Quantum.Bitwise.XBits
title: Функция Ксбитс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: 969be01204bad497496ff24cb64213f5fe1f089b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209763"
---
# <a name="xbits-function"></a><span data-ttu-id="7f158-102">Функция Ксбитс</span><span class="sxs-lookup"><span data-stu-id="7f158-102">XBits function</span></span>

<span data-ttu-id="7f158-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="7f158-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="7f158-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7f158-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7f158-105">Возвращает целое число, представляющее X бит массива операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="7f158-105">Returns an integer representing the X bits of an array of Pauli operators.</span></span>

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="7f158-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7f158-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="7f158-107">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="7f158-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="7f158-108">Массив операторов Паули, которые должны быть представлены в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="7f158-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="7f158-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7f158-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7f158-110">Целочисленное $x $ с двоичным представлением $ (p_ {62} \, p_ {61} \, \дотс \, p_0) $, где $p _i = $0, если `paulis[i]` имеет значение `PauliI` или `PauliZ` и, где $p _i = $1, если `paulis[i]` имеет значение `PauliX` или `PauliY` .</span><span class="sxs-lookup"><span data-stu-id="7f158-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliZ` and where $p_i = 1$ if `paulis[i]` is `PauliX` or `PauliY`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f158-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f158-111">Remarks</span></span>

<span data-ttu-id="7f158-112">Функция вызывает исключение, если длина `paulis` массива больше 63.</span><span class="sxs-lookup"><span data-stu-id="7f158-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f158-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="7f158-113">See Also</span></span>

- [<span data-ttu-id="7f158-114">Microsoft. тактов. побитовое. Збитс</span><span class="sxs-lookup"><span data-stu-id="7f158-114">Microsoft.Quantum.Bitwise.ZBits</span></span>](xref:Microsoft.Quantum.Bitwise.ZBits)