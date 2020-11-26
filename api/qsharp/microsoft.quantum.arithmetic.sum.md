---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Операция суммирования
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: 7758e29c9f08f4d05253defbe5a43a5316289522
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221799"
---
# <a name="sum-operation"></a><span data-ttu-id="88954-102">Операция суммирования</span><span class="sxs-lookup"><span data-stu-id="88954-102">Sum operation</span></span>

<span data-ttu-id="88954-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="88954-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="88954-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="88954-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="88954-105">Реализует шлюз обратимой суммы.</span><span class="sxs-lookup"><span data-stu-id="88954-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="88954-106">Учитывая поразрядность, закодированную в кубит `carryIn` и два бита слагаемому, закодированные в `summand1` и `summand2` , выполняет побитовую операцию XOR `carryIn` `summand1` и `summand2` в кубит `summand2` .</span><span class="sxs-lookup"><span data-stu-id="88954-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="88954-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="88954-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="88954-108">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="88954-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="88954-109">Кубит.</span><span class="sxs-lookup"><span data-stu-id="88954-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="88954-110">summand1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="88954-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="88954-111">First слагаемому кубит.</span><span class="sxs-lookup"><span data-stu-id="88954-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="88954-112">summand2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="88954-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="88954-113">Второй слагаемому кубит заменяется нижним битом суммы `summand1` и `summand2` .</span><span class="sxs-lookup"><span data-stu-id="88954-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="88954-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="88954-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="88954-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88954-115">Remarks</span></span>

<span data-ttu-id="88954-116">В отличие от `Carry` операции, это не приводит к вычислению бита выполнения.</span><span class="sxs-lookup"><span data-stu-id="88954-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>