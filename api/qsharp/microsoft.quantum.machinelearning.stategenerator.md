---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: Определяемый пользователем тип Статеженератор
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854877"
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
### <a name="prepare--littleendian--unit--is-adj--ctl"></a>Подготовка: [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Операция, которая подготавливает закодированные входные данные к регистру Кубитс с прямым порядком следования `NQubits` .