---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Функция Декомпосединтотиместепска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: e82df36d2e4f3767a152d5c92d7b1897c744a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840689"
---
# <a name="decomposedintotimestepsca-function"></a>Функция Декомпосединтотиместепска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает операцию, реализующую интегратор Троттер – Сузуки для данной операции.

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="nsteps--int"></a>Нстепс: [int](xref:microsoft.quantum.lang-ref.int)

Количество операций, которые необходимо отложить на временные шаги.


### <a name="op--intdoublet--unit--is-adj--ctl"></a>Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) для декомпозиции.


### <a name="trotterorder--int"></a>Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)

Выбирает порядок использования Троттер – Сузуки Integrator.
Порядок 1 и даже заказы 2, 4, 6,... в настоящее время поддерживаются.



## <a name="output--doublet--unit--is-adj--ctl"></a>Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Возвращает единую реализацию интегратора Троттер – Сузуки, где первым параметром `Double` является размер шага интеграции, а второй параметр — это целевой объект.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .

## <a name="remarks"></a>Remarks

При вызове с параметром `order` Equals `1` Эта функция возвращает операцию, которая может быть смоделирована с помощью самого низкого порядка Троттер – Сузуки Integrator $ $ \бегин{алигн} S_1 (\ламбда) = \ prod_ {j = 1} ^ {m} e ^ {H_j \ламбда}, \енд{алигн} $ $, где мы соблюдаем нотацию [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139) и разберем $ \ламбда $ как время развития (представленное первыми входными данными возвращаемой операции), и пусть $ \{ H_j \} _ {j = 1} ^ {m} $ является набором (неравномерные) динамических генераторов (хермитиан), которые `op(j, lambda, _)` моделируются с помощью единого оператора $e ^ {H_j \lambda} $.

Аналогично, функция `order` из `2` возвращает симметричный Троттер — Сузуки Integrator $ $ \бегин{алигн} S_2 (\ламбда) = \ prod_ {j = 1} ^ {m} e ^ {H_k \ламбда/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \ламбда/2}.
\енд{алигн} $ $

Более высокие значения даже `order` реализуются с помощью рекурсивного создания [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).

## <a name="references"></a>Ссылки

- [*D. W. Берри, G. Ахокас, R. Cleve, B. C. Сандерс*](https://arxiv.org/abs/quant-ph/0508139)