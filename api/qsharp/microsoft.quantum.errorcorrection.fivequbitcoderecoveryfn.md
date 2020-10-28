---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: Функция Фивекубиткодерековерифн
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 5b8afe222d197eb7d342ac45f027f2de9130b61a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712331"
---
# <a name="fivequbitcoderecoveryfn-function"></a>Функция Фивекубиткодерековерифн

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Функция возвращает функцию, которая сопоставляет измерения Error синдром с соответствующими операторами Паули с ошибками по таблице уточняющих запросов для ⟦ 5, 1, 3 ⟧ тактового кода.

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Функция типа `RecoveryFn` , которая принимает синдром измерение `Result[]` и возвращает `Pauli[]` операторы, которые исправляет обнаруженную ошибку.

## <a name="remarks"></a>Remarks

Просматривая все ошибки веса $1 $, мы получаем общую сумму в $3 – раз 5 = 15 $ возможные нетривиальные синдромес.
Вместе с удостоверением создается таблица ошибок и соответствующих синдром. Для 5-кубит кода, который получает эта таблица: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ с $Y _i $ получено путем добавления $X _i $ и $Z _i $ синдромес. Обратите внимание, что порядок в восстановлении таблицы подстановки задается путем преобразования битвекторс в целые числа (с прямым порядком байтов).

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)