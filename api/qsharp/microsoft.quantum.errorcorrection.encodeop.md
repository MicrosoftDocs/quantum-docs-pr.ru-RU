---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Определяемый пользователем тип Енкодеоп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: da947cdc25cb0edd3a4144022bbfc6ecb84c647f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712346"
---
# <a name="encodeop-user-defined-type"></a>Определяемый пользователем тип Енкодеоп

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Представляет операцию, которая кодирует физическую регистрацию в логическую регистрацию с помощью предоставленного вспомогательного Кубитс.

Первый аргумент принимается в качестве физического регистра, который будет кодироваться, а второй аргумент является временным регистром, который будет использоваться.

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

