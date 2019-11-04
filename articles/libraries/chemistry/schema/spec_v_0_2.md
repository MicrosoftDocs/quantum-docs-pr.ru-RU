---
title: Спецификация схемы брумбридже
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
ms.openlocfilehash: 2f4be96bc6f1e8e6fe21b93bc0d9ab2aa367fd53
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185313"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="be10a-102">Спецификация брумбридже v 0,2</span><span class="sxs-lookup"><span data-stu-id="be10a-102">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="be10a-103">Ключевые слова "обязательно", "не должны", "обязательно", "должно", "не", "должно", "не должно", "рекомендуется", "Май" и "необязательно" в этом документе должны интерпретироваться, как описано в [RFC 2119](https://tools.ietf.org/html/rfc2119).</span><span class="sxs-lookup"><span data-stu-id="be10a-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="be10a-104">Любая боковая панель с заголовками «Примечание», «информация» или «предупреждение» является информативной.</span><span class="sxs-lookup"><span data-stu-id="be10a-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="be10a-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="be10a-105">Introduction</span></span> ##

<span data-ttu-id="be10a-106">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-106">This section is informative.</span></span>

<span data-ttu-id="be10a-107">Документы брумбридже предназначены для обмена экземплярами проблем моделирования в тактовой химия для обработки с помощью моделирования тактов и программирования цепочек инструментов.</span><span class="sxs-lookup"><span data-stu-id="be10a-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="be10a-108">Сериализация</span><span class="sxs-lookup"><span data-stu-id="be10a-108">Serialization</span></span> ##

<span data-ttu-id="be10a-109">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-109">This section is normative.</span></span>

