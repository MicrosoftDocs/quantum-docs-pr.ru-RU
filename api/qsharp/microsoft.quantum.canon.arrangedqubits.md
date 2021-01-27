---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Функция Арранжедкубитс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841081"
---
# <a name="arrangedqubits-function"></a>Функция Арранжедкубитс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Размещение элементов управления, целевых объектов и вспомогательных Кубитс в соответствии с индексом

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a>Описание

Возвращает массив кубит с целевым объектом с индексом 0 и элементом управления i в индексе 2 ^ i.  Вспомогательные Кубитс вставляются во все остальные позиции в массиве.

## <a name="input"></a>Входные данные

### <a name="controls--qubit"></a>элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)




### <a name="helper--qubit"></a>Helper: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--qubit"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

