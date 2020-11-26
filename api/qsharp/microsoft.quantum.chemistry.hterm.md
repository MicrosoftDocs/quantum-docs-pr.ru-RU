---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Определяемый пользователем тип Хтерм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 504d55dc57ce92c12e6f016e9afcedfd59664aa1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204136"
---
# <a name="hterm-user-defined-type"></a>Определяемый пользователем тип Хтерм

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Формат данных, передаваемых из C# в Q # для представления термина Хамилтониан.
Значение представленных данных определяется алгоритмом, который их получает.

```qsharp

newtype HTerm = (Int[], Double[]);
```

