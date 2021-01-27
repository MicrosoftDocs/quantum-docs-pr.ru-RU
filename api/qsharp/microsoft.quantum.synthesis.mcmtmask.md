---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: Определяемый пользователем тип Мкмтмаск
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 50bec0f9aca95afab83491db6b742d1f0323371f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855376"
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

