---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode операция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 273692efa629cb8cc20069ef500c4e0902fbc3ff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201348"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a>_ExtractLogicalQubitFromSteaneCode операция

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Синдром измерение и обратное внедрение.

$X $-and $Z $-стабилизерс не обрабатываются одинаково, что обусловлено определенным выбором канала кодирования.
Эта асимметрию приводит к другой подпрограммы извлечения синдром.
Можно измерить синдром, изменив оператор Multi-кубит Паули непосредственно в состоянии кода, но для цели «по-прежнему» логическая кубит возвращается в один кубит, в рамках которого измерения синдром могут быть выполнены без дополнительных анЦиллас.

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a>Входные данные

### <a name="code--logicalregister"></a>код: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)





## <a name="output--qubitintint"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

Логические кубит и пара целых чисел для $X $-синдром и $Z $-синдром.
Они представляют индекс кода кубит, в котором одна $X $-или $Z $-Error вызывала измеряемый синдром.

## <a name="remarks"></a>Комментарии

Обратите внимание, что эта операция не помечена как `internal` , так как модульные тесты непосредственно зависят от этой операции. В качестве будущего улучшения модульные тесты должны быть подвергнуты рефакторингу, чтобы они зависели только от открытых вызываемых.

> [!WARNING]
> Эта подпрограмма адаптирована к определенному каналу кодирования для кода Стеане 7 кубит; Если канал кодирования изменен, результат синдром может быть интерпретирован иначе.