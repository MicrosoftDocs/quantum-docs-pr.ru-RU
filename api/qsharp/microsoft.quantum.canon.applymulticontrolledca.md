---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Операция Апплимултиконтролледка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: a6549084b1c2fda885823f451d17f9c2ebbb4600
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841692"
---
# <a name="applymulticontrolledca-operation"></a>Операция Апплимултиконтролледка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет версию управляемой операции с одной операцией умножения.
Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="singlycontrolledop--qubit--unit--is-adj"></a>Сингликонтролледоп: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

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

- [*Майкл A. Nielsen, Исаак L. Чжуанский*, вычисление такта и сведения о такте](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплимултиконтролледк](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)