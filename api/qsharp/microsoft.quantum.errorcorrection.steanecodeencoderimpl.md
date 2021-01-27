---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Операция Стеанекодинкодеримпл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 81abe75e2a315fe9a994147242f3c8c9bde586ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824724"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="d33d3-102">Операция Стеанекодинкодеримпл</span><span class="sxs-lookup"><span data-stu-id="d33d3-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="d33d3-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d33d3-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d33d3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d33d3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d33d3-105">Закрытая операция, используемая для реализации кодировщика кода Стеане и декодера.</span><span class="sxs-lookup"><span data-stu-id="d33d3-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="d33d3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d33d3-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="d33d3-107">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d33d3-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d33d3-108">массив, содержащий 1 кубит, который является входным кубит.</span><span class="sxs-lookup"><span data-stu-id="d33d3-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="d33d3-109">Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d33d3-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d33d3-110">массив, содержащий 6 Кубитс, которые добавляют избыточность.</span><span class="sxs-lookup"><span data-stu-id="d33d3-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d33d3-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d33d3-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

