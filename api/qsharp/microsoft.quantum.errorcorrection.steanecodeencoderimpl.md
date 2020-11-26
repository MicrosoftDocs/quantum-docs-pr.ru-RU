---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Операция Стеанекодинкодеримпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 3a9a1b11ed9255f18135e3717de7e9e1ec891298
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200431"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="11e7e-102">Операция Стеанекодинкодеримпл</span><span class="sxs-lookup"><span data-stu-id="11e7e-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="11e7e-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="11e7e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="11e7e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11e7e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11e7e-105">Закрытая операция, используемая для реализации кодировщика кода Стеане и декодера.</span><span class="sxs-lookup"><span data-stu-id="11e7e-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="11e7e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="11e7e-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="11e7e-107">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="11e7e-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="11e7e-108">массив, содержащий 1 кубит, который является входным кубит.</span><span class="sxs-lookup"><span data-stu-id="11e7e-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="11e7e-109">Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="11e7e-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="11e7e-110">массив, содержащий 6 Кубитс, которые добавляют избыточность.</span><span class="sxs-lookup"><span data-stu-id="11e7e-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="11e7e-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="11e7e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

