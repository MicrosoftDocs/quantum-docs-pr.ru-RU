---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderTTK
title: Операция Рипплекарряддерттк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: 45ba1b644166029ee548307cc1a7290c48e48a4b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221949"
---
# <a name="ripplecarryadderttk-operation"></a><span data-ttu-id="00bda-102">Операция Рипплекарряддерттк</span><span class="sxs-lookup"><span data-stu-id="00bda-102">RippleCarryAdderTTK operation</span></span>

<span data-ttu-id="00bda-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="00bda-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="00bda-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="00bda-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="00bda-105">Обратимое выполнение — добавление двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="00bda-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="00bda-106">Учитывая два $n $-разрядных целых чисел, закодированных в регистрах Литтлиндиан `xs` и `ys` , и кубит, операция вычисляет сумму двух целых чисел, в которых $n $ наименьшие значащие биты результата, `ys` а бит выполнения — ксоред кубит `carry` .</span><span class="sxs-lookup"><span data-stu-id="00bda-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="00bda-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="00bda-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="00bda-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="00bda-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="00bda-109">Литтлиндиан кубит Зарегистрируйте первое целое число слагаемому.</span><span class="sxs-lookup"><span data-stu-id="00bda-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="00bda-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="00bda-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="00bda-111">Литтлиндиан кубит зарегистрировать второе целое слагаемому, изменяется для хранения $n $ наименьших значащих разрядов суммы.</span><span class="sxs-lookup"><span data-stu-id="00bda-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="00bda-112">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="00bda-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="00bda-113">Кубит, ксоред с наиболее значащим битом суммы.</span><span class="sxs-lookup"><span data-stu-id="00bda-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="00bda-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="00bda-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="00bda-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00bda-115">Remarks</span></span>

<span data-ttu-id="00bda-116">Эта операция имеет те же функциональные возможности, что и Рипплекарряддерд и, Рипплекарряддеркдкм, но не использует анЦилла Кубитс.</span><span class="sxs-lookup"><span data-stu-id="00bda-116">This operation has the same functionality as RippleCarryAdderD and, RippleCarryAdderCDKM but does not use any ancilla qubits.</span></span>

## <a name="references"></a><span data-ttu-id="00bda-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="00bda-117">References</span></span>

- <span data-ttu-id="00bda-118">Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="00bda-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530