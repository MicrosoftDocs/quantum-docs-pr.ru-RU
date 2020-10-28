---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: Функция Думпмачине
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: c85cf6764bdc913a71448c525318f45743bf1df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712877"
---
# <a name="dumpmachine-function"></a>Функция Думпмачине

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Remarks

Этот метод позволяет вывести сведения о текущем состоянии целевого компьютера в файл или в другое расположение.
Фактически сформированные сведения и семантика `location` относятся к каждому целевому компьютеру. Однако предоставление пустого кортежа в качестве расположения ( `()` ) или просто пропуск `location` параметра обычно означает создание выходных данных в консоли.

Для локального симулятора полного состояния, распространяемого в составе пакета средств разработки такта, этот метод ожидает строку с путем к файлу, в котором она будет записывать функцию Wave как одномерный массив комплексных чисел, в котором каждый элемент представляет амплитуды вероятности измерения соответствующего состояния.