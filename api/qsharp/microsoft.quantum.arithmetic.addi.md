---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Операция Адди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: a17403652cc2b2712defe52112a3ac599330da9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843848"
---
# <a name="addi-operation"></a><span data-ttu-id="fa80a-102">Операция Адди</span><span class="sxs-lookup"><span data-stu-id="fa80a-102">AddI operation</span></span>

<span data-ttu-id="fa80a-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="fa80a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="fa80a-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="fa80a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="fa80a-105">Автоматически выбирает между добавлением и без, в зависимости от размера регистра `ys` .</span><span class="sxs-lookup"><span data-stu-id="fa80a-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fa80a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fa80a-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="fa80a-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fa80a-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fa80a-108">$n $-bit слагаемое.</span><span class="sxs-lookup"><span data-stu-id="fa80a-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="fa80a-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fa80a-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fa80a-110">Слагаемое по крайней мере $n $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="fa80a-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="fa80a-111">Будет содержать результат.</span><span class="sxs-lookup"><span data-stu-id="fa80a-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fa80a-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa80a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

