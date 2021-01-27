---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Функция Паулиаррайасинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: 4c3c51813ef509fdc52773b15a956c0a99500603
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832705"
---
# <a name="pauliarrayasint-function"></a><span data-ttu-id="a49a2-102">Функция Паулиаррайасинт</span><span class="sxs-lookup"><span data-stu-id="a49a2-102">PauliArrayAsInt function</span></span>

<span data-ttu-id="a49a2-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="a49a2-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="a49a2-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a49a2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a49a2-105">Кодирует оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули в целое число.</span><span class="sxs-lookup"><span data-stu-id="a49a2-105">Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.</span></span>

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="a49a2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a49a2-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="a49a2-107">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="a49a2-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="a49a2-108">Массив из не более 31 одного кубит операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="a49a2-108">An array of at most 31 single-qubit Pauli operators.</span></span>



## <a name="output--int"></a><span data-ttu-id="a49a2-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a49a2-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a49a2-110">Целое число, однозначно идентифицирующее `paulis` , как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="a49a2-110">An integer uniquely identifying `paulis`, as described below.</span></span>

## <a name="remarks"></a><span data-ttu-id="a49a2-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="a49a2-111">Remarks</span></span>

<span data-ttu-id="a49a2-112">Каждый оператор Паули может быть закодирован с использованием двух битов: $ $ \бегин{алигн} \болдоне \мапсто 00, \куад X \мапсто 01, \куад Y \мапсто 11, \куад Z \мапсто 10.</span><span class="sxs-lookup"><span data-stu-id="a49a2-112">Each Pauli operator can be encoded using two bits: $$ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span></span>
<span data-ttu-id="a49a2-113">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="a49a2-113">\end{align} $$</span></span>

<span data-ttu-id="a49a2-114">При наличии массива операторов Паули `[P0, ..., Pn]` Эта функция возвращает целое число с расширением binary, сформированное путем сцепления сопоставлений каждого оператора Паули в порядке с обратным порядком байтов `bits(Pn) ... bits(P0)` .</span><span class="sxs-lookup"><span data-stu-id="a49a2-114">Given an array of Pauli operators `[P0, ..., Pn]`, this function returns an integer with binary expansion formed by concatenating the mappings of each Pauli operator in big-endian order `bits(Pn) ... bits(P0)`.</span></span>