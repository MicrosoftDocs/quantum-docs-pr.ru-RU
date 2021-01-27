---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Операция Аппроксиматекфт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 31fd87c0f61292142c7493cc29cad1082a9a2d67
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850322"
---
# <a name="approximateqft-operation"></a>Операция Аппроксиматекфт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Примените примерное преобразование Фурье (АКФТ) к тактовому регистру.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
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

- [*M. роеттелер, TH. Бет*, прим. \ ENG. коммун. Учет. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. копперсмис* арксив: Куант-pH/0201067v1](https://arxiv.org/abs/quant-ph/0201067)