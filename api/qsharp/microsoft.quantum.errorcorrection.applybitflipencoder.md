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
# <a name="applybitflipencoder-operation"></a>Операция Апплибитфлипенкодер

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Закрытая операция, используемая для реализации кодировщика и декодера битовой перелистывания.

Обратите внимание, что этот кодировщик может использовать восстановление с согласованием на месте, в этом случае это вызовет ошибку, описанную в начальном состоянии `auxQubits` .
В частности, если `auxQubits` изначально находится в состоянии $ \кет {10} $, это вызовет ошибку $X _1 $ в кодированном кубит.

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="coherentrecovery--bool"></a>Кохерентрековери: [bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="data--qubit"></a>данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="scratch--qubit"></a>Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- ДОИ: 10.1103/Фисрева. 85.044302