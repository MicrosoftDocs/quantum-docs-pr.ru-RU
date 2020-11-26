---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Функция Стеанекоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: b981c82acfa82cd58d82666703d4bb95ac5df280
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200481"
---
# <a name="steanecode-function"></a>Функция Стеанекоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение CSS, представляющее кодировщик кода ⟦ 7, 1, 3 ⟧ Стеане и декодер с измерением синдром на месте.

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a>Выходные данные: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

Объект типа CSS, который собирает все релевантные данные для выполнения кодирования и исправления ошибок для ⟦ 7, 1, 3 ⟧ Стеане Code.

## <a name="remarks"></a>Комментарии

Этот код был найден в следующем документе:

- A. Стеане, "множественные помехи частиц и исправление ошибок такта", proc. Рой. SoC. Лонд. A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.