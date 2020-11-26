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
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="bf4e3-102">Операция Жеткубитсаваилаблетаусе</span><span class="sxs-lookup"><span data-stu-id="bf4e3-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="bf4e3-103">Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="bf4e3-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="bf4e3-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bf4e3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bf4e3-105">Возвращает количество Кубитс, доступных в данный момент для использования.</span><span class="sxs-lookup"><span data-stu-id="bf4e3-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="bf4e3-106">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf4e3-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf4e3-107">Число Кубитс, которое может быть выделено в `using` инструкции.</span><span class="sxs-lookup"><span data-stu-id="bf4e3-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="bf4e3-108">Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.</span><span class="sxs-lookup"><span data-stu-id="bf4e3-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf4e3-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="bf4e3-109">See Also</span></span>

- [<span data-ttu-id="bf4e3-110">Microsoft. тактов. Environment. Жеткубитсаваилаблетоборров</span><span class="sxs-lookup"><span data-stu-id="bf4e3-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)