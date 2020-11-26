---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Операция Апплимултиконтролледка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 28797583c23e21eb4bcae996a34c70ee06c6dbe8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209287"
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



## <a name="remarks"></a>Комментарии

Эта операция использует только чистый анЦилла Кубитс.

Описание и схема схемы см. на рис. 4,10 раздела 4,3 в Nielsen & Чжуанский

## <a name="references"></a>Ссылки

- [*Майкл A. Nielsen, Исаак L. Чжуанский*, вычисление такта и сведения о такте](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплимултиконтролледк](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)