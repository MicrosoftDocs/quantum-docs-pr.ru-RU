---
uid: Microsoft.Quantum.Intrinsic.SWAP
title: Операция переключения
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: SWAP
qsharp.summary: >-
  Applies the SWAP gate to a pair of qubits.

  \begin{align} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}, \end{align}

  where rows and columns are ordered as in the quantum concepts guide.
ms.openlocfilehash: e93c976f2fdf02de77fafa4d22e95fe9a33a9ba6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198424"
---
# <a name="swap-operation"></a>Операция переключения

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет шлюз подкачки к паре Кубитс.

\бегин{алигн} \Операторнаме{СВАП} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \енд{бматрикс}, \енд{алигн}

где строки и столбцы упорядочиваются как в разделе "Основные понятия о такте".

```qsharp
operation SWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="qubit1--qubit"></a>qubit1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый кубит, который нужно поменять местами.


### <a name="qubit2--qubit"></a>qubit2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй кубит, который необходимо поменять местами.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Эквивалентно:

```qsharp
CNOT(qubit1, qubit2);
CNOT(qubit2, qubit1);
CNOT(qubit1, qubit2);
```