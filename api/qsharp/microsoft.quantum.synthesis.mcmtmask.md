---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Определяемый пользователем тип Мкмтмаск
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 3c2debbb1f2019c7188dcb00f8ac09154fd4fd4f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203030"
---
# <a name="mcmtmask-user-defined-type"></a>Определяемый пользователем тип Мкмтмаск

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Тип для представления многоцелевого шлюза Тоффоли с несколькими управляемыми.

Первое целое число является битовой маской для управляющих линий.  Битовые индексы, которые установлены в соответствии с индексами строк управления.

Второе целое число является битовой маской для целевых строк.  Битовые индексы, которые заданы, соответствуют индексам целевой строки.

Битовые индексы обоих целых чисел должны быть несвязанными.

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="controlmask--int"></a>Контролмаск: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="targetmask--int"></a>Таржетмаск: [int](xref:microsoft.quantum.lang-ref.int)

