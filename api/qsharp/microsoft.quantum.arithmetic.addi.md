---
uid: Microsoft.Quantum.Arithmetic.AddI
title: Операция Адди
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 7ee2b9099ea65b95647422dadc1efe4bf043d147
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731896"
---
# <a name="addi-operation"></a><span data-ttu-id="6e76a-102">Операция Адди</span><span class="sxs-lookup"><span data-stu-id="6e76a-102">AddI operation</span></span>

<span data-ttu-id="6e76a-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6e76a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6e76a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6e76a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6e76a-105">Автоматически выбирает между добавлением и без, в зависимости от размера регистра `ys` .</span><span class="sxs-lookup"><span data-stu-id="6e76a-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="6e76a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6e76a-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="6e76a-107">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6e76a-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6e76a-108">$n $-bit слагаемое.</span><span class="sxs-lookup"><span data-stu-id="6e76a-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="6e76a-109">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6e76a-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6e76a-110">Слагаемое по крайней мере $n $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="6e76a-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="6e76a-111">Будет содержать результат.</span><span class="sxs-lookup"><span data-stu-id="6e76a-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6e76a-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6e76a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

