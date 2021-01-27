---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Операция Жеткубитсаваилаблетаусе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 2ed8c3789331a15b351769be960d06f6364d8047
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827800"
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