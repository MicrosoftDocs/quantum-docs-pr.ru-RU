---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Операция Апплиннертткаддервисауткарри
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 3335c63b8509090deed1172419158da0d5e80409
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731865"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a>Операция Апплиннертткаддервисауткарри

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Реализует функцию внутреннего сложения для операции Рипплекарряддернокарриттк. Это внутренняя операция, которая сопряжена с внешней операцией для создания полной Adder.

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит Зарегистрируйте первый целочисленный вход слагаемому в Рипплекарряддернокарриттк.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Литтлиндиан кубит регистрирует второе целое число входных слагаемому в Рипплекарряддернокарриттк.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Указанная управляемая операция использует симметрию и взаимную отмену операций для улучшения реализации по умолчанию, добавляющей элемент управления в каждую операцию.

## <a name="references"></a>Ссылки

- Ясухиро Такахаши, Сеиичиро Тани, Нобору Кунихиро: "каналы добавления тактов и неограниченный вентилятор", сведения о такте и вычисление, vol. 10, 2010.
  https://arxiv.org/abs/0910.2530