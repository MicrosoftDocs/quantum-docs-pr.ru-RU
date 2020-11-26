---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Функция Думпмачине
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: e7eb2dfce060b61e27deae31e3c1fc6dc3d7655c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202113"
---
# <a name="dumpmachine-function"></a>Функция Думпмачине

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Выводит дамп текущего состояния целевого компьютера.

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a>Входные данные

### <a name="location--t"></a>Расположение: не

Содержит сведения о том, где создать дамп компьютера.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

Отсутствует.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Комментарии

Этот метод позволяет вывести сведения о текущем состоянии целевого компьютера в файл или в другое расположение.
Фактически сформированные сведения и семантика `location` относятся к каждому целевому компьютеру. Однако предоставление пустого кортежа в качестве расположения ( `()` ) или просто пропуск `location` параметра обычно означает создание выходных данных в консоли.

Для локального симулятора полного состояния, распространяемого в составе пакета средств разработки такта, этот метод ожидает строку с путем к файлу, в котором она будет записывать функцию Wave как одномерный массив комплексных чисел, в котором каждый элемент представляет амплитуды вероятности измерения соответствующего состояния.