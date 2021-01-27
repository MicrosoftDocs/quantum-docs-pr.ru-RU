---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Определяемый пользователем тип Декодеоп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 2b3d4558f6528c2e0f597398d12fc9331ab381b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827373"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="0d275-102">Определяемый пользователем тип Декодеоп</span><span class="sxs-lookup"><span data-stu-id="0d275-102">DecodeOp user defined type</span></span>

<span data-ttu-id="0d275-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="0d275-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="0d275-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0d275-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0d275-105">Представляет операцию, которая декодирует закодированный регистр в физический регистр и Кубитс, используемый для записи синдром.</span><span class="sxs-lookup"><span data-stu-id="0d275-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="0d275-106">Аргумент для Декодеоп совпадает с возвращаемым из Енкодеоп, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="0d275-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

