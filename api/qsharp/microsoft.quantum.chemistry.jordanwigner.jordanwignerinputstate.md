---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState
title: Определяемый пользователем тип Жорданвигнеринпутстате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerInputState
qsharp.summary: Format of data passed from C# to Q# to represent preparation of the initial state The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 171a2999ab8c73925d4624c565bfd41a4e73c99d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713983"
---
# <a name="jordanwignerinputstate-user-defined-type"></a>Определяемый пользователем тип Жорданвигнеринпутстате

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакеты [](https://nuget.org/packages/)


Формат данных, передаваемых из C# в Q # для представления подготовки начального состояния, значение представленных данных определяется алгоритмом, который их получает.

```qsharp

newtype JordanWignerInputState = ((Double, Double), Int[]);
```

