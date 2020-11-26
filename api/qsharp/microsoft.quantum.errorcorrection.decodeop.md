---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Определяемый пользователем тип Декодеоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: f1fc2851b7ed8b12cf8a47fabe794235a3083d31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201008"
---
# <a name="decodeop-user-defined-type"></a>Определяемый пользователем тип Декодеоп

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет операцию, которая декодирует закодированный регистр в физический регистр и Кубитс, используемый для записи синдром.

Аргумент для Декодеоп совпадает с возвращаемым из Енкодеоп, и наоборот.

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

