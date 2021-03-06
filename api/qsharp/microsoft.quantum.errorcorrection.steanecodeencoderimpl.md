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
# <a name="steanecodeencoderimpl-operation"></a>Операция Стеанекодинкодеримпл

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Закрытая операция, используемая для реализации кодировщика кода Стеане и декодера.

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="data--qubit"></a>данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

массив, содержащий 1 кубит, который является входным кубит.


### <a name="scratch--qubit"></a>Рабочая область: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

массив, содержащий 6 Кубитс, которые добавляют избыточность.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

