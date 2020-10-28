---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Определяемый пользователем тип Обливиаусоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 7c5b35984f3c8828a5ba9bdae8f9effbc1d378f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710988"
---
# <a name="obliviousoracle-user-defined-type"></a>Определяемый пользователем тип Обливиаусоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


Представляет Oracle для усиления амплитуды очевидным.

Входные данные для Oracle $O $:

- АнЦилла Register $a $, с которым $O $ работает.
- Системная регистрация $s $, к которой применяется требуемая единая $U $, после выбора зарегистрировать $a $ в состоянии $ \кет{т} \_ a $.

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Remarks

Эта база данных Oracle, определенная $ $ О\кет {s} \_ а\кет {\ PSI} \_ s = \Ламбда\кет{т} \_ a U \кет{\пси} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет{т ^ \перп} \_ а\кдотс $ $, действует в анЦилла состоянии $ \кет{с} \_ a $ для реализации единой $U $ в любом состоянии системы $ \кет{\пси} \_ s $ с амплитудой $ \lambda $ в основе, помеченной $ \ket{t} \_ a $.
Первый параметр — кубит регистр $ \кет{с} \_ a $. Вторым параметром является кубит регистр $ \кет{\пси} \_ s $.