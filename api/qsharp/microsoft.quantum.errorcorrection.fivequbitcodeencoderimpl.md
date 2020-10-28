---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Операция Фивекубиткодинкодеримпл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 29b0f47ddffeae3ed4dfda4084304427418e02fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712332"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="808aa-102">Операция Фивекубиткодинкодеримпл</span><span class="sxs-lookup"><span data-stu-id="808aa-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="808aa-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="808aa-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="808aa-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="808aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="808aa-105">Закрытая операция, используемая для реализации кодировщика и декодера 5 кубит.</span><span class="sxs-lookup"><span data-stu-id="808aa-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="808aa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="808aa-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="808aa-107">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="808aa-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="808aa-108">массив, содержащий 1 кубит, который является входным кубит.</span><span class="sxs-lookup"><span data-stu-id="808aa-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="808aa-109">Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="808aa-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="808aa-110">массив, содержащий 4 Кубитс, который добавим избыточность.</span><span class="sxs-lookup"><span data-stu-id="808aa-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="808aa-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="808aa-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="808aa-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="808aa-112">Remarks</span></span>

<span data-ttu-id="808aa-113">Выбранный кодировщик взят из бумаги V. Клиучников и D. Маслов, "Оптимизация Клиффордных цепей," инвентаризационная. Rev. инвентаризационная. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Рис. 4b) и требует всего 11 шлюзов.</span><span class="sxs-lookup"><span data-stu-id="808aa-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>