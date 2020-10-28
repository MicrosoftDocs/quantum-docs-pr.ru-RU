---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Определяемый пользователем тип Фикседпоинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: f1370cd2f8a7d6488ae0f6be841abd95e61f038e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731536"
---
# <a name="fixedpoint-user-defined-type"></a><span data-ttu-id="d3ab5-102">Определяемый пользователем тип Фикседпоинт</span><span class="sxs-lookup"><span data-stu-id="d3ab5-102">FixedPoint user defined type</span></span>

<span data-ttu-id="d3ab5-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d3ab5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d3ab5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d3ab5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d3ab5-105">Представляет регистр Кубитс кодирования числа с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="d3ab5-105">Represents a register of qubits encoding a fixed-point number.</span></span> <span data-ttu-id="d3ab5-106">Состоит из целого числа, равного числу Кубитс слева от двоичной точки, т. е. Кубитс весовой коэффициент больше или равен 1, и регистр такта.</span><span class="sxs-lookup"><span data-stu-id="d3ab5-106">Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.</span></span>

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

