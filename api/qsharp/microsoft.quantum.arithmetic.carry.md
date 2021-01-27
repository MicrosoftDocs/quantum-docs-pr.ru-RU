---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Выполнение операции
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843356"
---
# <a name="carry-operation"></a><span data-ttu-id="97eaa-102">Выполнение операции</span><span class="sxs-lookup"><span data-stu-id="97eaa-102">Carry operation</span></span>

<span data-ttu-id="97eaa-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="97eaa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="97eaa-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="97eaa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="97eaa-105">Реализует обратимый вентиль.</span><span class="sxs-lookup"><span data-stu-id="97eaa-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="97eaa-106">Учитывая поразрядность, закодированную в кубит `carryIn` и два слагаемому бит, закодированные в `summand1` и `summand2` , вычисляют побитовое исключающее XOR `carryIn` , `summand1` а `summand2` в кубит, `summand2` а также ксоред в кубит `carryOut` .</span><span class="sxs-lookup"><span data-stu-id="97eaa-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="97eaa-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="97eaa-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="97eaa-108">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="97eaa-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="97eaa-109">Кубит.</span><span class="sxs-lookup"><span data-stu-id="97eaa-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="97eaa-110">summand1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="97eaa-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="97eaa-111">First слагаемому кубит.</span><span class="sxs-lookup"><span data-stu-id="97eaa-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="97eaa-112">summand2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="97eaa-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="97eaa-113">Второй слагаемому кубит заменяется нижним битом суммы `summand1` и `summand2` .</span><span class="sxs-lookup"><span data-stu-id="97eaa-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="97eaa-114">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="97eaa-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="97eaa-115">Кубит для выполнения, будет ксоред с более высоким битом суммы.</span><span class="sxs-lookup"><span data-stu-id="97eaa-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97eaa-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97eaa-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

