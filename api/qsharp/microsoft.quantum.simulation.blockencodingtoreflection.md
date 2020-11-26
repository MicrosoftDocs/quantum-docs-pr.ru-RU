---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Функция Блоккенкодингторефлектион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: 742d4f5623c7c26810998f6c96e2c7b05cc452d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225352"
---
# <a name="blockencodingtoreflection-function"></a>Функция Блоккенкодингторефлектион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует `BlockEncoding` в эквивалентный `BLockEncodingReflection` .

То есть, учитывая `BlockEncoding` единое $U $, которое кодирует некоторый оператор $H $ of, преобразует его в `BlockEncodingReflection` $U "$, который кодирует тот же оператор, но также удовлетворяет $U" ^ \Дагжер = U "$.
Это увеличивает размер дополнительного регистра $U $ на один кубит.

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Входные данные

### <a name="blockencoding--blockencoding"></a>Блоккенкодинг: [блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)

`BlockEncoding`Единое $U $ для преобразования в отражение.



## <a name="output--blockencodingreflection"></a>Выходные данные: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Единая $U "$ действует совместно с регистрами `a` и `s` блок-кодировка $H $ и соответствует $U" ^ \Дагжер = U "$.

## <a name="remarks"></a>Комментарии

Это увеличивает размер дополнительного регистра $U $ на один кубит.

## <a name="references"></a>Ссылки

- Имитация хамилтониан с Кубитизатион Guang Хао Low, Исаак L. Чжуанский https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. тактов. моделирование. Блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)