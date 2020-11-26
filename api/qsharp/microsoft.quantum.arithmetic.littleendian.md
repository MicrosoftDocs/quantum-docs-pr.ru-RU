---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Определяемый пользователем тип Литтлиндиан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 2a00e499bf59e6d22a774706331737461e8e95e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222785"
---
# <a name="littleendian-user-defined-type"></a><span data-ttu-id="a377e-102">Определяемый пользователем тип Литтлиндиан</span><span class="sxs-lookup"><span data-stu-id="a377e-102">LittleEndian user defined type</span></span>

<span data-ttu-id="a377e-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a377e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a377e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a377e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a377e-105">Регистр кодирует целое число без знака в порядке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a377e-105">Register that encodes an unsigned integer in little-endian order.</span></span> <span data-ttu-id="a377e-106">Кубит с индексом `0` кодирует наименьший бит целого числа без знака.</span><span class="sxs-lookup"><span data-stu-id="a377e-106">The qubit with index `0` encodes the lowest bit of an unsigned integer.</span></span>

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="a377e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a377e-107">Remarks</span></span>

<span data-ttu-id="a377e-108">Мы предлагаем сокращение, `LittleEndian` как `LE` в документации.</span><span class="sxs-lookup"><span data-stu-id="a377e-108">We abbreviate `LittleEndian` as `LE` in the documentation.</span></span>