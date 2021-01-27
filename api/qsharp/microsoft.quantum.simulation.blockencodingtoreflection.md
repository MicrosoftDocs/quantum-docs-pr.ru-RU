---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Функция Блоккенкодингторефлектион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: bada0dcc54d2a8d67cf7383d7153c7f46a4a8415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847260"
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

## <a name="remarks"></a>Remarks

Это увеличивает размер дополнительного регистра $U $ на один кубит.

## <a name="references"></a>Ссылки

- Имитация хамилтониан с Кубитизатион Guang Хао Low, Исаак L. Чжуанский https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. тактов. моделирование. Блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)