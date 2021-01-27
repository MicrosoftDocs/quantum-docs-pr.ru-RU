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
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="38f15-102">Операция Жеткубитсаваилаблетаусе</span><span class="sxs-lookup"><span data-stu-id="38f15-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="38f15-103">Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="38f15-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="38f15-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="38f15-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="38f15-105">Возвращает количество Кубитс, доступных в данный момент для использования.</span><span class="sxs-lookup"><span data-stu-id="38f15-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="38f15-106">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="38f15-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="38f15-107">Число Кубитс, которое может быть выделено в `using` инструкции.</span><span class="sxs-lookup"><span data-stu-id="38f15-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="38f15-108">Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.</span><span class="sxs-lookup"><span data-stu-id="38f15-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="38f15-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="38f15-109">See Also</span></span>

- [<span data-ttu-id="38f15-110">Microsoft. тактов. Environment. Жеткубитсаваилаблетоборров</span><span class="sxs-lookup"><span data-stu-id="38f15-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)