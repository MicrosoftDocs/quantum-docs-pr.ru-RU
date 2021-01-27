---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: Функция Иснотзеро
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839597"
---
# <a name="isnotzero-function"></a>Функция Иснотзеро

Пространство имен: [Microsoft. тактов. Химия](xref:Microsoft.Quantum.Chemistry)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Проверяет `Double` , не равен ли число приблизительно нулю.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Входные данные

### <a name="number--double"></a>число: [Double](xref:microsoft.quantum.lang-ref.double)

Число для проверки



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

Возвращает значение true `number` , если имеет абсолютное значение больше `1e-15` .