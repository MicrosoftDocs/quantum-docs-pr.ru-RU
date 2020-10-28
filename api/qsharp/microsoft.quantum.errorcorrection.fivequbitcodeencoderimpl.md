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
# <a name="fivequbitcodeencoderimpl-operation"></a>Операция Фивекубиткодинкодеримпл

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Закрытая операция, используемая для реализации кодировщика и декодера 5 кубит.

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="data--qubit"></a>данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

массив, содержащий 1 кубит, который является входным кубит.


### <a name="scratch--qubit"></a>Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

массив, содержащий 4 Кубитс, который добавим избыточность.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Выбранный кодировщик взят из бумаги V. Клиучников и D. Маслов, "Оптимизация Клиффордных цепей," инвентаризационная. Rev. инвентаризационная. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Рис. 4b) и требует всего 11 шлюзов.