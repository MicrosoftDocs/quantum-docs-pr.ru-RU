---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Определяемый пользователем тип Фикседпоинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 18e85120647c5a1f41ccab5fbfb27ea602a279af
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843207"
---
# <a name="fixedpoint-user-defined-type"></a><span data-ttu-id="b2951-102">Определяемый пользователем тип Фикседпоинт</span><span class="sxs-lookup"><span data-stu-id="b2951-102">FixedPoint user defined type</span></span>

<span data-ttu-id="b2951-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b2951-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b2951-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="b2951-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="b2951-105">Представляет регистр Кубитс кодирования числа с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="b2951-105">Represents a register of qubits encoding a fixed-point number.</span></span> <span data-ttu-id="b2951-106">Состоит из целого числа, равного числу Кубитс слева от двоичной точки, т. е. Кубитс весовой коэффициент больше или равен 1, и регистр такта.</span><span class="sxs-lookup"><span data-stu-id="b2951-106">Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.</span></span>

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

