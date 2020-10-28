---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Операция суммирования
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: b31d8ab39676ee6723e5fc053eba9e0af3ac2b2f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730440"
---
# <a name="sum-operation"></a><span data-ttu-id="ed2e9-102">Операция суммирования</span><span class="sxs-lookup"><span data-stu-id="ed2e9-102">Sum operation</span></span>

<span data-ttu-id="ed2e9-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ed2e9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ed2e9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ed2e9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ed2e9-105">Реализует шлюз обратимой суммы.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="ed2e9-106">Учитывая поразрядность, закодированную в кубит `carryIn` и два бита слагаемому, закодированные в `summand1` и `summand2` , выполняет побитовую операцию XOR `carryIn` `summand1` и `summand2` в кубит `summand2` .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ed2e9-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ed2e9-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="ed2e9-108">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ed2e9-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ed2e9-109">Кубит.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="ed2e9-110">summand1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ed2e9-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ed2e9-111">First слагаемому кубит.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="ed2e9-112">summand2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ed2e9-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ed2e9-113">Второй слагаемому кубит заменяется нижним битом суммы `summand1` и `summand2` .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ed2e9-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ed2e9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ed2e9-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="ed2e9-115">Remarks</span></span>

<span data-ttu-id="ed2e9-116">В отличие от `Carry` операции, это не приводит к вычислению бита выполнения.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>