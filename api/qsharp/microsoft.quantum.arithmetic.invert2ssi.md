---
uid: Microsoft.Quantum.Arithmetic.Invert2sSI
title: Операция Invert2sSI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Invert2sSI
qsharp.summary: Inverts a given integer modulo 2's complement.
ms.openlocfilehash: 86d90fc5406089549de0036fcaebd9dc9d188c40
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222853"
---
# <a name="invert2ssi-operation"></a><span data-ttu-id="0bb77-102">Операция Invert2sSI</span><span class="sxs-lookup"><span data-stu-id="0bb77-102">Invert2sSI operation</span></span>

<span data-ttu-id="0bb77-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0bb77-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0bb77-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0bb77-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0bb77-105">Инвертирует дополнение заданного целочисленного модуля 2.</span><span class="sxs-lookup"><span data-stu-id="0bb77-105">Inverts a given integer modulo 2's complement.</span></span>

```qsharp
operation Invert2sSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0bb77-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0bb77-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="0bb77-107">xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0bb77-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="0bb77-108">n-разрядное целое число со знаком (Сигнедлиттлиндиан) будет дополнять обратный остаток от деления 2.</span><span class="sxs-lookup"><span data-stu-id="0bb77-108">n-bit signed integer (SignedLittleEndian), will be inverted modulo 2's complement.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0bb77-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0bb77-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

