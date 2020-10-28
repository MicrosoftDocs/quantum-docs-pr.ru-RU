---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Операция Аппликсконтролледонтрустабле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 73d63936f02a52dfbbad7b8575110177a9e4463d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733929"
---
# <a name="applyxcontrolledontruthtable-operation"></a>Операция Аппликсконтролледонтрустабле

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакеты [](https://nuget.org/packages/)


Применяет @"microsoft.quantum.intrinsic.x" операцию к `target` , если логическая функция `func` возвращает значение true для классического назначения в `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="description"></a>Описание

Операция реализует единую операцию \бегин{алигн} У\кет {x} \ Сисакет {y} = \кет{КС}\кет{и \оплус f (x)} \енд{алигн}, где $x $ and $y $ представляют `controlRegister` и `target` соответственно.

Логическая функция $f $ представлена в виде таблицы истинности с точки зрения длинного целого числа.
Например, функция большинства для трех входов представлена битстринг `11101000` , где наиболее значащий бит `1` соответствует назначению ввода `(1, 1, 1)` , а наименее значащий бит `0` соответствует назначению ввода `(0, 0, 0)` .
Оно может представляться большим целым числом `0xE8L` в шестнадцатеричной нотации или `232L` в виде десятичной нотации.  `L`Суффикс указывает, что константа имеет тип `BigInt` .
Дополнительные сведения об этом представлении можно найти в [таблице истинности Ката](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).

В реализации используются @"microsoft.quantum.intrinsic.cnot" @"microsoft.quantum.intrinsic.r1" шлюзы и.

## <a name="input"></a>Входные данные

### <a name="func--bigint"></a>Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Логическая таблица истинности, представленная как большое целое число


### <a name="controlregister--qubit"></a>Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация элемента управления Кубитс


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- [*N. счуч* , *J. сиеверт* , прл 91, No 027902, 2003, арксив: Куант-pH/0303063](https://arxiv.org/abs/quant-ph/0303063)
- [*Матиас соекен* , *Мартен роеттелер* , арксив: 2005.12310](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. синтез. Аппликсконтролледонтрустаблевисклеантаржет](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)