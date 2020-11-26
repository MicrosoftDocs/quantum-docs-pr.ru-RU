---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Определяемый пользователем тип Жорданвигнеринпутстате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 81993a7449098c03639cf090fb36ed39c6ba17c0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214693"
---
# <a name="jordanwignerinputstate-user-defined-type"></a>Определяемый пользователем тип Жорданвигнеринпутстате

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Формат данных, передаваемых из C# в Q # для представления подготовки начального состояния, значение представленных данных определяется алгоритмом, который их получает.

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

