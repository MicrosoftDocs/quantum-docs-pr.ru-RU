---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Определяемый пользователем тип Блоккенкодинг
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 75fdbf13cf07d906982d4a611d1d25b3e29db2cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225437"
---
# <a name="blockencoding-user-defined-type"></a>Определяемый пользователем тип Блоккенкодинг

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет собой единое место кодирования произвольного оператора в верхнем левом блоке.

То есть, `BlockEncoding` представляет собой единое $U $, где произвольный оператор $H $, который действует на системный регистр, `s` кодируется в верхнем левом блоке, соответствующем вспомогательному состоянию $ \кет {0} _A $. Это означает следующее:

$ $ \бегин{алигн} (\бра {0} _A \отимес I_s) U (\кет {0} _a \отимес I_s) = H \енд{алигн} $ $.

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

