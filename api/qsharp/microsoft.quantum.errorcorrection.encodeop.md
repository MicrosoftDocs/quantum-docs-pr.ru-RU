---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Определяемый пользователем тип Енкодеоп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: c9959f1afbd44df974c06b79f73eccd090b17985
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826177"
---
# <a name="encodeop-user-defined-type"></a><span data-ttu-id="de42e-102">Определяемый пользователем тип Енкодеоп</span><span class="sxs-lookup"><span data-stu-id="de42e-102">EncodeOp user defined type</span></span>

<span data-ttu-id="de42e-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="de42e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="de42e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="de42e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="de42e-105">Представляет операцию, которая кодирует физическую регистрацию в логическую регистрацию с помощью предоставленного вспомогательного Кубитс.</span><span class="sxs-lookup"><span data-stu-id="de42e-105">Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.</span></span>

<span data-ttu-id="de42e-106">Первый аргумент принимается в качестве физического регистра, который будет кодироваться, а второй аргумент является временным регистром, который будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="de42e-106">The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.</span></span>

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

