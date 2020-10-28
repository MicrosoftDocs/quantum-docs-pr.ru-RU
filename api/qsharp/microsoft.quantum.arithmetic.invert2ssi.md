---
uid: Microsoft.Quantum.Arithmetic.Invert2sSI
title: Операция Invert2sSI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Invert2sSI
qsharp.summary: Inverts a given integer modulo 2's complement.
ms.openlocfilehash: 6cb27477d66320ba741eb902e7c8a9e740a9b3f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731464"
---
# <a name="invert2ssi-operation"></a><span data-ttu-id="c8bcc-102">Операция Invert2sSI</span><span class="sxs-lookup"><span data-stu-id="c8bcc-102">Invert2sSI operation</span></span>

<span data-ttu-id="c8bcc-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c8bcc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c8bcc-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c8bcc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c8bcc-105">Инвертирует дополнение заданного целочисленного модуля 2.</span><span class="sxs-lookup"><span data-stu-id="c8bcc-105">Inverts a given integer modulo 2's complement.</span></span>

```qsharp
operation Invert2sSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="c8bcc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c8bcc-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="c8bcc-107">xs: [сигнедлиттлиндиан](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c8bcc-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="c8bcc-108">n-разрядное целое число со знаком (Сигнедлиттлиндиан) будет дополнять обратный остаток от деления 2.</span><span class="sxs-lookup"><span data-stu-id="c8bcc-108">n-bit signed integer (SignedLittleEndian), will be inverted modulo 2's complement.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c8bcc-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c8bcc-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

