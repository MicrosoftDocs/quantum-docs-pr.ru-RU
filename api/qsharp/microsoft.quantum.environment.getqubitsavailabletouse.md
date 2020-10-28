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
# <a name="getqubitsavailabletouse-operation"></a><span data-ttu-id="01529-102">Операция Жеткубитсаваилаблетаусе</span><span class="sxs-lookup"><span data-stu-id="01529-102">GetQubitsAvailableToUse operation</span></span>

<span data-ttu-id="01529-103">Пространство имен: [Microsoft. такт. Environment](xref:Microsoft.Quantum.Environment)</span><span class="sxs-lookup"><span data-stu-id="01529-103">Namespace: [Microsoft.Quantum.Environment](xref:Microsoft.Quantum.Environment)</span></span>

<span data-ttu-id="01529-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="01529-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="01529-105">Возвращает количество Кубитс, доступных в данный момент для использования.</span><span class="sxs-lookup"><span data-stu-id="01529-105">Returns the number of qubits currently available to use.</span></span>

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a><span data-ttu-id="01529-106">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="01529-106">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="01529-107">Число Кубитс, которое может быть выделено в `using` инструкции.</span><span class="sxs-lookup"><span data-stu-id="01529-107">The number of qubits that could be allocated in a `using` statement.</span></span>
<span data-ttu-id="01529-108">Если используемый целевой компьютер не предоставляет эти сведения, `-1` возвращается.</span><span class="sxs-lookup"><span data-stu-id="01529-108">If the target machine being used does not provide this information, then `-1` is returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="01529-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="01529-109">See Also</span></span>

- [<span data-ttu-id="01529-110">Microsoft. тактов. Environment. Жеткубитсаваилаблетоборров</span><span class="sxs-lookup"><span data-stu-id="01529-110">Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow</span></span>](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)