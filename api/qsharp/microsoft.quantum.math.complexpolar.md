---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Определяемый пользователем тип Комплексполар
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709644"
---
# <a name="complexpolar-user-defined-type"></a>Определяемый пользователем тип Комплексполар

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


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