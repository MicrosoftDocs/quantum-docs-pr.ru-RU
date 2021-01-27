---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: Операция Апплибитфлипенкодер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: cc70cc409cb472a747899838d3a9ad2d78f6b5ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827698"
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