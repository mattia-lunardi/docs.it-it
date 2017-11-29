---
title: Celle di riferimento (F#)
description: 'Informazioni su come le celle di riferimento di F # sono percorsi di archiviazione che consentono di creare valori modificabili con semantica di riferimento.'
keywords: visual f#, f#, programmazione funzionale
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 09a0b221-ea21-45c4-bae8-5e4a339750c4
ms.openlocfilehash: c7470c9a36cf2cd24dd89ceffcf6e90c6dc4d2dd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="reference-cells"></a><span data-ttu-id="2c0b0-104">Celle di riferimento</span><span class="sxs-lookup"><span data-stu-id="2c0b0-104">Reference Cells</span></span>

<span data-ttu-id="2c0b0-105">*Fare riferimento alle celle* sono percorsi di archiviazione che consentono di creare valori modificabili con semantica di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-105">*Reference cells* are storage locations that enable you to create mutable values with reference semantics.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0b0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c0b0-106">Syntax</span></span>

```fsharp
ref expression
```

## <a name="remarks"></a><span data-ttu-id="2c0b0-107">Note</span><span class="sxs-lookup"><span data-stu-id="2c0b0-107">Remarks</span></span>
<span data-ttu-id="2c0b0-108">L'operatore `ref` viene utilizzato prima di un valore per creare una nuova cella di riferimento che incapsuli il valore.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-108">You use the `ref` operator before a value to create a new reference cell that encapsulates the value.</span></span> <span data-ttu-id="2c0b0-109">È quindi possibile modificare il valore sottostante, in quanto è modificabile.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-109">You can then change the underlying value because it is mutable.</span></span>

<span data-ttu-id="2c0b0-110">Una cella di riferimento contiene un valore effettivo e non solo un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-110">A reference cell holds an actual value; it is not just an address.</span></span> <span data-ttu-id="2c0b0-111">Quando si crea una cella di riferimento utilizzando l'operatore `ref`, si crea una copia del valore sottostante come valore modificabile incapsulato.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-111">When you create a reference cell by using the `ref` operator, you create a copy of the underlying value as an encapsulated mutable value.</span></span>

<span data-ttu-id="2c0b0-112">È possibile dereferenziare una cella di riferimento utilizzando l'operatore `!` (punto esclamativo).</span><span class="sxs-lookup"><span data-stu-id="2c0b0-112">You can dereference a reference cell by using the `!` (bang) operator.</span></span>

<span data-ttu-id="2c0b0-113">Nell'esempio di codice seguente vengono illustrati la dichiarazione e l'utilizzo di celle di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-113">The following code example illustrates the declaration and use of reference cells.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2201.fs)]

<span data-ttu-id="2c0b0-114">L'output è `50`.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-114">The output is `50`.</span></span>

<span data-ttu-id="2c0b0-115">Le celle di riferimento sono istanze del tipo di record generico `Ref`, dichiarato come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-115">Reference cells are instances of the `Ref` generic record type, which is declared as follows.</span></span>

```fsharp
type Ref<'a> =
{ mutable contents: 'a }
```

<span data-ttu-id="2c0b0-116">Il tipo `'a ref` è sinonimo di `Ref<'a>`.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-116">The type `'a ref` is a synonym for `Ref<'a>`.</span></span> <span data-ttu-id="2c0b0-117">Il primo viene visualizzato dal compilatore e da IntelliSense nell'interfaccia IDE per questo tipo, mentre il secondo rappresenta la definizione sottostante.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-117">The compiler and IntelliSense in the IDE display the former for this type, but the underlying definition is the latter.</span></span>

<span data-ttu-id="2c0b0-118">L'operatore `ref` consente di creare una nuova cella di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-118">The `ref` operator creates a new reference cell.</span></span> <span data-ttu-id="2c0b0-119">Il codice seguente rappresenta la dichiarazione dell'operatore `ref`.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-119">The following code is the declaration of the `ref` operator.</span></span>

```fsharp
let ref x = { contents = x }
```

<span data-ttu-id="2c0b0-120">Nella tabella seguente sono indicate le funzionalità disponibili nella cella di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-120">The following table shows the features that are available on the reference cell.</span></span>

|<span data-ttu-id="2c0b0-121">Operatore, membro o campo</span><span class="sxs-lookup"><span data-stu-id="2c0b0-121">Operator, member, or field</span></span>|<span data-ttu-id="2c0b0-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c0b0-122">Description</span></span>|<span data-ttu-id="2c0b0-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c0b0-123">Type</span></span>|<span data-ttu-id="2c0b0-124">Definizione</span><span class="sxs-lookup"><span data-stu-id="2c0b0-124">Definition</span></span>|
|--------------------------|-----------|----|----------|
|<span data-ttu-id="2c0b0-125">`!` (operatore di dereferenziazione)</span><span class="sxs-lookup"><span data-stu-id="2c0b0-125">`!` (dereference operator)</span></span>|<span data-ttu-id="2c0b0-126">Restituisce il valore sottostante.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-126">Returns the underlying value.</span></span>|`'a ref -> 'a`|`let (!) r = r.contents`|
|<span data-ttu-id="2c0b0-127">`:=` (operatore di assegnazione)</span><span class="sxs-lookup"><span data-stu-id="2c0b0-127">`:=` (assignment operator)</span></span>|<span data-ttu-id="2c0b0-128">Modifica il valore sottostante.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-128">Changes the underlying value.</span></span>|`'a ref -> 'a -> unit`|`let (:=) r x = r.contents <- x`|
|<span data-ttu-id="2c0b0-129">`ref` (operatore)</span><span class="sxs-lookup"><span data-stu-id="2c0b0-129">`ref` (operator)</span></span>|<span data-ttu-id="2c0b0-130">Incapsula un valore in una nuova cella di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-130">Encapsulates a value into a new reference cell.</span></span>|`'a -> 'a ref`|`let ref x = { contents = x }`|
|<span data-ttu-id="2c0b0-131">`Value` (proprietà)</span><span class="sxs-lookup"><span data-stu-id="2c0b0-131">`Value` (property)</span></span>|<span data-ttu-id="2c0b0-132">Ottiene o imposta il valore sottostante.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-132">Gets or sets the underlying value.</span></span>|`unit -> 'a`|`member x.Value = x.contents`|
|<span data-ttu-id="2c0b0-133">`contents` (campo del record)</span><span class="sxs-lookup"><span data-stu-id="2c0b0-133">`contents` (record field)</span></span>|<span data-ttu-id="2c0b0-134">Ottiene o imposta il valore sottostante.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-134">Gets or sets the underlying value.</span></span>|`'a`|`let ref x = { contents = x }`|
<span data-ttu-id="2c0b0-135">È possibile accedere al valore sottostante in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-135">There are several ways to access the underlying value.</span></span> <span data-ttu-id="2c0b0-136">Il valore restituito dall'operatore di dereferenziazione (`!`) non è un valore assegnabile.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-136">The value returned by the dereference operator (`!`) is not an assignable value.</span></span> <span data-ttu-id="2c0b0-137">Se pertanto si modifica il valore sottostante, è necessario utilizzare l'operatore di assegnazione (`:=`).</span><span class="sxs-lookup"><span data-stu-id="2c0b0-137">Therefore, if you are modifying the underlying value, you must use the assignment operator (`:=`) instead.</span></span>

<span data-ttu-id="2c0b0-138">Sia la proprietà `Value` che il campo `contents` sono valori assegnabili</span><span class="sxs-lookup"><span data-stu-id="2c0b0-138">Both the `Value` property and the `contents` field are assignable values.</span></span> <span data-ttu-id="2c0b0-139">e possono pertanto essere utilizzati per accedere al valore sottostante o per modificare tale valore, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-139">Therefore, you can use these to either access or change the underlying value, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2203.fs)]

<span data-ttu-id="2c0b0-140">L'output è indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-140">The output is as follows.</span></span>

```
10
10
11
12
```

<span data-ttu-id="2c0b0-141">Il campo `contents` viene fornito per garantire compatibilità con altre versioni di ML e comporta la generazione di un avviso durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-141">The field `contents` is provided for compatibility with other versions of ML and will produce a warning during compilation.</span></span> <span data-ttu-id="2c0b0-142">Per disabilitare l'avviso, utilizzare l'opzione del compilatore `--mlcompatibility`.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-142">To disable the warning, use the `--mlcompatibility` compiler option.</span></span> <span data-ttu-id="2c0b0-143">Per altre informazioni, vedere [Opzioni del compilatore](compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="2c0b0-143">For more information, see [Compiler Options](compiler-options.md).</span></span>

<span data-ttu-id="2c0b0-144">Nell'esempio di codice seguente viene illustrato l'utilizzo di celle di riferimento nel passaggio dei parametri.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-144">The following code illustrates the use of reference cells in parameter passing.</span></span> <span data-ttu-id="2c0b0-145">Il tipo di Incrementatore ha un metodo Increment che accetta un parametro che include il tipo di parametro byref.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-145">The Incrementor type has a method Increment that takes a parameter that includes byref in the parameter type.</span></span> <span data-ttu-id="2c0b0-146">Byref nel tipo di parametro indica che i chiamanti devono passare una cella di riferimento o l'indirizzo di una variabile tipica del tipo specificato, in questo caso int Il codice restante viene illustrato come chiamare Increment con entrambi i tipi di argomenti e viene illustrato come utilizzare l'operatore di riferimento in una variabile per creare una cella di riferimento (ref myDelta1).</span><span class="sxs-lookup"><span data-stu-id="2c0b0-146">The byref in the parameter type indicates that callers must pass a reference cell or the address of a typical variable of the specified type, in this case int. The remaining code illustrates how to call Increment with both of these types of arguments, and shows the use of the ref operator on a variable to create a reference cell (ref myDelta1).</span></span> <span data-ttu-id="2c0b0-147">Viene quindi illustrato l'utilizzo dell'operatore address-of (&amp;) per generare un argomento appropriato.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-147">It then shows the use of the address-of operator (&amp;) to generate an appropriate argument.</span></span> <span data-ttu-id="2c0b0-148">Infine, l'incremento viene chiamato nuovamente utilizzando una cella di riferimento viene dichiarata utilizzando un binding let.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-148">Finally, the Increment method is called again by using a reference cell that is declared by using a let binding.</span></span> <span data-ttu-id="2c0b0-149">L'ultima riga del codice viene illustrato come utilizzare il!</span><span class="sxs-lookup"><span data-stu-id="2c0b0-149">The final line of code demonstrates the use of the !</span></span> <span data-ttu-id="2c0b0-150">operatore per dereferenziare la cella di riferimento per la stampa.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-150">operator to dereference the reference cell for printing.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2204.fs)]

<span data-ttu-id="2c0b0-151">Per ulteriori informazioni su come passare per riferimento, vedere [parametri e argomenti](parameters-and-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="2c0b0-151">For more information about how to pass by reference, see [Parameters and Arguments](parameters-and-arguments.md).</span></span>

>[!NOTE]
<span data-ttu-id="2c0b0-152">I programmatori c# devono sapere che ref funziona in modo diverso in F # rispetto a quello usato in c#.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-152">C# programmers should know that ref works differently in F# than it does in C#.</span></span> <span data-ttu-id="2c0b0-153">Ad esempio, l'utilizzo di riferimento quando si passa un argomento non hanno lo stesso effetto in F # a quanto accade in c#.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-153">For example, the use of ref when you pass an argument does not have the same effect in F# as it does in C#.</span></span>

## <a name="consuming-c-ref-returns"></a><span data-ttu-id="2c0b0-154">Utilizzo in c# `ref` restituisce</span><span class="sxs-lookup"><span data-stu-id="2c0b0-154">Consuming C# `ref` returns</span></span>

<span data-ttu-id="2c0b0-155">A partire da F # 4.1, è possibile utilizzare `ref` restituisce generato in c#.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-155">Starting with F# 4.1, you can consume `ref` returns generated in C#.</span></span>  <span data-ttu-id="2c0b0-156">Il risultato della chiamata di questo tipo è un `byref<_>` puntatore.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-156">The result of such a call is a `byref<_>` pointer.</span></span>

<span data-ttu-id="2c0b0-157">Il seguente metodo c#:</span><span class="sxs-lookup"><span data-stu-id="2c0b0-157">The following C# method:</span></span>

```csharp
namespace RefReturns
{
    public static class RefClass
    {
        public static ref int Find(int val, int[] vals)
        {
            for (int i = 0; i < vals.Length; i++)
            {
                if (vals[i] == val)
                {
                    return ref numbers[i]; // Returns the location, not the value
                }
            }

            throw new IndexOutOfRangeException($"{nameof(number)} not found");
        }
    }
}
```

<span data-ttu-id="2c0b0-158">Può essere trasparente chiamato da F # con alcuna sintassi particolare:</span><span class="sxs-lookup"><span data-stu-id="2c0b0-158">Can be transparently called by F# with no special syntax:</span></span>

```fsharp
open RefReturns

let consumeRefReturn() =
    let result = RefClass.Find(3, [| 1; 2; 3; 4; 5 |]) // 'result' is of type 'byref<int>'.
    ()
```

<span data-ttu-id="2c0b0-159">È inoltre possibile dichiarare funzioni che richiedono un `ref` restituire come input, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2c0b0-159">You can also declare functions which could take a `ref` return as input, for example:</span></span>

```fsharp
let f (x: byref<int>) = &x
```

<span data-ttu-id="2c0b0-160">Non è attualmente possibile generare un `ref` restituito in F # che poteva essere usata in c#.</span><span class="sxs-lookup"><span data-stu-id="2c0b0-160">There is currently no way to generate a `ref` return in F# which could be consumed in C#.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c0b0-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2c0b0-161">See Also</span></span>
[<span data-ttu-id="2c0b0-162">Riferimenti per il linguaggio F#</span><span class="sxs-lookup"><span data-stu-id="2c0b0-162">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="2c0b0-163">Parametri e argomenti</span><span class="sxs-lookup"><span data-stu-id="2c0b0-163">Parameters and Arguments</span></span>](parameters-and-arguments.md)

[<span data-ttu-id="2c0b0-164">Riferimenti per simboli e operatori</span><span class="sxs-lookup"><span data-stu-id="2c0b0-164">Symbol and Operator Reference</span></span>](symbol-and-operator-reference/index.md)