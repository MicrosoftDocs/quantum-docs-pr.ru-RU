---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Операция Жеткубитсаваилаблетоборров
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: f2294fadb9c10d800b7a743fbfe0810f36f18516
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853247"
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