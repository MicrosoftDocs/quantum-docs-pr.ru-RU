---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderD
title: Операция Рипплекарряддерд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderD
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: f0f6f39fbff9f682f8f74a982c0a41847df1397a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842962"
---
# <a name="ripplecarryadderd-operation"></a><span data-ttu-id="33a21-102">Операция Рипплекарряддерд</span><span class="sxs-lookup"><span data-stu-id="33a21-102">RippleCarryAdderD operation</span></span>

<span data-ttu-id="33a21-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="33a21-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="33a21-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33a21-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33a21-105">Обратимое выполнение — добавление двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="33a21-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="33a21-106">Учитывая два $n $-разрядных целых чисел, закодированных в регистрах Литтлиндиан `xs` и `ys` , и кубит, операция вычисляет сумму двух целых чисел, в которых $n $ наименьшие значащие биты результата, `ys` а бит выполнения — ксоред кубит `carry` .</span><span class="sxs-lookup"><span data-stu-id="33a21-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderD (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="33a21-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="33a21-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="33a21-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="33a21-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="33a21-109">Литтлиндиан кубит Зарегистрируйте первое целое число слагаемому.</span><span class="sxs-lookup"><span data-stu-id="33a21-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="33a21-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="33a21-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="33a21-111">Литтлиндиан кубит зарегистрировать второе целое слагаемому, изменяется для хранения $n $ наименьших значащих разрядов суммы.</span><span class="sxs-lookup"><span data-stu-id="33a21-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="33a21-112">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="33a21-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="33a21-113">Кубит, ксоред с наиболее значащим битом суммы.</span><span class="sxs-lookup"><span data-stu-id="33a21-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="33a21-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33a21-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="33a21-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="33a21-115">Remarks</span></span>

<span data-ttu-id="33a21-116">Указанная управляемая операция использует симметрию и взаимную отмену операций для улучшения реализации по умолчанию, добавляющей элемент управления в каждую операцию.</span><span class="sxs-lookup"><span data-stu-id="33a21-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="33a21-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="33a21-117">References</span></span>

- <span data-ttu-id="33a21-118">Томас G. Драпер: "Добавление на тактовый компьютер", 2000.</span><span class="sxs-lookup"><span data-stu-id="33a21-118">Thomas G. Draper: "Addition on a Quantum Computer", 2000.</span></span>
  https://arxiv.org/abs/quant-ph/0008033