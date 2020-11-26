---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Определяемый пользователем тип Статеженератор
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: 5c9643f5c917ff3cb25fa8c046856b03cc287edd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211565"
---
# <a name="stategenerator-user-defined-type"></a>Определяемый пользователем тип Статеженератор

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Описывает операцию, которая подготавливает заданный вход для последовательного классификатора.

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Именованные элементы

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, для которых определено закодированное входное значение.
### <a name="prepare--littleendian--unit--is-adj--ctl"></a>Подготовка: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Операция, которая подготавливает закодированные входные данные к регистру Кубитс с прямым порядком следования `NQubits` .