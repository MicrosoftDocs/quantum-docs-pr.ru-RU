---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: Функция Фивекубиткоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 7509de880b1e3ea8964b61e4b3f034ce20b2f202
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712345"
---
# <a name="fivequbitcode-function"></a>Функция Фивекубиткоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Возвращает значение КЕКК, представляющее ⟦ 5, 1, 3 ⟧ кодировщика кода и декодер с измерением синдром "на месте".

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a>Выходные данные: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Возвращает реализацию кода исправления ошибки такта путем указания `QECC` типа.

## <a name="remarks"></a>Remarks

Этот код был найден независимо в следующих двух документах:

- В. З. Беннет, D. Дивинцензо, J. A. Смолин и W. K. Вуттерс, "смешанное состояние замкнутые и исправление ошибок такта", "инвентаризационная. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 и
- Ф. ЛаФламме, C. Микуел, J. P. Пас и W. H. Зурек, «отличный код исправления тактовой ошибки», «инвентаризационная. Rev. Летт. 77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019