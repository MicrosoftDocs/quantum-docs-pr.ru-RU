---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateCA
title: Операция Препаречоистатека
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateCA
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation with both controlled and adjoint variants onto given reference and target registers.
ms.openlocfilehash: b9d2cdaea1ebc957719d92bf12901c54a55a56aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709447"
---
# <a name="preparechoistateca-operation"></a>Операция Препаречоистатека

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакеты [](https://nuget.org/packages/)


Подготавливает состояние Чои – Жамиłковски для заданной операции с управляемыми и соседними вариантами на заданный эталонный и целевой регистры.

```qsharp
operation PrepareChoiStateCA (op : (Qubit[] => Unit is Adj + Ctl), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit-adj--ctl"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL




### <a name="reference--qubit"></a>Ссылка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Препаречоистате](xref:Microsoft.Quantum.Preparation.PrepareChoiState)