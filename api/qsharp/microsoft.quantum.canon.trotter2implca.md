---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Операция Trotter2ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 34b60934b67c19b2d1d718d68b85a2f0fffeab5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852017"
---
# <a name="trotter2implca-operation"></a>Операция Trotter2ImplCA

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализация второго порядка Троттер – Сузуки Integrator.

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="nsteps--int"></a>Нстепс: [int](xref:microsoft.quantum.lang-ref.int)

Количество операций, которые необходимо отложить на временные шаги.


### <a name="op--intdoublet--unit--is-adj--ctl"></a>Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) и тактовый регистр (тип `'T` ) для декомпозиции.


### <a name="stepsize--double"></a>Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Множитель по размеру каждого этапа моделирования.


### <a name="target--t"></a>Целевой объект: 'T

Регистр такта, на котором действует операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .

## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
op(0, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(0, deltaT / 2.0, target);
```

и

```qsharp
Trotter2ImplCA((2, op), deltaT, target);
```