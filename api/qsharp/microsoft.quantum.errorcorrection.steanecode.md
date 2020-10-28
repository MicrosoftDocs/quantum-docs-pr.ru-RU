---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Функция Стеанекоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: ea36320fff1f0c24426e2fcead976ef051d6699f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712178"
---
# <a name="steanecode-function"></a>Функция Стеанекоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Возвращает значение CSS, представляющее кодировщик кода ⟦ 7, 1, 3 ⟧ Стеане и декодер с измерением синдром на месте.

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a>Выходные данные: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Объект типа CSS, который собирает все релевантные данные для выполнения кодирования и исправления ошибок для ⟦ 7, 1, 3 ⟧ Стеане Code.

## <a name="remarks"></a>Remarks

Этот код был найден в следующем документе:

- А. Стеане, "множественные помехи частиц и исправление ошибок такта", proc. Рой. SoC. Лонд. A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.