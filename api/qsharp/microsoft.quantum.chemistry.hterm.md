---
uid: Microsoft.Quantum.Chemistry.HTerm
title: Определяемый пользователем тип Хтерм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 744668a4fe96ee00fe2f7991f4e1f05eea19d417
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851788"
---
# <a name="hterm-user-defined-type"></a>Определяемый пользователем тип Хтерм

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Формат данных, передаваемых из C# в Q # для представления термина Хамилтониан.
Значение представленных данных определяется алгоритмом, который их получает.

```qsharp

newtype HTerm = (Int[], Double[]);
```

