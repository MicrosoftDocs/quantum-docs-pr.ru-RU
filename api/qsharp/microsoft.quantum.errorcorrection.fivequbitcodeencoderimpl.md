---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Операция Фивекубиткодинкодеримпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: f70d2d1352c7b2eebee7a863eba97d78d7351dab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200855"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="fd480-102">Операция Фивекубиткодинкодеримпл</span><span class="sxs-lookup"><span data-stu-id="fd480-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="fd480-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="fd480-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="fd480-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fd480-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fd480-105">Закрытая операция, используемая для реализации кодировщика и декодера 5 кубит.</span><span class="sxs-lookup"><span data-stu-id="fd480-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="fd480-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fd480-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="fd480-107">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fd480-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fd480-108">массив, содержащий 1 кубит, который является входным кубит.</span><span class="sxs-lookup"><span data-stu-id="fd480-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="fd480-109">Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fd480-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fd480-110">массив, содержащий 4 Кубитс, который добавим избыточность.</span><span class="sxs-lookup"><span data-stu-id="fd480-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fd480-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fd480-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fd480-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd480-112">Remarks</span></span>

<span data-ttu-id="fd480-113">Выбранный кодировщик взят из бумаги V. Клиучников и D. Маслов, "Оптимизация Клиффордных цепей," инвентаризационная. Rev. инвентаризационная. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Рис. 4b) и требует всего 11 шлюзов.</span><span class="sxs-lookup"><span data-stu-id="fd480-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>