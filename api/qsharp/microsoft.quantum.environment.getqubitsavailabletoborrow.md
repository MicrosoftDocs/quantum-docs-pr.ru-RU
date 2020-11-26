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
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="87bd2-102">Операция Жеткубитсаваилаблетоборров</span><span class="sxs-lookup"><span data-stu-id="87bd2-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="87bd2-103">Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="87bd2-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="87bd2-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="87bd2-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="87bd2-105">Возвращает количество Кубитс, доступных в данный момент для займа.</span><span class="sxs-lookup"><span data-stu-id="87bd2-105">Returns the number of qubits currently available to borrow.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="87bd2-106">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="87bd2-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="87bd2-107">Количество Кубитс, которое может быть заимствовано и не будет выделено как часть `borrowing` инструкции.</span><span class="sxs-lookup"><span data-stu-id="87bd2-107">The number of qubits that could be borrowed and won't be allocated as part of a `borrowing` statement.</span></span>
<span data-ttu-id="87bd2-108">Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.</span><span class="sxs-lookup"><span data-stu-id="87bd2-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="87bd2-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="87bd2-109">See Also</span></span>

- [<span data-ttu-id="87bd2-110">Microsoft. тактов. Environment. Жеткубитсаваилаблетаусе</span><span class="sxs-lookup"><span data-stu-id="87bd2-110">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)