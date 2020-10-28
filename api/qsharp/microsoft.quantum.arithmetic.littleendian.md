---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Определяемый пользователем тип Литтлиндиан
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: fd2744a8372793ad01d1391c035c64de1264d2f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731465"
---
# <a name="littleendian-user-defined-type"></a><span data-ttu-id="2abd4-102">Определяемый пользователем тип Литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="2abd4-102">LittleEndian user defined type</span></span>

<span data-ttu-id="2abd4-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2abd4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2abd4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2abd4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2abd4-105">Регистр кодирует целое число без знака в порядке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="2abd4-105">Register that encodes an unsigned integer in little-endian order.</span></span> <span data-ttu-id="2abd4-106">Кубит с индексом `0` кодирует наименьший бит целого числа без знака.</span><span class="sxs-lookup"><span data-stu-id="2abd4-106">The qubit with index `0` encodes the lowest bit of an unsigned integer.</span></span>

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="2abd4-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="2abd4-107">Remarks</span></span>

<span data-ttu-id="2abd4-108">Мы предлагаем сокращение, `LittleEndian` как `LE` в документации.</span><span class="sxs-lookup"><span data-stu-id="2abd4-108">We abbreviate `LittleEndian` as `LE` in the documentation.</span></span>