---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Операция Апплитотаил
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850439"
---
# <a name="applytotail-operation"></a>Операция Апплитотаил

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к последнему элементу массива.

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будет применен последний объект `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="example"></a>Пример

Следующие фрагменты кода Q # эквивалентны:

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитотаила](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [Microsoft. тактов. Canon. Апплитотаилк](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [Microsoft. тактов. Canon. Апплитотаилка](xref:Microsoft.Quantum.Canon.ApplyToTailCA)