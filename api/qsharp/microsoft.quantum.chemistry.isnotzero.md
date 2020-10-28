---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Функция Иснотзеро
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 3c0f9c6695e8c9ec4a0953d5217c28c512ac7de1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714824"
---
# <a name="isnotzero-function"></a>Функция Иснотзеро

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакеты [](https://nuget.org/packages/)


Проверяет `Double` , не равен ли число приблизительно нулю.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="number--double"></a>число: [Double](xref:microsoft.quantum.lang-ref.double)

Число для проверки



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

Возвращает значение true `number` , если имеет абсолютное значение больше `1e-15` .