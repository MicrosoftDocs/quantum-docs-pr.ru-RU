---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: Операция Рипплекарряддеркдкм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: df9b62b649af532a4202aacc3e8dd4613eb8665d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846363"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="35a8b-102">Операция Рипплекарряддеркдкм</span><span class="sxs-lookup"><span data-stu-id="35a8b-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="35a8b-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="35a8b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="35a8b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="35a8b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="35a8b-105">Обратимое выполнение — добавление двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="35a8b-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="35a8b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="35a8b-106">Description</span></span>

<span data-ttu-id="35a8b-107">Учитывая два $n $-разрядных целых чисел, закодированных в регистрах Литтлиндиан `xs` и `ys` , и кубит, операция вычисляет сумму двух целых чисел, в которых $n $ наименьшие значащие биты результата, `ys` а бит выполнения — ксоред кубит `carry` .</span><span class="sxs-lookup"><span data-stu-id="35a8b-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="35a8b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="35a8b-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="35a8b-109">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="35a8b-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="35a8b-110">Литтлиндиан кубит Зарегистрируйте первое целое число слагаемому.</span><span class="sxs-lookup"><span data-stu-id="35a8b-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="35a8b-111">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="35a8b-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="35a8b-112">Литтлиндиан кубит зарегистрировать второе целое слагаемому, изменяется для хранения n минимально значимых битов суммы.</span><span class="sxs-lookup"><span data-stu-id="35a8b-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="35a8b-113">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="35a8b-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="35a8b-114">Кубит, ксоред с наиболее значащим битом суммы.</span><span class="sxs-lookup"><span data-stu-id="35a8b-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="35a8b-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="35a8b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="35a8b-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="35a8b-116">Remarks</span></span>

<span data-ttu-id="35a8b-117">Эта операция имеет те же функциональные возможности, что и Рипплекарряддерд, но использует только один вспомогательный кубит вместо $n $.</span><span class="sxs-lookup"><span data-stu-id="35a8b-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="35a8b-118">Ссылки</span><span class="sxs-lookup"><span data-stu-id="35a8b-118">References</span></span>

- <span data-ttu-id="35a8b-119">Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.</span><span class="sxs-lookup"><span data-stu-id="35a8b-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1