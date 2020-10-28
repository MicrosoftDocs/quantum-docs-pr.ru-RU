---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: Функция Меасурементоператорс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713676"
---
# <a name="measurementoperators-function"></a>Функция Меасурементоператорс

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакеты [](https://nuget.org/packages/)


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