---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Операция Апплитранспоситион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855578"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="2ba83-102">Операция Апплитранспоситион</span><span class="sxs-lookup"><span data-stu-id="2ba83-102">ApplyTransposition operation</span></span>

<span data-ttu-id="2ba83-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="2ba83-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="2ba83-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ba83-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="2ba83-105">Описание</span><span class="sxs-lookup"><span data-stu-id="2ba83-105">Description</span></span>

<span data-ttu-id="2ba83-106">Эта операция меняет местами амплитуду с индексом на `a` амплитуду по индексу `b` в заданном векторе состояния `register` длины $n $.</span><span class="sxs-lookup"><span data-stu-id="2ba83-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="2ba83-107">Если `a` равно `b` , вектор состояния не изменяется.</span><span class="sxs-lookup"><span data-stu-id="2ba83-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="2ba83-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2ba83-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="2ba83-109">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2ba83-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2ba83-110">Первый индекс (должен быть значением от 0 до $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="2ba83-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="2ba83-111">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2ba83-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2ba83-112">Второй индекс (должен быть значением от 0 до $2 ^ n-$1)</span><span class="sxs-lookup"><span data-stu-id="2ba83-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="2ba83-113">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2ba83-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2ba83-114">Список $n $ Кубитс, к которому применяется транспоситион.</span><span class="sxs-lookup"><span data-stu-id="2ba83-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2ba83-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2ba83-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="2ba83-116">Пример</span><span class="sxs-lookup"><span data-stu-id="2ba83-116">Example</span></span>

<span data-ttu-id="2ba83-117">Подготовьте единое геоотносительное количество Штатов $ | 1 \ рангле $, $ | 2 \ рангле $ и $ | 3 \ рангле $ on 2 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="2ba83-117">Prepare a uniform superposition of number states $|1\rangle$, $|2\rangle$, and $|3\rangle$ on 2 qubits.</span></span>

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```