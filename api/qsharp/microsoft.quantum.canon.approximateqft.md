---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Операция Аппроксиматекфт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: ffa3a3737a43fbe6acc57700ae122a13586482e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716770"
---
# <a name="approximateqft-operation"></a>Операция Аппроксиматекфт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Примените примерное преобразование Фурье (АКФТ) к тактовому регистру.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)

параметр аппроксимации, определяющий уровень управляемых поворотов Z, происходящих в цепи Кфт.

Параметр аппроксимации определяет уровень очистки поворотов по оси Z, т. е. ∈ {0.. n} и все повороты Z 2π/2000, где k>a удаляется из канала Кфт. Известно, что для k >= log ₂ (n) + log ₂ (1/ε) + 3 можно привязать | | КФТ-АКФТ | |<ε.


### <a name="qs--bigendian"></a>QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Регистр такта в n Кубитс, к которому применяется приблизительное преобразование тактов в виде Фурье.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

АКФТ требует использования шлюзов Z в форме 2π/2000 и Хадамард Gates.

Предполагается, что входные и выходные данные кодируются в кодировке с обратным порядком байтов.

## <a name="references"></a>Ссылки

- [*M. роеттелер, TH. Бет* , прим. \ ENG. коммун. Учет. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. копперсмис* арксив: Куант-pH/0201067v1](https://arxiv.org/abs/quant-ph/0201067)