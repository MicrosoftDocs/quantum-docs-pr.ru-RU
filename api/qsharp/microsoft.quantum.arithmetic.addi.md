---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Операция Адди
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 9a90d15defd57cf2836a6fda5b52ddaa816fd55e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191029"
---
# <a name="addi-operation"></a><span data-ttu-id="f88cf-102">Операция Адди</span><span class="sxs-lookup"><span data-stu-id="f88cf-102">AddI operation</span></span>

<span data-ttu-id="f88cf-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f88cf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f88cf-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="f88cf-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="f88cf-105">Автоматически выбирает между добавлением и без, в зависимости от размера регистра `ys` .</span><span class="sxs-lookup"><span data-stu-id="f88cf-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f88cf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f88cf-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f88cf-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f88cf-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f88cf-108">$n $-bit слагаемое.</span><span class="sxs-lookup"><span data-stu-id="f88cf-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="f88cf-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f88cf-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f88cf-110">Слагаемое по крайней мере $n $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="f88cf-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="f88cf-111">Будет содержать результат.</span><span class="sxs-lookup"><span data-stu-id="f88cf-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f88cf-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f88cf-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

