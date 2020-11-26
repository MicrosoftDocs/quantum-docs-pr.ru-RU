---
uid: Microsoft.Quantum.Canon.Trotter1ImplCA
title: Операция Trotter1ImplCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter1ImplCA
qsharp.summary: Implementation of the first-order Trotter–Suzuki integrator.
ms.openlocfilehash: 1b4e0a9597f4f30b8e92ef91ff0780e7c7ecdc9b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204799"
---
# <a name="trotter1implca-operation"></a>Операция Trotter1ImplCA

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализация первого порядка Троттер – Сузуки Integrator.

```qsharp
operation Trotter1ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
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