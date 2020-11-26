---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Операция Рипплекарряддернокарриттк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: a539d85a4800c2f4452a1c6fe2c4f88a6296c3e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222003"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="32a79-102">Операция Рипплекарряддернокарриттк</span><span class="sxs-lookup"><span data-stu-id="32a79-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="32a79-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="32a79-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="32a79-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="32a79-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="32a79-105">Обратимое выполнение — добавление двух целых чисел без выполнения.</span><span class="sxs-lookup"><span data-stu-id="32a79-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="32a79-106">Описание</span><span class="sxs-lookup"><span data-stu-id="32a79-106">Description</span></span>

<span data-ttu-id="32a79-107">При наличии двух $n $-разрядных целых чисел, закодированных в регистрах Литтлиндиан `xs` `ys` , операция вычисляет сумму двух целочисленных целых чисел от 2 до n $, где $n $ — это разрядный размер входных данных `xs` и `ys` .</span><span class="sxs-lookup"><span data-stu-id="32a79-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="32a79-108">Он не выполняет вычисление бита выполнения.</span><span class="sxs-lookup"><span data-stu-id="32a79-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="32a79-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="32a79-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="32a79-110">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="32a79-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="32a79-111">Литтлиндиан кубит Зарегистрируйте первое целое число слагаемому.</span><span class="sxs-lookup"><span data-stu-id="32a79-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="32a79-112">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="32a79-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="32a79-113">Литтлиндиан кубит зарегистрировать второе целое слагаемому, изменяется для хранения $n $ наименьших значащих разрядов суммы.</span><span class="sxs-lookup"><span data-stu-id="32a79-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="32a79-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32a79-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="32a79-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32a79-115">Remarks</span></span>

<span data-ttu-id="32a79-116">Эта операция имеет те же функции, что и Рипплекарряддерттк, но не возвращает допустимый бит.</span><span class="sxs-lookup"><span data-stu-id="32a79-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="32a79-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="32a79-117">References</span></span>

- <span data-ttu-id="32a79-118">Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="32a79-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530