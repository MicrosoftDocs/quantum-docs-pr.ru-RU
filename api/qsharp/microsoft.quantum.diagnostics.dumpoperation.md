---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Операция Думпоператион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: cde188806506c586c4c77a7f9b2b43ad0e10ef1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829273"
---
# <a name="dumpoperation-operation"></a>Операция Думпоператион

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции отображает диагностику операции, которая стала доступной для текущего целевого объекта выполнения.

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, на которых действует данная операция.


### <a name="op--qubit--unit--is-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция, которую необходимо диагностировать.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

При запуске на целевом объекте такта имитатора следующий фрагмент выводит матрицу $ $ \бегин{алигнед} \лефт (\бегин{Матрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \енд{Матрикс}\ригхт) \енд{алигнед}.
$$

```qsharp
operation DumpCnot() : Unit {
    DumpOperation(2, ApplyToFirstTwoQubitsCA(CNOT, _));
}
```

## <a name="remarks"></a>Remarks

Вызов этой операции не имеет наблюдаемого воздействия в Q #. Точная диагностика, отображаемая при их наличии, зависит от текущего целевого объекта выполнения и среды редактора.
Например, при использовании в симуляторе с полным состоянием отображается единая матрица, используемая для представления `op` .

Обратите внимание, что при запуске в симуляторах, которые приводят к неоднозначности глобального этапа (например, симулятор с полным состоянием), возвращаемые представления могут отличаться до глобального этапа.

Аналогичным образом, упорядочивание матричных представлений строк и столбцов может отличаться от соглашений, используемых каждым симулятором, поддерживающим эту операцию.