<span data-ttu-id="be10a-110">Документ Брумбридже должен быть сериализован как [документ YAML 1,2](http://yaml.org/spec/) , представляющий объект JSON, как описано в [RFC 4627](https://tools.ietf.org/html/rfc4627) , раздел 2,2.</span><span class="sxs-lookup"><span data-stu-id="be10a-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="be10a-111">Объект, сериализованный в YAML, должен иметь свойство `"$schema"`, значение которого равно `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, и должно быть допустимым в соответствии со спецификацией JSON Schema-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="be10a-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="be10a-112">В оставшейся части этой спецификации объект Брумбридже будет ссылаться на объект JSON, десериализованный из документа YAML Брумбридже.</span><span class="sxs-lookup"><span data-stu-id="be10a-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="be10a-113">Если явно не указано иное, объекты не должны иметь дополнительных свойств, кроме указанных явно в этом документе.</span><span class="sxs-lookup"><span data-stu-id="be10a-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="be10a-114">Дополнительные определения</span><span class="sxs-lookup"><span data-stu-id="be10a-114">Additional Definitions</span></span> ##

<span data-ttu-id="be10a-115">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="be10a-116">Объекты Quantity</span><span class="sxs-lookup"><span data-stu-id="be10a-116">Quantity Objects</span></span> ###

<span data-ttu-id="be10a-117">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-117">This section is normative.</span></span>

<span data-ttu-id="be10a-118">_Объект Quantity_ является объектом JSON и должен иметь свойство `units`, значение которого является одним из допустимых значений, перечисленных в таблице 1.</span><span class="sxs-lookup"><span data-stu-id="be10a-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="be10a-119">Объект Quantity — это _простой объект Quantity_ , если в дополнение к свойству `units` имеется одно свойство `value`.</span><span class="sxs-lookup"><span data-stu-id="be10a-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="be10a-120">Значение свойства `value` должно быть числом.</span><span class="sxs-lookup"><span data-stu-id="be10a-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="be10a-121">Объект Quantity является _связанным объектом Quantity_ , если он содержит свойства `lower` и `upper` в дополнение к свойству `units`.</span><span class="sxs-lookup"><span data-stu-id="be10a-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="be10a-122">Значения свойств `lower` и `upper` должны быть числами.</span><span class="sxs-lookup"><span data-stu-id="be10a-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="be10a-123">Связанный объект Quantity может иметь свойство `value`, значением которого является число.</span><span class="sxs-lookup"><span data-stu-id="be10a-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="be10a-124">Объект Quantity — это _объект количества разреженных массивов_ , если он содержит свойство `format` и свойство `values` в дополнение к свойству `units`.</span><span class="sxs-lookup"><span data-stu-id="be10a-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="be10a-125">Значение `format` должно быть строкой `sparse`.</span><span class="sxs-lookup"><span data-stu-id="be10a-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="be10a-126">Значение свойства `values` должно быть массивом.</span><span class="sxs-lookup"><span data-stu-id="be10a-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="be10a-127">Каждый элемент `values` должен быть массивом, представляющим индексы, и значением количества разреженных массивов.</span><span class="sxs-lookup"><span data-stu-id="be10a-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="be10a-128">Индексы каждого элемента объекта количества разреженных массивов должны быть уникальными во всем объекте количества разреженных массивов.</span><span class="sxs-lookup"><span data-stu-id="be10a-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="be10a-129">Если индекс имеет значение `0`, то синтаксический анализатор должен обрабатывать объект Quantity разреженных массивов идентично объекту количества разреженных массивов, в котором этот индекс отсутствует.</span><span class="sxs-lookup"><span data-stu-id="be10a-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="be10a-130">Объект Quantity должен иметь значение</span><span class="sxs-lookup"><span data-stu-id="be10a-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="be10a-131">Объект простого количества,</span><span class="sxs-lookup"><span data-stu-id="be10a-131">a simple quantity object,</span></span>
- <span data-ttu-id="be10a-132">связанный объект Quantity или</span><span class="sxs-lookup"><span data-stu-id="be10a-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="be10a-133">Объект количества разреженных массивов.</span><span class="sxs-lookup"><span data-stu-id="be10a-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="be10a-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="be10a-134">Examples</span></span> ###

<span data-ttu-id="be10a-135">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-135">This section is informative.</span></span>

<span data-ttu-id="be10a-136">Простое количество, представляющее $1.9844146837\,\Масрм{ха} $:</span><span class="sxs-lookup"><span data-stu-id="be10a-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="be10a-137">Ограниченное количество, представляющее равномерное распределение по интервалу $ [-7,-6]\,\Масрм{ха} $:</span><span class="sxs-lookup"><span data-stu-id="be10a-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="be10a-138">Ниже приведено количество разреженных массивов с элементом, `[1, 2]` равным `hello`, а элемент `[3, 4]` равен `world`:</span><span class="sxs-lookup"><span data-stu-id="be10a-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="be10a-139">Раздел формата</span><span class="sxs-lookup"><span data-stu-id="be10a-139">Format Section</span></span> ##

<span data-ttu-id="be10a-140">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-140">This section is normative.</span></span>

<span data-ttu-id="be10a-141">Объект Брумбридже должен иметь свойство `format`, значение которого является объектом JSON с одним свойством, именуемым `version`.</span><span class="sxs-lookup"><span data-stu-id="be10a-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="be10a-142">Свойство `version` должно иметь значение `"0.2"`.</span><span class="sxs-lookup"><span data-stu-id="be10a-142">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="be10a-143">Пример</span><span class="sxs-lookup"><span data-stu-id="be10a-143">Example</span></span> ###

<span data-ttu-id="be10a-144">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="be10a-145">Раздел описания проблемы</span><span class="sxs-lookup"><span data-stu-id="be10a-145">Problem Description Section</span></span> ##

<span data-ttu-id="be10a-146">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-146">This section is normative.</span></span>

<span data-ttu-id="be10a-147">Объект Брумбридже должен иметь свойство `problem_description`, значение которого является массивом JSON.</span><span class="sxs-lookup"><span data-stu-id="be10a-147">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="be10a-148">Каждый элемент в значении свойства `problem_description` должен быть объектом JSON, описывающим один набор целых чисел, как описано в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="be10a-148">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="be10a-149">В оставшейся части этого раздела термин "объект описания проблемы" будет ссылаться на элемент в значении свойства `problem_description` объекта Брумбридже.</span><span class="sxs-lookup"><span data-stu-id="be10a-149">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="be10a-150">Каждый объект описания проблемы должен иметь свойство `metadata`, значение которого является объектом JSON.</span><span class="sxs-lookup"><span data-stu-id="be10a-150">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="be10a-151">Значение `metadata` может быть пустым объектом JSON (то есть `{}`) или может содержать дополнительные свойства, определенные разработчиком.</span><span class="sxs-lookup"><span data-stu-id="be10a-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="be10a-152">Раздел хамилтониан</span><span class="sxs-lookup"><span data-stu-id="be10a-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="be10a-153">Краткое описание</span><span class="sxs-lookup"><span data-stu-id="be10a-153">Overview</span></span> ####

<span data-ttu-id="be10a-154">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-154">This section is informative.</span></span>

<span data-ttu-id="be10a-155">Свойство `hamiltonian` каждого объекта описания проблемы описывает Хамилтониан для определенной проблемы такта химия, вычисляя его один-и два основных термина в виде разреженных массивов вещественных чисел.</span><span class="sxs-lookup"><span data-stu-id="be10a-155">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="be10a-156">Операторы Хамилтониан, описанные каждым объектом описания проблемы, принимают форму</span><span class="sxs-lookup"><span data-stu-id="be10a-156">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="be10a-157">$ $ H = \сум\_\{i, j\}\сум\_{\сигма\ин\\{\упарров, \довнарров\\}} H\_\{ИЖ\} а ^\{\дагжер\}\_{i , \сигма}\_{j, \сигма} + \фрак{1}{2}\сум\_\{i, j, k, l\}\сум\_{\сигма, \рхо\ин\\{\упарров, \довнарров\\}} h\_{ижкл} a ^ \дагжер\_{i , \сигма} a ^ \дагжер\_{k, \рхо}\_{l, \рхо}\_{j, \сигма}, $ $</span><span class="sxs-lookup"><span data-stu-id="be10a-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="be10a-158">Здесь $h _ {ижкл} = (ИЖ | КЛ) $ в соглашении Мулликен.</span><span class="sxs-lookup"><span data-stu-id="be10a-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="be10a-159">Для ясности термина «один электронное» —</span><span class="sxs-lookup"><span data-stu-id="be10a-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="be10a-160">$ $ H_ {ИЖ} = \инт {\масрм d} x \пси ^ \*\_i (x) \лефт (\фрак{1}{2}\набла ^ 2 + \сум\_{A} \Фрак{з\_а} {| x-x\_A |}  \ригхт) \пси\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="be10a-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="be10a-161">и два электронного выражения:</span><span class="sxs-lookup"><span data-stu-id="be10a-161">and the two-electron term is</span></span>

<span data-ttu-id="be10a-162">$ $ h\_\{ижкл\} = \иинт \{\масрм d\}x ^ 2 \пси ^\{\*\}\_i (x\_1) \пси\_j (x\_1) \фрак\{1\}\{\|x\_1-x\_2\|\}\пси\_k ^\{\*\}(x\_2) \пси\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="be10a-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="be10a-163">Как отмечалось в описании [свойства`basis_set`](#basis-set-object) каждого элемента свойства `integral_sets`, мы еще дальше предполагаю, что используемые основные функции являются реальными.</span><span class="sxs-lookup"><span data-stu-id="be10a-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="be10a-164">Это позволяет нам использовать следующие симметриес между терминами для сжатия представления Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="be10a-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="be10a-165">$ $ H_ {ижкл} = H_ {ижлк} = H_ {жикл} = H_ {жилк} = H_ {клиж} = H_ {клжи} = H_ {лкиж} = H_ {лкжи}.</span><span class="sxs-lookup"><span data-stu-id="be10a-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="be10a-166">Контент</span><span class="sxs-lookup"><span data-stu-id="be10a-166">Contents</span></span> ####

<span data-ttu-id="be10a-167">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-167">This section is normative.</span></span>

<span data-ttu-id="be10a-168">Каждый объект описания проблемы должен иметь свойство `hamiltonian`, значение которого является объектом JSON.</span><span class="sxs-lookup"><span data-stu-id="be10a-168">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="be10a-169">Значение свойства `hamiltonian` известно как объект Хамилтониан и должно иметь свойства `one_electron_integrals` и `two_electron_integrals`, как описано в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="be10a-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="be10a-170">Каждый объект описания проблемы должен иметь свойство `coulomb_repulsion`, значение которого является простым объектом Quantity.</span><span class="sxs-lookup"><span data-stu-id="be10a-170">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="be10a-171">Каждый объект описания проблемы должен иметь свойство `energy_offet`, значение которого является простым объектом Quantity.</span><span class="sxs-lookup"><span data-stu-id="be10a-171">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="be10a-172">МЕТИМ Значения `coulomb_repulsion` и `energy_offet` добавлены вместе, захватывают идентификатор удостоверения Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="be10a-172">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="be10a-173">Объект «интегралы за один электронный»</span><span class="sxs-lookup"><span data-stu-id="be10a-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="be10a-174">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-174">This section is normative.</span></span>

<span data-ttu-id="be10a-175">Свойство `one_electron_integrals` объекта Хамилтониан должно быть разреженным массивом, индексом которого является два целых числа и значения которых являются числами.</span><span class="sxs-lookup"><span data-stu-id="be10a-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="be10a-176">Каждый термин должен иметь индексы `[i, j]`, где `i >= j`.</span><span class="sxs-lookup"><span data-stu-id="be10a-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="be10a-177">МЕТИМ Это отражает симметрию, которая $h _ {ИЖ} = H_ {ji} $, что является следствием того факта, что Хамилтониан является Хермитиан.</span><span class="sxs-lookup"><span data-stu-id="be10a-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="be10a-178">Пример</span><span class="sxs-lookup"><span data-stu-id="be10a-178">Example</span></span> ######

<span data-ttu-id="be10a-179">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-179">This section is informative.</span></span>

<span data-ttu-id="be10a-180">Следующее количество разреженных массивов представляет Хамилтониан $ $ H = \лефт (-5,0 (a ^\{\дагжер\}\_{1, \упарров}\_{1, \упарров} + a ^\{\дагжер\}\_{1, \довнарров} a\_{1 , \довнарров}) + 0,17 (a ^\{\дагжер\}\_{2, \упарров} a\_{1, \упарров} + a ^\{\дагжер\}\_{1, \упарров} a\_{2, \упарров} + a ^\{\дагжер\}\_{2 , \довнарров}\_{1, \довнарров} + a ^\{\дагжер\}\_{1, \довнарров} a\_{2, \довнарров}) \ригхт)\\, \Масрм{ха}.</span><span class="sxs-lookup"><span data-stu-id="be10a-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
$$

```yaml
one_electron_integrals:     # required
    units: hartree          # required
    format: sparse          # required
    values:                 # required
        # i j f(i,j)
        - [1, 1, -5.0]
        - [2, 1,  0.17]
```
> [!NOTE]
> <span data-ttu-id="be10a-181">Брумбридже использует индексирование, основанное на 1.</span><span class="sxs-lookup"><span data-stu-id="be10a-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="be10a-182">Объект интегралов с двумя электронными данными</span><span class="sxs-lookup"><span data-stu-id="be10a-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="be10a-183">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-183">This section is normative.</span></span>

<span data-ttu-id="be10a-184">Свойство `two_electron_integrals` объекта Хамилтониан должно быть количеством разреженных массивов с одним дополнительным свойством с именем `index_convention`.</span><span class="sxs-lookup"><span data-stu-id="be10a-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="be10a-185">Каждый элемент значения `two_electron_integrals` должен иметь четыре индекса.</span><span class="sxs-lookup"><span data-stu-id="be10a-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="be10a-186">Каждое свойство `two_electron_integrals` должно иметь свойство `index_convention`.</span><span class="sxs-lookup"><span data-stu-id="be10a-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="be10a-187">Значение свойства `index_convention` должно быть одним из допустимых значений, перечисленных в таблице 1.</span><span class="sxs-lookup"><span data-stu-id="be10a-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="be10a-188">Если значение `index_convention` равно `mulliken`, то для каждого элемента `two_electron_integrals` количество разреженных массивов средство синтаксического анализа, загружая документ Брумбридже, должно создать экземпляр Хамилтониан, равный оператору Two-электронного оператора $h _ {i, j, k, l} а ^ \dagger_i a ^ \dagger_j a_k a_l $ , где $i $, $j $, $k $ и $l $ должны быть целыми числами со значением не менее 1, а $h _ {i, j, k, l} $ — это элемент `[i, j, k, l, h(i, j, k, l)]` из количества разреженных массивов.</span><span class="sxs-lookup"><span data-stu-id="be10a-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="be10a-189">симметриес</span><span class="sxs-lookup"><span data-stu-id="be10a-189">Symmetries</span></span> ######

<span data-ttu-id="be10a-190">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-190">This section is normative.</span></span>

<span data-ttu-id="be10a-191">Если свойство `index_convention` объекта `two_electron_integrals` равно `mulliken`, то при наличии элемента с индексами `[i, j, k, l]` следующие индексы не должны присутствовать, если они не равны `[i, j, k, l]`:</span><span class="sxs-lookup"><span data-stu-id="be10a-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="be10a-192">Поскольку свойство `index_convention` является объектом разреженного количества, индексы не могут повторяться в разных элементах.</span><span class="sxs-lookup"><span data-stu-id="be10a-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="be10a-193">В частности, если имеется элемент с индексами `[i, j, k, l]`, другие элементы не могут содержать эти индексы.</span><span class="sxs-lookup"><span data-stu-id="be10a-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="be10a-194">Пример</span><span class="sxs-lookup"><span data-stu-id="be10a-194">Example</span></span> #######

<span data-ttu-id="be10a-195">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-195">This section is informative.</span></span>

<span data-ttu-id="be10a-196">Следующий объект указывает Хамилтониан</span><span class="sxs-lookup"><span data-stu-id="be10a-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="be10a-197">$ $ H = \frac12 \сум\_{\сигма, \рхо\ин\\{\упарров, \довнарров\\}} \Биггр (1,6 a ^ {\дагжер}\_{1, \сигма} a ^ {\дагжер}\_{1, \рхо} a\_{1, \рхо} a\_{1, \сигма}-0,1 a ^ {\dagger}\_{6 , \сигма} a ^ {\дагжер}\_{1, \рхо}\_{3, \рхо}\_{2, \сигма}-0,1 а ^ {\дагжер}\_{6, \сигма} a ^ {\дагжер}\_{1, \рхо} a\_{2, \рхо} a\_{3 , \сигма}-0,1 a ^ {\дагжер}\_{1, \сигма} a ^ {\дагжер}\_{6, \рхо} а\_{3, \рхо} a\_{2, \сигма}-0,1 а ^ {\дагжер}\_{1, \сигма} a ^ {\дагжер}\_{6, \рхо} a\_{2 , \рхо}\_{3, \сигма} $ $ $ $-0,1 a ^ {\дагжер}\_{3, \сигма} а ^ {\дагжер}\_{2, \рхо} a\_{6, \рхо} a\_{1, \сигма}-0,1 а ^ {\дагжер}\_{3, \сигма} a ^ {\дагжер}\_{2 , \рхо}\_{1, \рхо}\_{6, \сигма}-0,1 a ^ {\дагжер}\_{2, \сигма} a ^ {\дагжер}\_{3, \рхо} а\_{6, \рхо} a\_{1, \сигма}-0,1 a ^ {\дагжер}\_{2 , \сигма} a ^ {\дагжер}\_{3, \рхо}\_{1, \рхо}\_{6, \Сигма}\биггр)\\, \Текстрм{ха}.</span><span class="sxs-lookup"><span data-stu-id="be10a-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
$$

```yaml
two_electron_integrals:
    index_convention: mulliken
    units: hartree
    format: sparse
    values:
        - [1, 1, 1, 1,  1.6]
        - [6, 1, 3, 2, -0.1]
```

### <a name="initial-state-section"></a><span data-ttu-id="be10a-198">Раздел начального состояния</span><span class="sxs-lookup"><span data-stu-id="be10a-198">Initial State Section</span></span> ###

<span data-ttu-id="be10a-199">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-199">This section is normative.</span></span>

<span data-ttu-id="be10a-200">Объект `initial_state_suggestion`, значение которого является массивом JSON, указывает начальные состояния такта, представляющие интерес для указанного Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="be10a-200">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="be10a-201">Каждый элемент в значении свойства `initial_state_suggestion` должен быть объектом JSON, описывающим одно состояние такта, как описано в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="be10a-201">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="be10a-202">В оставшейся части этого раздела термин "объект состояния" будет ссылаться на элемент в значении свойства `initial_state_suggestion` объекта Брумбридже.</span><span class="sxs-lookup"><span data-stu-id="be10a-202">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="be10a-203">Объект State</span><span class="sxs-lookup"><span data-stu-id="be10a-203">State object</span></span> ####

<span data-ttu-id="be10a-204">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-204">This section is normative.</span></span>

<span data-ttu-id="be10a-205">Каждый объект состояния должен иметь свойство `label`, содержащее строку.</span><span class="sxs-lookup"><span data-stu-id="be10a-205">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="be10a-206">Каждый объект состояния должен иметь свойство `method`.</span><span class="sxs-lookup"><span data-stu-id="be10a-206">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="be10a-207">Значение свойства `method` должно быть одним из допустимых значений, перечисленных в таблице 3.</span><span class="sxs-lookup"><span data-stu-id="be10a-207">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="be10a-208">Каждый объект состояния может иметь свойство `energy`, значение которого должно быть простым объектом Quantity.</span><span class="sxs-lookup"><span data-stu-id="be10a-208">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="be10a-209">Если значение свойства `method` равно `sparse_multi_configurational`, то объект состояния должен иметь свойство `superposition`, содержащее массив состояний и их ненормализованные амплитуды.</span><span class="sxs-lookup"><span data-stu-id="be10a-209">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="be10a-210">Например, начальное состояние $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\дагжер}\_{1, \упарров}а ^ {\дагжер}\_{2, \упарров}а ^ {\дагжер}\_{2, \довнарров}) \кет{0} $ $ $ $ \Кет{е} = \frac{0.1 (a ^ {\дагжер}\_{1 , \упарров}а ^ {\дагжер}\_{2, \упарров}а ^ {\дагжер}\_{2, \довнарров}) + 0,2 (a ^ {\дагжер}\_{1, \упарров}а ^ {\дагжер}\_{3, \упарров}а ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket{0}, $ $ где $ \Кет{е} $ имеет Energy $0,987 \Текстрм{ха} $, представлены</span><span class="sxs-lookup"><span data-stu-id="be10a-210">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "|G0>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
  - label: "|G1>"
    method: sparse_multi_configurational
    superposition:
      - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
  - label: "|G2>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
  - label: "|E>"
    energy: {units: hartree, value: 0.987}
    method: sparse_multi_configurational
    superposition:
      - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
      - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

<span data-ttu-id="be10a-211">Если значение свойства `method` `unitary_coupled_cluster`, то объект состояния должен иметь свойство `cluster_operator`, значение которого является объектом JSON.</span><span class="sxs-lookup"><span data-stu-id="be10a-211">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="be10a-212">Объект JSON должен иметь свойство `reference_state`, значение которого является состоянием основания.</span><span class="sxs-lookup"><span data-stu-id="be10a-212">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="be10a-213">Объект JSON может иметь свойство `one_body_amplitudes`, значение которого является массивом операторов кластера одного тела и их амплитудами.</span><span class="sxs-lookup"><span data-stu-id="be10a-213">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="be10a-214">Объект JSON может иметь свойство `two_body_amplitudes`, значение которого является массивом операторов кластера из двух тела и их амплитудами.</span><span class="sxs-lookup"><span data-stu-id="be10a-214">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="be10a-215">содержит массив состояний основания и их ненормализованные амплитуды.</span><span class="sxs-lookup"><span data-stu-id="be10a-215">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="be10a-216">Например, состояние $ $ \кет{\текст{референце}} = (a ^ {\дагжер}\_{1, \упарров}а ^ {\дагжер}\_{2, \упарров}а ^ {\дагжер}\_{2, \довнарров}) \ket{0}, $ $</span><span class="sxs-lookup"><span data-stu-id="be10a-216">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="be10a-217">$ $ \Кет{\текст{укксд}} = e ^ {T-T ^ \дагжер}\кет{\текст{референце}}, $ $</span><span class="sxs-lookup"><span data-stu-id="be10a-217">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="be10a-218">$ $ T = 0,1 a ^ {\дагжер}\_{3, \упарров}а\_{2, \довнарров} + 0,2 a ^ {\дагжер}\_{2, \упарров}а\_{2, \довнарров}-0,3 a ^ {\дагжер}\_{1, \упарров}а ^ {\dagger}\_{3, \downarrow}a\_{3 , \упарров}а\_{2, \довнарров} $ $ представляется</span><span class="sxs-lookup"><span data-stu-id="be10a-218">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "UCCSD"
    method: unitary_coupled_cluster
    cluster_operator: # Initial state that cluster operator is applied to.
        reference_state: 
          [1.0, "(1a)+", "(2a)+", "(2b)+", '|vacuum>']
        one_body_amplitudes: # A one-body cluster term is t^{q}_{p} a^\dag_p a_q   
            - [0.1, "(3a)+", "(2b)"]
            - [-0.2, "(2a)+", "(2b)"]
        two_body_amplitudes: # A two-body unitary cluster term is t^{rs}_{pq} a^\dag_p a^\dag_q a_r a_s
            - [-0.3, "(1a)+", "(3b)+", "(3a)", "(2b)"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="be10a-219">Объект базового набора</span><span class="sxs-lookup"><span data-stu-id="be10a-219">Basis Set Object</span></span> ####

<span data-ttu-id="be10a-220">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-220">This section is normative.</span></span>

<span data-ttu-id="be10a-221">Каждый объект описания проблемы может иметь свойство `basis_set`.</span><span class="sxs-lookup"><span data-stu-id="be10a-221">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="be10a-222">При наличии значение свойства `basis_set` должно быть объектом с двумя свойствами: `type` и `name`.</span><span class="sxs-lookup"><span data-stu-id="be10a-222">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="be10a-223">Основные функции, определяемые значением свойства `basis_set`, должны быть реальными.</span><span class="sxs-lookup"><span data-stu-id="be10a-223">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="be10a-224">Предположение, что все основные функции являются реальными, могут быть неослабленными в будущих версиях этой спецификации.</span><span class="sxs-lookup"><span data-stu-id="be10a-224">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="be10a-225">Таблицы и списки</span><span class="sxs-lookup"><span data-stu-id="be10a-225">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="be10a-226">Таблица 1.</span><span class="sxs-lookup"><span data-stu-id="be10a-226">Table 1.</span></span> <span data-ttu-id="be10a-227">Разрешенные физические устройства</span><span class="sxs-lookup"><span data-stu-id="be10a-227">Allowed Physical Units</span></span> ###

<span data-ttu-id="be10a-228">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-228">This section is normative.</span></span>

<span data-ttu-id="be10a-229">Любая строка, задающая единицу, должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="be10a-229">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="be10a-230">Средства синтаксического анализа и производители должны рассматривать следующие простые объекты Quantity как эквивалентные:</span><span class="sxs-lookup"><span data-stu-id="be10a-230">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="be10a-231">Таблица 2.</span><span class="sxs-lookup"><span data-stu-id="be10a-231">Table 2.</span></span> <span data-ttu-id="be10a-232">Допустимые соглашения об индексах</span><span class="sxs-lookup"><span data-stu-id="be10a-232">Allowed Index Conventions</span></span> ###

<span data-ttu-id="be10a-233">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-233">This section is normative.</span></span>

<span data-ttu-id="be10a-234">Любая строка, задающая соглашение об индексах, должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="be10a-234">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="be10a-235">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-235">This section is informative.</span></span>

<span data-ttu-id="be10a-236">В будущих версиях этой спецификации могут быть введены дополнительные соглашения об индексах.</span><span class="sxs-lookup"><span data-stu-id="be10a-236">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="be10a-237">Интерпретация соглашений об индексах</span><span class="sxs-lookup"><span data-stu-id="be10a-237">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="be10a-238">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-238">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="be10a-239">Таблица 3.</span><span class="sxs-lookup"><span data-stu-id="be10a-239">Table 3.</span></span> <span data-ttu-id="be10a-240">Методы разрешенного состояния</span><span class="sxs-lookup"><span data-stu-id="be10a-240">Allowed State methods</span></span> ###

<span data-ttu-id="be10a-241">Этот раздел является нормативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-241">This section is normative.</span></span>

<span data-ttu-id="be10a-242">Любая строка, задающая метод State, должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="be10a-242">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="be10a-243">Этот раздел является информативным.</span><span class="sxs-lookup"><span data-stu-id="be10a-243">This section is informative.</span></span>

<span data-ttu-id="be10a-244">Дополнительные методы состояния могут быть представлены в будущих версиях этой спецификации.</span><span class="sxs-lookup"><span data-stu-id="be10a-244">Additional state methods may be introduced in future versions of this specification.</span></span>
