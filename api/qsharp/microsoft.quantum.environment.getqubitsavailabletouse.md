---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Операция Жеткубитсаваилаблетаусе
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201416"
---
# <a name="getqubitsavailabletouse-operation"></a>Операция Жеткубитсаваилаблетаусе

Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает количество Кубитс, доступных в данный момент для использования.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, которое может быть выделено в `using` инструкции.
Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Environment. Жеткубитсаваилаблетоборров](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)