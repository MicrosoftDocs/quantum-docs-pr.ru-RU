---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Операция Жеткубитсаваилаблетоборров
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: 30b97c2b6e1353f008d085c3bae6160763557c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201467"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Операция Жеткубитсаваилаблетоборров

Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает количество Кубитс, доступных в данный момент для займа.

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Количество Кубитс, которое может быть заимствовано и не будет выделено как часть `borrowing` инструкции.
Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Environment. Жеткубитсаваилаблетаусе](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)