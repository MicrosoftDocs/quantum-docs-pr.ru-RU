---
uid: Microsoft.Quantum.Canon.AndLadder
title: Операция Андладдер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 2c6114ec8a5caabdeea8ab7e26a4877e1633671c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209729"
---
# <a name="andladder-operation"></a>Операция Андладдер

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет управляемый "и" лестницу "для регистра целевых Кубитс.

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj
```


## <a name="description"></a>Описание

Эта операция применяет преобразование, описываемое в следующем сопоставлении вычислительной области, $ $ \бегин{алигн} \кет{КС \_ 1, \дотс, x \_ n} \кет{и \_ 1, \дотс, y \_ {n-1}} \мапсто \кет{КС \_ 1, \дотс, x \_ n} \кет{y \_ 1 \оплус (x \_ 1 \ланд x \_ 2), \дотс, y \_ {n-1} \оплус (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{align} $ $ WHERE $ \ket{x \_ 1, \dots, x \_ n} $ относится к вычислительным состояниям `controls` и где $ \ket{y \_ 1, \dots, y \_ {n-1}} $ относится к вычислительным состояниям `targets` .

## <a name="input"></a>Входные данные

### <a name="ccnot--ccnotop"></a>ккнот: [ккнотоп](xref:Microsoft.Quantum.Canon.CCNOTop)

Шлюз ККНОТ, используемый для создания.


### <a name="controls--qubit"></a>элементы управления: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс, который будет использоваться в качестве элементов управления для и в лестнице.
Эта операция оставляет основные состояния вычисления `controls` инвариантного.
Длина `controls` должна быть не меньше 2 и должна быть равна единице плюс длина `targets` .


### <a name="targets--qubit"></a>целевые объекты: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Длина `targets` должна быть не меньше 1 и равна длине `controls` минус единица.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

- Используется как часть <xref:microsoft.quantum.canon.applymulticontrolledc> и <xref:microsoft.quantum.canon.applymulticontrolledca> .
- Описание и схема схемы см. на рис. 4,10 раздела 4,3 в Nielsen & Чжуанский.

## <a name="references"></a>Ссылки

- [*Майкл A. Nielsen, Исаак L. Чжуанский*, вычисление такта и сведения о такте](http://doi.org/10.1017/CBO9780511976667)