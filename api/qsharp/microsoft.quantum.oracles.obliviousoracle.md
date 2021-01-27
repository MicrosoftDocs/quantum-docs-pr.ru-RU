---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Определяемый пользователем тип Обливиаусоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 793e72af56e288f9b437302f9958665e92e5e763
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842552"
---
# <a name="obliviousoracle-user-defined-type"></a>Определяемый пользователем тип Обливиаусоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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