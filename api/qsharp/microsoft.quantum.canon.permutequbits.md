---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Операция Пермутекубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 2fbbe0d99ad1383d77cb08ff6b03bcebd8a1971f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852327"
---
# <a name="permutequbits-operation"></a>Операция Пермутекубитс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Пермутес Кубитс с помощью операции переключения.

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="ordering--int"></a>упорядочение: [int](xref:microsoft.quantum.lang-ref.int)[]

Описание нового порядка Кубитс, где кубит с индексом теперь будет в порядке [i].


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

При указании Order = [2, 1, 0] и Register $ \кет{\ alpha_0} \кет{\ alpha_1} \кет{\ alpha_2} $ Пермутекубитс изменяет регистр на $ \кет{\ alpha_2} \кет{\ alpha_1} \кет{\ alpha_0} $

```qsharp
// The following two lines are equivalent
PermuteQubits([2, 1, 0], register);
SWAP(register[0], register[2]);
```