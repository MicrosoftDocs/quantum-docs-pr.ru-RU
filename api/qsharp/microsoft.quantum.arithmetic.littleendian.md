---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Определяемый пользователем тип Литтлиндиан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 2a00e499bf59e6d22a774706331737461e8e95e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222785"
---
# <a name="littleendian-user-defined-type"></a>Определяемый пользователем тип Литтлиндиан

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Регистр кодирует целое число без знака в порядке с прямым порядком байтов. Кубит с индексом `0` кодирует наименьший бит целого числа без знака.

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Комментарии

Мы предлагаем сокращение, `LittleEndian` как `LE` в документации.