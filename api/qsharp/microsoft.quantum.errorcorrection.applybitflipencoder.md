---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Операция Апплибитфлипенкодер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: e56e84effa001f104bbd5e28e7181dbd39a4cf5e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201297"
---
# <a name="applybitflipencoder-operation"></a><span data-ttu-id="2462c-102">Операция Апплибитфлипенкодер</span><span class="sxs-lookup"><span data-stu-id="2462c-102">ApplyBitFlipEncoder operation</span></span>

<span data-ttu-id="2462c-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="2462c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="2462c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2462c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2462c-105">Закрытая операция, используемая для реализации кодировщика и декодера битовой перелистывания.</span><span class="sxs-lookup"><span data-stu-id="2462c-105">Private operation used to implement both the bit flip encoder and decoder.</span></span>

<span data-ttu-id="2462c-106">Обратите внимание, что этот кодировщик может использовать восстановление с согласованием на месте, в этом случае это вызовет ошибку, описанную в начальном состоянии `auxQubits` .</span><span class="sxs-lookup"><span data-stu-id="2462c-106">Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`.</span></span>
<span data-ttu-id="2462c-107">В частности, если `auxQubits` изначально находится в состоянии $ \кет {10} $, это вызовет ошибку $X _1 $ в кодированном кубит.</span><span class="sxs-lookup"><span data-stu-id="2462c-107">In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.</span></span>

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="2462c-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2462c-108">Input</span></span>

### <a name="coherentrecovery--bool"></a><span data-ttu-id="2462c-109">Кохерентрековери: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2462c-109">coherentRecovery : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="data--qubit"></a><span data-ttu-id="2462c-110">данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2462c-110">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="scratch--qubit"></a><span data-ttu-id="2462c-111">Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2462c-111">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="2462c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2462c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="2462c-113">Ссылки</span><span class="sxs-lookup"><span data-stu-id="2462c-113">References</span></span>

- <span data-ttu-id="2462c-114">ДОИ: 10.1103/Фисрева. 85.044302</span><span class="sxs-lookup"><span data-stu-id="2462c-114">doi:10.1103/PhysRevA.85.044302</span></span>