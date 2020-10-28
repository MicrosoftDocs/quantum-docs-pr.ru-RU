---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Определяемый пользователем тип Декодеоп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 0733ec016e50a320b162b111c7d87c32140fdacb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712415"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="a7f39-102">Определяемый пользователем тип Декодеоп</span><span class="sxs-lookup"><span data-stu-id="a7f39-102">DecodeOp user defined type</span></span>

<span data-ttu-id="a7f39-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a7f39-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a7f39-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7f39-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7f39-105">Представляет операцию, которая декодирует закодированный регистр в физический регистр и Кубитс, используемый для записи синдром.</span><span class="sxs-lookup"><span data-stu-id="a7f39-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="a7f39-106">Аргумент для Декодеоп совпадает с возвращаемым из Енкодеоп, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="a7f39-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

