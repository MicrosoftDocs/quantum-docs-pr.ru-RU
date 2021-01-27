---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Определяемый пользователем тип Статеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 005d7862214abb3dcb9c0caa006343720d179a52
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854469"
---
# <a name="stateoracle-user-defined-type"></a>Определяемый пользователем тип Статеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет Oracle для подготовки состояния.

Входные данные для Oracle $O $:

- Целочисленное индексирование флага кубит $f $.
- Система регистрирует $s $, которая будет хранить требуемое состояние такта $ \кет{\пси} \_ s $.

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Remarks

Эта база данных Oracle, определяемая $ $ О\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ PSI} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, $ $ действует на основе вычислительного состояния $ \кет {0} \_ {f} \кет {0} \_ s $ для создания целевого состояния $ \кет{\пси} \_ s $ с амплитудой $ \ламбда $ в базе, помеченной $ \кет {1} \_ f $.
Первый параметр является индексом кубит регистра $ \кет {0} \_ f $. Второй параметр охватывает оба регистра.