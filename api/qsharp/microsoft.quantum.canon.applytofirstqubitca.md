---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Операция Апплитофирсткубитка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: ba82199cc7a548d771027141780873c05de71c57
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841431"
---
# <a name="applytofirstqubitca-operation"></a>Операция Апплитофирсткубитка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет Op операции к первому кубит в регистре.
Модификатор `CA` указывает, что операция является управляемой и аджоинтабле.

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit--is-adj--ctl"></a>Op: [](xref:microsoft.quantum.lang-ref.qubit) => [единица](xref:microsoft.quantum.lang-ref.unit) кубит — "года + CTL"

Операция, применяемая к первому кубит


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит к первому кубит, к которому применяется операция



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитофирсткубит](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)