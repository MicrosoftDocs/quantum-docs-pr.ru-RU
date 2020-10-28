---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Операция Апплимултиконтролледка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 5662efe0dc6f665206b8773596bf885ce631413c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717960"
---
# <a name="applymulticontrolledca-operation"></a>Операция Апплимултиконтролледка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет версию управляемой операции с одной операцией умножения.
Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="singlycontrolledop--qubit--unit-adj"></a>Сингликонтролледоп: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция, управляемая для одного кубит.
Первым кубит в аргументе операции считается элемент управления, а остальные считаются целевыми Кубитс.
`ApplyMultiControlled` всегда вызывает `singlyControlledOp` аргумент длиной не менее 1.


### <a name="ccnot--ccnotop"></a>ккнот: [ккнотоп](xref:Microsoft.Quantum.Canon.CCNOTop)

Шлюз с управляемым контролем, не используемый для построения.


### <a name="controls--qubit"></a>элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс, управление которым должно осуществляться `singlyControlledOp` .
Длина `controls` должна быть не меньше 1.


### <a name="targets--qubit"></a>целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Целевой Кубитс, на `singlyControlledOp` основе которого действует.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Эта операция использует только чистый анЦилла Кубитс.

Описание и схема схемы см. на рис. 4,10 раздела 4,3 в Nielsen & Чжуанский

## <a name="references"></a>Ссылки

- [*Майкл A. Nielsen, Исаак L. Чжуанский* , вычисление такта и сведения о такте](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплимултиконтролледк](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)