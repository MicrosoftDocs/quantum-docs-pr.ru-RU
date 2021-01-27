---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Определяемый пользователем тип байтов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843391"
---
# <a name="bigendian-user-defined-type"></a><span data-ttu-id="ab127-102">Определяемый пользователем тип байтов</span><span class="sxs-lookup"><span data-stu-id="ab127-102">BigEndian user defined type</span></span>

<span data-ttu-id="ab127-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ab127-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ab127-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ab127-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ab127-105">Регистрация, которая кодирует целое число без знака в порядке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ab127-105">Register that encodes an unsigned integer in big-endian order.</span></span> <span data-ttu-id="ab127-106">Кубит с индексом `0` кодирует наибольший бит целого числа без знака.</span><span class="sxs-lookup"><span data-stu-id="ab127-106">The qubit with index `0` encodes the highest bit of an unsigned integer.</span></span>

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="ab127-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="ab127-107">Remarks</span></span>

<span data-ttu-id="ab127-108">Мы предлагаем сокращение, `BigEndian` как `BE` в документации.</span><span class="sxs-lookup"><span data-stu-id="ab127-108">We abbreviate `BigEndian` as `BE` in the documentation.</span></span>