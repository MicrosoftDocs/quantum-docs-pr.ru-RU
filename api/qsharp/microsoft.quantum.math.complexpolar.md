---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Определяемый пользователем тип Комплексполар
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: a4f3a7b6ffa73271d7ac9674d8c718f6f09c0291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210987"
---
# <a name="complexpolar-user-defined-type"></a>Определяемый пользователем тип Комплексполар

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет комплексное число в полярной форме.

Полярное представление комплексного числа имеет $c = r e ^ {i t} $.

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a>Именованные элементы

### <a name="magnitude--double"></a>Величина: [Double](xref:microsoft.quantum.lang-ref.double)

Абсолютное значение $r \же $0 из $c $.
### <a name="argument--double"></a>Аргумент: [Double](xref:microsoft.quantum.lang-ref.double)

Фаза $t \ин \масбб R $ of $c $.