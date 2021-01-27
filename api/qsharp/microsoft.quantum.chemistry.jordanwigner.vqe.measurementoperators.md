---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Функция Меасурементоператорс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 204ae621b77559a894f0bce14e494824d58e4ad6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835400"
---
# <a name="measurementoperators-function"></a>Функция Меасурементоператорс

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Вычисление всех операторов измерения, необходимых для расчета ожидания Jordan-Wigner термина.

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, необходимое для имитации системы молекулярное.


### <a name="indices--int"></a>индексы: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив, содержащий индексы кубит, к которым применяется каждый оператор Паули.


### <a name="termtype--int"></a>Термтипе: [int](xref:microsoft.quantum.lang-ref.int)

Тип Jordan-Wigner термина.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Массив операторов измерения (каждый из которых является массивом из Паули).