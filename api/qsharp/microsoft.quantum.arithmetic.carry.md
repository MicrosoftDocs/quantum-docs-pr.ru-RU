---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Выполнение операции
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: 2b977151861fb01be7d7dbad6e0a7b803fded880
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731641"
---
# <a name="carry-operation"></a><span data-ttu-id="0fdf7-102">Выполнение операции</span><span class="sxs-lookup"><span data-stu-id="0fdf7-102">Carry operation</span></span>

<span data-ttu-id="0fdf7-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0fdf7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0fdf7-105">Реализует обратимый вентиль.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="0fdf7-106">Учитывая поразрядность, закодированную в кубит `carryIn` и два слагаемому бит, закодированные в `summand1` и `summand2` , вычисляют побитовое исключающее XOR `carryIn` , `summand1` а `summand2` в кубит, `summand2` а также ксоред в кубит `carryOut` .</span><span class="sxs-lookup"><span data-stu-id="0fdf7-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0fdf7-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0fdf7-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="0fdf7-108">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0fdf7-109">Кубит.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="0fdf7-110">summand1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0fdf7-111">First слагаемому кубит.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="0fdf7-112">summand2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0fdf7-113">Второй слагаемому кубит заменяется нижним битом суммы `summand1` и `summand2` .</span><span class="sxs-lookup"><span data-stu-id="0fdf7-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="0fdf7-114">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0fdf7-115">Кубит для выполнения, будет ксоред с более высоким битом суммы.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0fdf7-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0fdf7-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

