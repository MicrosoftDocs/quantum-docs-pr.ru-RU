---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Функция Збитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: f66b8ef0370e898dd1d095ff2840c91566f32cb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729792"
---
# <a name="zbits-function"></a><span data-ttu-id="42b05-102">Функция Збитс</span><span class="sxs-lookup"><span data-stu-id="42b05-102">ZBits function</span></span>

<span data-ttu-id="42b05-103">Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="42b05-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="42b05-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="42b05-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="42b05-105">Возвращает целое число, представляющее Z бит массива операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="42b05-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="42b05-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="42b05-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="42b05-107">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="42b05-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="42b05-108">Массив операторов Паули, которые должны быть представлены в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="42b05-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="42b05-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="42b05-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="42b05-110">Целочисленное $x $ с двоичным представлением $ (p_ {62} \, p_ {61} \, \дотс \, p_0) $, где $p _i = $0, если `paulis[i]` имеет значение `PauliI` или `PauliX` и, где $p _i = $1, если `paulis[i]` имеет значение `PauliY` или `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="42b05-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="42b05-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="42b05-111">Remarks</span></span>

<span data-ttu-id="42b05-112">Функция вызывает исключение, если длина `paulis` массива больше 63.</span><span class="sxs-lookup"><span data-stu-id="42b05-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="42b05-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="42b05-113">See Also</span></span>

- [<span data-ttu-id="42b05-114">Microsoft. тактов. побитовое. Ксбитс</span><span class="sxs-lookup"><span data-stu-id="42b05-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)