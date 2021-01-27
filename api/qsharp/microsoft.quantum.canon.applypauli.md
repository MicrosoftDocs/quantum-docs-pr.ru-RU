---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Операция Апплипаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: b3557c6d8b5a90019f6d4cfa7b405475a3ab39fb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844743"
---
# <a name="applypauli-operation"></a>Операция Апплипаули

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии кубит оператора Паули применяет соответствующую операцию к регистру.

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Оператор Multi-кубит Паули, представленный в виде массива операторов с одним кубит Паули.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Зарегистрируйтесь, чтобы применить данную операцию Паули к.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
ApplyPauli([PauliY, PauliZ, PauliX], target);
```

и

```qsharp
Y(target[0]);
Z(target[1]);
X(target[2]);
```