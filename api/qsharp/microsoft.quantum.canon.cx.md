---
uid: Microsoft.Quantum.Canon.CX
title: Операция CX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: c430525b71ad4ef0812d90a8ff20c41a5d5b8708
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716377"
---
# <a name="cx-operation"></a>Операция CX

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет шлюз с управляемой X (CX) к паре Кубитс.

$ $ \бегин{алигн} \лефт (\бегин{Матрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{Матрикс}\ригхт) \енд{алигн}, $ $, где строки и столбцы упорядочены как в разделе "Основные понятия о такте".

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="control--qubit"></a>элемент управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Управление кубит для шлюза CX.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит для шлюза CX.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Эквивалентно:

```qsharp
Controlled X([control], target);
```

и в:

```qsharp
CNOT(control, target);
```