---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Функция Арранжедкубитс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716742"
---
# <a name="arrangedqubits-function"></a>Функция Арранжедкубитс

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


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

