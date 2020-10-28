---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: Функция Думпрегистер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: a6d29dbf0525077fd804563f85f189740fdc0429
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712836"
---
# <a name="dumpregister-function"></a>Функция Думпрегистер

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Выводит состояние текущего целевого компьютера, связанного с заданным Кубитс.

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="location--t"></a>Расположение: не

Содержит сведения о том, где можно создать дамп состояния.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Список Кубитс для отчета.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

Отсутствует.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Этот метод позволяет сохранить дамп сведений, связанных с состоянием заданного Кубитс, в файл или в другое расположение.
Фактически сформированные сведения и семантика `location` относятся к каждому целевому компьютеру. Однако предоставление пустого кортежа в качестве расположения ( `()` ) обычно означает создание выходных данных в консоли.

Для локального симулятора полного состояния, распространяемого в составе пакета средств разработки тактов, этот метод ожидает строку с путем к файлу, в котором он будет записывать состояние данного Кубитс (т. е. Функция Wave соответствующей подсистемы) как одномерный массив комплексных чисел, в котором каждый элемент представляет амплитуды вероятности измерения соответствующего состояния.
Если заданный Кубитс запутанными с другим кубит и их состояние нельзя разделить, то просто сообщает, что Кубитс являются запутанными.