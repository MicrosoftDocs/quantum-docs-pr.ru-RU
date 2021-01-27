---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Операция Аппликсконтролледонтрустабле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 6e956038f7cd15db7348ff830da8bc9eae53aa61
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855564"
---
# <a name="applyxcontrolledontruthtable-operation"></a>Операция Аппликсконтролледонтрустабле

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет @"microsoft.quantum.intrinsic.x" операцию к `target` , если логическая функция `func` возвращает значение true для классического назначения в `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
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

- [*N. счуч*, *J. сиеверт*, прл 91, No 027902, 2003, арксив: Куант-pH/0303063](https://arxiv.org/abs/quant-ph/0303063)
- [*Матиас соекен*, *Мартен роеттелер*, арксив: 2005.12310](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. синтез. Аппликсконтролледонтрустаблевисклеантаржет](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)