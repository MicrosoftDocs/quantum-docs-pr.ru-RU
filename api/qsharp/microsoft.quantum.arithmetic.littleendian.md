---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Определяемый пользователем тип Литтлиндиан
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: fd2744a8372793ad01d1391c035c64de1264d2f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731465"
---
# <a name="littleendian-user-defined-type"></a>Определяемый пользователем тип Литтлиндиан

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Регистр кодирует целое число без знака в порядке с прямым порядком байтов. Кубит с индексом `0` кодирует наименьший бит целого числа без знака.

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Remarks

Мы предлагаем сокращение, `LittleEndian` как `LE` в документации.