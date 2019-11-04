---
title: Язык программирования Q# | Документация Майкрософт
description: Язык программирования Q#
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: 560926f6f3e05c32a935f01ca5107a614e743ee2
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442470"
---
# <a name="the-q-programming-language"></a><span data-ttu-id="ba0bb-103">Язык программирования Q#</span><span class="sxs-lookup"><span data-stu-id="ba0bb-103">The Q# Programming Language</span></span>

## <a name="introduction"></a><span data-ttu-id="ba0bb-104">Введение</span><span class="sxs-lookup"><span data-stu-id="ba0bb-104">Introduction</span></span>

<span data-ttu-id="ba0bb-105">Естественная модель для квантовых вычислений состоит в том, чтобы рассматривать квантовый компьютер как сопроцессор, подобный тому, который используется для GPU, ППВМ и других вспомогательных процессоров.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-105">A natural model for quantum computation is to treat the quantum computer as a coprocessor, similar to that used for GPUs, FPGAs, and other adjunct processors.</span></span>
<span data-ttu-id="ba0bb-106">Первичная логика управления запускает классический код на классическом "основном" компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-106">The primary control logic runs classical code on a classical "host" computer.</span></span>
<span data-ttu-id="ba0bb-107">При необходимости основная программа может вызвать подпрограмму, которая выполняется на вспомогательном процессоре.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-107">When appropriate and necessary, the host program can invoke a subroutine that runs on the adjunct processor.</span></span>
<span data-ttu-id="ba0bb-108">После завершения выполнения подпрограммы основная программа получает доступ к результатам подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-108">When the subroutine completes, the host program gets access to the subroutine's results.</span></span>

<span data-ttu-id="ba0bb-109">Q# (Q-sharp) — это язык программирования для определенного домена, используемый для выражения квантовых алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-109">Q# (Q-sharp) is a domain-specific programming language used for expressing quantum algorithms.</span></span>
<span data-ttu-id="ba0bb-110">Он используется для написания подпрограмм, выполняемых на вспомогательном квантовом процессоре под управлением классической основной программы и компьютера.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-110">It is to be used for writing subroutines that execute on an adjunct quantum processor, under the control of a classical host program and computer.</span></span>
<span data-ttu-id="ba0bb-111">Пока квантовые процессоры не будут широко доступны, подпрограммы Q # выполняются в симуляторе.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-111">Until quantum processors are widely available, Q# subroutines execute on a simulator.</span></span>

<span data-ttu-id="ba0bb-112">Q # предоставляет небольшой набор примитивных типов, а также два способа (массивы и кортежи) для создания новых структурированных типов.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-112">Q# provides a small set of primitive types, along with two ways (arrays and tuples) for creating new, structured types.</span></span>
<span data-ttu-id="ba0bb-113">Он поддерживает базовую процедурную модель для написания программ, с циклами и операторами "if/then" (если/тогда).</span><span class="sxs-lookup"><span data-stu-id="ba0bb-113">It supports a basic procedural model for writing programs, with loops and if/then statements.</span></span>
<span data-ttu-id="ba0bb-114">Конструкции верхнего уровня в Q # представляют собой определяемые пользователем типы, операции и функции.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-114">The top-level constructs in Q# are user defined types, operations, and functions.</span></span>

<span data-ttu-id="ba0bb-115">Подробные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ba0bb-115">The following sections detail:</span></span>
- [<span data-ttu-id="ba0bb-116">Модель типов</span><span class="sxs-lookup"><span data-stu-id="ba0bb-116">The Type Model</span></span>](xref:microsoft.quantum.language.type-model)
- [<span data-ttu-id="ba0bb-117">Выражения</span><span class="sxs-lookup"><span data-stu-id="ba0bb-117">Expressions</span></span>](xref:microsoft.quantum.language.expressions)
- [<span data-ttu-id="ba0bb-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="ba0bb-118">Statements</span></span>](xref:microsoft.quantum.language.statements)
- [<span data-ttu-id="ba0bb-119">Структура файла</span><span class="sxs-lookup"><span data-stu-id="ba0bb-119">File Structure</span></span>](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a><span data-ttu-id="ba0bb-120">Соглашения</span><span class="sxs-lookup"><span data-stu-id="ba0bb-120">Conventions</span></span>

<span data-ttu-id="ba0bb-121">Мы работаем над тем, чтобы во всех ситуациях использовались обычные знаки препинания.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-121">We are working to ensure that common punctuation marks are used consistently in all situations.</span></span>
<span data-ttu-id="ba0bb-122">Мы ожидаем, что это облегчит изучение и чтение Q #, потому что эти знаки всегда означают одно и то же, и одна и та же концепция всегда представляется одинаково.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-122">We expect that this will make Q# easier to learn and to read because these marks always mean the same thing, and the same concept is always represented the same way.</span></span>

<span data-ttu-id="ba0bb-123">В частности:</span><span class="sxs-lookup"><span data-stu-id="ba0bb-123">Specifically:</span></span>

- <span data-ttu-id="ba0bb-124">Точка с запятой, `;`, используется для завершения инструкции или однострочной директивы.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-124">The semi-colon, `;`, is used to end a statement or single-line directive.</span></span>
  <span data-ttu-id="ba0bb-125">Она не должена использоваться для других целей.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-125">It is not used for any other purpose.</span></span>
- <span data-ttu-id="ba0bb-126">Запятая, `,`, используется для разделения элементов последовательности.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-126">The comma, `,`, is used to separate elements of a sequence.</span></span> <span data-ttu-id="ba0bb-127">Она используется для литералов кортежа, литералов массивов, списков аргументов, определений кортежей и списков типов.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-127">It is used for tuple literals, array literals, argument lists, tuple definitions, and type lists.</span></span> <span data-ttu-id="ba0bb-128">**В изменениях более ранних версий `;` больше не поддерживается в качестве разделителя литерала массива.**</span><span class="sxs-lookup"><span data-stu-id="ba0bb-128">**In a change from earlier versions, `;` is no longer supported as an array literal separator.**</span></span>
- <span data-ttu-id="ba0bb-129">Двоеточие, `:`, используется для представления заметки типа.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-129">The colon, `:`, is used to introduce a type annotation.</span></span> <span data-ttu-id="ba0bb-130">Оно в основном используется в вызываемых сигнатурах.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-130">It is primarily used in callable signatures.</span></span>
  <span data-ttu-id="ba0bb-131">Поскольку двоеточие всегда представляет сигнатуру типа, тернарный условный оператор, представленный в версии 0.3, использует вертикальную черту, `|`, для разделения значений true и false. Таким образом, Q # использует `cond ? tval | fval` вместо двоеточия в качестве разделителя, как в C.</span><span class="sxs-lookup"><span data-stu-id="ba0bb-131">Because colon always introduces a type signature, the ternary conditional operator introduced in 0.3 uses a vertical bar, `|`, to separate the true and false values; thus, Q# uses `cond ? tval | fval` instead of the colon as separator as in C.</span></span>
  
