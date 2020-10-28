---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Операция Жеткубитсаваилаблетаусе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712583"
---
# <a name="getqubitsavailabletouse-operation"></a>Операция Жеткубитсаваилаблетаусе

Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)

Пакеты [](https://nuget.org/packages/)


Возвращает количество Кубитс, доступных в данный момент для использования.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, которое может быть выделено в `using` инструкции.
Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Environment. Жеткубитсаваилаблетоборров](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)