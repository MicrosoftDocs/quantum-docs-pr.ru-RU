---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Операция Препаречоистате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: ced71c4278f42f577760acd54ae53e7f5e6dae4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210579"
---
# <a name="preparechoistate-operation"></a>Операция Препаречоистате

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Подготавливает состояние Чои – Жамиоłковски для данной операции к указанным ссылочным и целевым регистрам.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Необходимо подготовить операцию $ \Ламбда $, Чои — Жамиоłковски State $J (\Ламбда)/2 ^ N $, где $N $ — это количество Кубитс, на которое `op` действует.


### <a name="reference--qubit"></a>Ссылка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс, начиная с $ \ket{00\cdots 0} $, для использования в качестве ссылки на действие `op` .


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс изначально находится в состоянии $ \ket{00\cdots 0} $, `op` к которому применяется.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Параметр Чои – Жамиłковски State $J (\Ламбда) $ для тактового процесса определяется как $ $ \бегин{алигн} J (\Ламбда) \масрел{: =} (\болдоне \отимес \Ламбда) (| \болдоне\рангле \! \rangle\langle \! \langle\boldone |), \end{align} $ $ WHERE $ | Кс\рангле \! \рангле $ — это *вектор* матрицы, $X $ в соглашении о стеке столбцов. Изучение классического описания этого состояния предоставляет полную информацию о действии $ \Ламбда $, действующей на произвольные входные состояния, и формирует основу *тактового процесса томографи*.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. подготовка. Препаречоистатеа](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [Microsoft. тактов. подготовка. Препаречоистатек](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [Microsoft. тактов. подготовка. Препаречоистатека](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)