---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Определяемый пользователем тип байтов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 64590606f7c36e0598a9d29c5c6a7ba6d6451aa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731673"
---
# <a name="bigendian-user-defined-type"></a><span data-ttu-id="92914-102">Определяемый пользователем тип байтов</span><span class="sxs-lookup"><span data-stu-id="92914-102">BigEndian user defined type</span></span>

<span data-ttu-id="92914-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="92914-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="92914-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="92914-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="92914-105">Регистрация, которая кодирует целое число без знака в порядке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="92914-105">Register that encodes an unsigned integer in big-endian order.</span></span> <span data-ttu-id="92914-106">Кубит с индексом `0` кодирует наибольший бит целого числа без знака.</span><span class="sxs-lookup"><span data-stu-id="92914-106">The qubit with index `0` encodes the highest bit of an unsigned integer.</span></span>

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="92914-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="92914-107">Remarks</span></span>

<span data-ttu-id="92914-108">Мы предлагаем сокращение, `BigEndian` как `BE` в документации.</span><span class="sxs-lookup"><span data-stu-id="92914-108">We abbreviate `BigEndian` as `BE` in the documentation.</span></span>