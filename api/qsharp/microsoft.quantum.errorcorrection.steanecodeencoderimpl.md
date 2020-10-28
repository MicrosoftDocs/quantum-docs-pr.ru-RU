---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Операция Стеанекодинкодеримпл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: b843422a6007d01de9b57ec659c229b8ab0ad2e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712191"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="70284-102">Операция Стеанекодинкодеримпл</span><span class="sxs-lookup"><span data-stu-id="70284-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="70284-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="70284-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="70284-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="70284-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="70284-105">Закрытая операция, используемая для реализации кодировщика кода Стеане и декодера.</span><span class="sxs-lookup"><span data-stu-id="70284-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="70284-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="70284-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="70284-107">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="70284-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="70284-108">массив, содержащий 1 кубит, который является входным кубит.</span><span class="sxs-lookup"><span data-stu-id="70284-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="70284-109">Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="70284-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="70284-110">массив, содержащий 6 Кубитс, которые добавляют избыточность.</span><span class="sxs-lookup"><span data-stu-id="70284-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="70284-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="70284-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

