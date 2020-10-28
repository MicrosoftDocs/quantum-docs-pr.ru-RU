---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Функция Паулиаррайасинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713368"
---
# <a name="pauliarrayasint-function"></a><span data-ttu-id="c0c11-102">Функция Паулиаррайасинт</span><span class="sxs-lookup"><span data-stu-id="c0c11-102">PauliArrayAsInt function</span></span>

<span data-ttu-id="c0c11-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="c0c11-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="c0c11-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c0c11-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c0c11-105">Кодирует оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули в целое число.</span><span class="sxs-lookup"><span data-stu-id="c0c11-105">Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.</span></span>

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="c0c11-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c0c11-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="c0c11-107">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="c0c11-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="c0c11-108">Массив из не более 31 одного кубит операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="c0c11-108">An array of at most 31 single-qubit Pauli operators.</span></span>



## <a name="output--int"></a><span data-ttu-id="c0c11-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c0c11-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c0c11-110">Целое число, однозначно идентифицирующее `paulis` , как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="c0c11-110">An integer uniquely identifying `paulis`, as described below.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c11-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="c0c11-111">Remarks</span></span>

<span data-ttu-id="c0c11-112">Каждый оператор Паули может быть закодирован с использованием двух битов: $ $ \бегин{алигн} \болдоне \мапсто 00, \куад X \мапсто 01, \куад Y \мапсто 11, \куад Z \мапсто 10.</span><span class="sxs-lookup"><span data-stu-id="c0c11-112">Each Pauli operator can be encoded using two bits: $$ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span></span>
<span data-ttu-id="c0c11-113">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="c0c11-113">\end{align} $$</span></span>

<span data-ttu-id="c0c11-114">При наличии массива операторов Паули `[P0, ..., Pn]` Эта функция возвращает целое число с расширением binary, сформированное путем сцепления сопоставлений каждого оператора Паули в порядке с обратным порядком байтов `bits(Pn) ... bits(P0)` .</span><span class="sxs-lookup"><span data-stu-id="c0c11-114">Given an array of Pauli operators `[P0, ..., Pn]`, this function returns an integer with binary expansion formed by concatenating the mappings of each Pauli operator in big-endian order `bits(Pn) ... bits(P0)`.</span></span>