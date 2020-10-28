---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Операция Жеткубитсаваилаблетоборров
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712584"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Операция Жеткубитсаваилаблетоборров

Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)

Пакеты [](https://nuget.org/packages/)


Возвращает количество Кубитс, доступных в данный момент для займа.
Сюда входят неиспользуемые Кубитс; Это относится к Кубитс, возвращенному `GetQubitsAvailableToUse` .

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, которое может быть выделено в `borrowing` инструкции.
Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Environment. Жеткубитсаваилаблетаусе](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)