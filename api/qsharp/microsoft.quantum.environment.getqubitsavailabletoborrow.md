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
# <a name="getqubitsavailabletoborrow-operation"></a><span data-ttu-id="5af21-102">Операция Жеткубитсаваилаблетоборров</span><span class="sxs-lookup"><span data-stu-id="5af21-102">GetQubitsAvailableToBorrow operation</span></span>

<span data-ttu-id="5af21-103">Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="5af21-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="5af21-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5af21-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5af21-105">Возвращает количество Кубитс, доступных в данный момент для займа.</span><span class="sxs-lookup"><span data-stu-id="5af21-105">Returns the number of qubits currently available to borrow.</span></span>
<span data-ttu-id="5af21-106">Сюда входят неиспользуемые Кубитс; Это относится к Кубитс, возвращенному `GetQubitsAvailableToUse` .</span><span class="sxs-lookup"><span data-stu-id="5af21-106">This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.</span></span>

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a><span data-ttu-id="5af21-107">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5af21-107">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5af21-108">Число Кубитс, которое может быть выделено в `borrowing` инструкции.</span><span class="sxs-lookup"><span data-stu-id="5af21-108">The number of qubits that could be allocated in a `borrowing` statement.</span></span>
<span data-ttu-id="5af21-109">Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.</span><span class="sxs-lookup"><span data-stu-id="5af21-109">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="5af21-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="5af21-110">See Also</span></span>

- [<span data-ttu-id="5af21-111">Microsoft. тактов. Environment. Жеткубитсаваилаблетаусе</span><span class="sxs-lookup"><span data-stu-id="5af21-111">Microsoft.Quantum.Environment.GetQubitsAvailableToUse</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)