---
title: Overload degli operatori (F#)
description: 'Informazioni su come eseguire l''overload di operatori aritmetici in una classe o un tipo di record e a livello globale in F #.'
keywords: visual f#, f#, programmazione funzionale
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 019277ed-f649-4fa5-ad43-097865f449d9
ms.openlocfilehash: 76ddab5339e11d71bb326b60d727017eb838ccf4
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="operator-overloading"></a><span data-ttu-id="0b39d-104">Overload degli operatori</span><span class="sxs-lookup"><span data-stu-id="0b39d-104">Operator Overloading</span></span>

<span data-ttu-id="0b39d-105">In questo argomento viene descritto come eseguire l'overload di operatori aritmetici in una classe o un tipo di record e a livello globale.</span><span class="sxs-lookup"><span data-stu-id="0b39d-105">This topic describes how to overload arithmetic operators in a class or record type, and at the global level.</span></span>


## <a name="syntax"></a><span data-ttu-id="0b39d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b39d-106">Syntax</span></span>

```fsharp
// Overloading an operator as a class or record member.
static member (operator-symbols) (parameter-list) =
    method-body
// Overloading an operator at the global level
let [inline] (operator-symbols) parameter-list = function-body
```

## <a name="remarks"></a><span data-ttu-id="0b39d-107">Note</span><span class="sxs-lookup"><span data-stu-id="0b39d-107">Remarks</span></span>
<span data-ttu-id="0b39d-108">Nella sintassi precedente, il *simbolo di operatore* è uno dei `+`, `-`, `*`, `/`, `=`e così via.</span><span class="sxs-lookup"><span data-stu-id="0b39d-108">In the previous syntax, the *operator-symbol* is one of `+`, `-`, `*`, `/`, `=`, and so on.</span></span> <span data-ttu-id="0b39d-109">Il *elenco di parametri* specifica gli operandi in ordine appaiono nella sintassi consueto per tale operatore.</span><span class="sxs-lookup"><span data-stu-id="0b39d-109">The *parameter-list* specifies the operands in the order they appear in the usual syntax for that operator.</span></span> <span data-ttu-id="0b39d-110">Il *-corpo del metodo* costruisce il valore risultante.</span><span class="sxs-lookup"><span data-stu-id="0b39d-110">The *method-body* constructs the resulting value.</span></span>

<span data-ttu-id="0b39d-111">Overload degli operatori per gli operatori devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="0b39d-111">Operator overloads for operators must be static.</span></span> <span data-ttu-id="0b39d-112">Operatore di overload per gli operatori unari, ad esempio `+` e `-`, devono includere una tilde (`~`) nel *simbolo di operatore* per indicare che l'operatore unario e non è un operatore binario, come illustrato di dichiarazione seguente.</span><span class="sxs-lookup"><span data-stu-id="0b39d-112">Operator overloads for unary operators, such as `+` and `-`, must use a tilde (`~`) in the *operator-symbol* to indicate that the operator is a unary operator and not a binary operator, as shown in the following declaration.</span></span>

```fsharp
static member (~-) (v : Vector)
```

<span data-ttu-id="0b39d-113">Nel codice seguente viene illustrata una classe di vettori con solo due operatori, uno per meno unario e uno per la moltiplicazione per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="0b39d-113">The following code illustrates a vector class that has just two operators, one for unary minus and one for multiplication by a scalar.</span></span> <span data-ttu-id="0b39d-114">Nell'esempio, due overload per la moltiplicazione scalare sono necessarie perché l'operatore deve essere utilizzato indipendentemente dall'ordine in cui vengono visualizzati il vettore e un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="0b39d-114">In the example, two overloads for scalar multiplication are needed because the operator must work regardless of the order in which the vector and scalar appear.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4001.fs)]

## <a name="creating-new-operators"></a><span data-ttu-id="0b39d-115">Creazione di nuovi operatori</span><span class="sxs-lookup"><span data-stu-id="0b39d-115">Creating New Operators</span></span>
<span data-ttu-id="0b39d-116">È possibile eseguire l'overload di tutti gli operatori standard, ma è anche possibile creare nuovi operatori da sequenze di caratteri specifici.</span><span class="sxs-lookup"><span data-stu-id="0b39d-116">You can overload all the standard operators, but you can also create new operators out of sequences of certain characters.</span></span> <span data-ttu-id="0b39d-117">Caratteri consentiti sono `!`, `%`, `&`, `*`, `+`, `-`, `.`, `/`, `<`, `=`, `>`, `?`, `@`, `^`, `|`, e `~`.</span><span class="sxs-lookup"><span data-stu-id="0b39d-117">Allowed operator characters are `!`, `%`, `&`, `*`, `+`, `-`, `.`, `/`, `<`, `=`, `>`, `?`, `@`, `^`, `|`, and `~`.</span></span> <span data-ttu-id="0b39d-118">Il `~` carattere ha un significato speciale di rendere unario un operatore e non fa parte della sequenza di caratteri dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="0b39d-118">The `~` character has the special meaning of making an operator unary, and is not part of the operator character sequence.</span></span> <span data-ttu-id="0b39d-119">Non tutti gli operatori possono essere resi unari.</span><span class="sxs-lookup"><span data-stu-id="0b39d-119">Not all operators can be made unary.</span></span>

<span data-ttu-id="0b39d-120">A seconda di utilizzare la sequenza di caratteri esatta, l'operatore avrà un determinato la precedenza e associatività.</span><span class="sxs-lookup"><span data-stu-id="0b39d-120">Depending on the exact character sequence you use, your operator will have a certain precedence and associativity.</span></span> <span data-ttu-id="0b39d-121">Associazione possa essere da sinistra verso destra o da destra a sinistra e viene utilizzato ogni volta che operatori dello stesso livello di precedenza vengono visualizzati in sequenza senza parentesi.</span><span class="sxs-lookup"><span data-stu-id="0b39d-121">Associativity can be either left to right or right to left and is used whenever operators of the same level of precedence appear in sequence without parentheses.</span></span>

<span data-ttu-id="0b39d-122">Il carattere dell'operatore `.` non influisce sulla precedenza, in modo che, ad esempio, se si desidera definire la propria versione di moltiplicazione che ha la stessa precedenza e associatività come moltiplicazione ordinaria, è possibile creare operatori quali `.*`.</span><span class="sxs-lookup"><span data-stu-id="0b39d-122">The operator character `.` does not affect precedence, so that, for example, if you want to define your own version of multiplication that has the same precedence and associativity as ordinary multiplication, you could create operators such as `.*`.</span></span>

<span data-ttu-id="0b39d-123">Solo gli operatori `?` e `?<-` può iniziare con `?`.</span><span class="sxs-lookup"><span data-stu-id="0b39d-123">Only the operators `?` and `?<-` may start with `?`.</span></span>

<span data-ttu-id="0b39d-124">Una tabella che mostra la precedenza di tutti gli operatori in F # è reperibile [riferimenti per simboli e operatore](symbol-and-operator-reference/index.md).</span><span class="sxs-lookup"><span data-stu-id="0b39d-124">A table that shows the precedence of all operators in F# can be found in [Symbol and Operator Reference](symbol-and-operator-reference/index.md).</span></span>


## <a name="overloaded-operator-names"></a><span data-ttu-id="0b39d-125">Nomi degli operatori di overload</span><span class="sxs-lookup"><span data-stu-id="0b39d-125">Overloaded Operator Names</span></span>
<span data-ttu-id="0b39d-126">Quando il compilatore F # compila un'espressione di operatore, viene generato un metodo che presenta un nome generato dal compilatore per questo operatore.</span><span class="sxs-lookup"><span data-stu-id="0b39d-126">When the F# compiler compiles an operator expression, it generates a method that has a compiler-generated name for that operator.</span></span> <span data-ttu-id="0b39d-127">Questo è il nome visualizzato in Microsoft intermedio language (MSIL) per il metodo e nella reflection e IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="0b39d-127">This is the name that appears in the Microsoft intermediate language (MSIL) for the method, and also in reflection and IntelliSense.</span></span> <span data-ttu-id="0b39d-128">In genere, non è necessario utilizzare questi nomi nel codice F #.</span><span class="sxs-lookup"><span data-stu-id="0b39d-128">You do not normally need to use these names in F# code.</span></span>

<span data-ttu-id="0b39d-129">Nella tabella seguente illustra gli operatori standard e i relativi nomi generati.</span><span class="sxs-lookup"><span data-stu-id="0b39d-129">The following table shows the standard operators and their corresponding generated names.</span></span>



|<span data-ttu-id="0b39d-130">Operatore</span><span class="sxs-lookup"><span data-stu-id="0b39d-130">Operator</span></span>|<span data-ttu-id="0b39d-131">Nome generato</span><span class="sxs-lookup"><span data-stu-id="0b39d-131">Generated name</span></span>|
|--------|--------------|
|`[]`|`op_Nil`|
|`::`|`op_Cons`|
|`+`|`op_Addition`|
|`-`|`op_Subtraction`|
|`*`|`op_Multiply`|
|`/`|`op_Division`|
|`@`|`op_Append`|
|`^`|`op_Concatenate`|
|`%`|`op_Modulus`|
|`&&&`|`op_BitwiseAnd`|
|<code>&#124;&#124;&#124;</code>|`op_BitwiseOr`|
|`^^^`|`op_ExclusiveOr`|
|`<<<`|`op_LeftShift`|
|`~~~`|`op_LogicalNot`|
|`>>>`|`op_RightShift`|
|`~+`|`op_UnaryPlus`|
|`~-`|`op_UnaryNegation`|
|`=`|`op_Equality`|
|`<=`|`op_LessThanOrEqual`|
|`>=`|`op_GreaterThanOrEqual`|
|`<`|`op_LessThan`|
|`>`|`op_GreaterThan`|
|`?`|`op_Dynamic`|
|`?<-`|`op_DynamicAssignment`|
|<code>&#124;></code>|`op_PipeRight`|
|<code><&#124;</code>|`op_PipeLeft`|
|`!`|`op_Dereference`|
|`>>`|`op_ComposeRight`|
|`<<`|`op_ComposeLeft`|
|`<@ @>`|`op_Quotation`|
|`<@@ @@>`|`op_QuotationUntyped`|
|`+=`|`op_AdditionAssignment`|
|`-=`|`op_SubtractionAssignment`|
|`*=`|`op_MultiplyAssignment`|
|`/=`|`op_DivisionAssignment`|
|`..`|`op_Range`|
|`.. ..`|`op_RangeStep`|
<span data-ttu-id="0b39d-132">Altre combinazioni di caratteri dell'operatore che non sono elencati di seguito possono essere usati come operatori e hanno nomi composti da concatenando i nomi per i singoli caratteri della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0b39d-132">Other combinations of operator characters that are not listed here can be used as operators and have names that are made up by concatenating names for the individual characters from the following table.</span></span> <span data-ttu-id="0b39d-133">Ad esempio, +!</span><span class="sxs-lookup"><span data-stu-id="0b39d-133">For example, +!</span></span> <span data-ttu-id="0b39d-134">diventa `op_PlusBang`.</span><span class="sxs-lookup"><span data-stu-id="0b39d-134">becomes `op_PlusBang`.</span></span>



|<span data-ttu-id="0b39d-135">Carattere dell'operatore</span><span class="sxs-lookup"><span data-stu-id="0b39d-135">Operator character</span></span>|<span data-ttu-id="0b39d-136">Nome</span><span class="sxs-lookup"><span data-stu-id="0b39d-136">Name</span></span>|
|------------------|----|
|`>`|`Greater`|
|`<`|`Less`|
|`+`|`Plus`|
|`-`|`Minus`|
|`*`|`Multiply`|
|`/`|`Divide`|
|`=`|`Equals`|
|`~`|`Twiddle`|
|`%`|`Percent`|
|`.`|`Dot`|
|`&`|`Amp`|
|<code>&#124;</code>|`Bar`|
|`@`|`At`|
|`^`|`Hat`|
|`!`|`Bang`|
|`?`|`Qmark`|
|`(`|`LParen`|
|`,`|`Comma`|
|`)`|`RParen`|
|`[`|`LBrack`|
|`]`|`RBrack`|

## <a name="prefix-and-infix-operators"></a><span data-ttu-id="0b39d-137">Prefisso e gli operatori infissi</span><span class="sxs-lookup"><span data-stu-id="0b39d-137">Prefix and Infix Operators</span></span>
<span data-ttu-id="0b39d-138">*Prefisso* gli operatori devono essere inseriti davanti a uno o più operandi, analogamente a una funzione.</span><span class="sxs-lookup"><span data-stu-id="0b39d-138">*Prefix* operators are expected to be placed in front of an operand or operands, much like a function.</span></span> <span data-ttu-id="0b39d-139">*Infisso* gli operatori devono essere racchiuse tra i due operandi.</span><span class="sxs-lookup"><span data-stu-id="0b39d-139">*Infix* operators are expected to be placed between the two operands.</span></span>

<span data-ttu-id="0b39d-140">Solo determinati operatori possono essere utilizzati come gli operatori prefisso.</span><span class="sxs-lookup"><span data-stu-id="0b39d-140">Only certain operators can be used as prefix operators.</span></span> <span data-ttu-id="0b39d-141">Alcuni operatori sono sempre gli operatori prefisso, altri possono essere infisso o prefisso e il resto è sempre operatori infisso.</span><span class="sxs-lookup"><span data-stu-id="0b39d-141">Some operators are always prefix operators, others can be infix or prefix, and the rest are always infix operators.</span></span> <span data-ttu-id="0b39d-142">Gli operatori che iniziano con `!`, ad eccezione di `!=`e l'operatore `~`, o ripetuti sequenze di`~`, sono sempre gli operatori prefisso.</span><span class="sxs-lookup"><span data-stu-id="0b39d-142">Operators that begin with `!`, except `!=`, and the operator `~`, or repeated sequences of`~`, are always prefix operators.</span></span> <span data-ttu-id="0b39d-143">Gli operatori `+`, `-`, `+.`, `-.`, `&`, `&&`, `%`, e `%%` può essere operatori prefisso o operatori infissi.</span><span class="sxs-lookup"><span data-stu-id="0b39d-143">The operators `+`, `-`, `+.`, `-.`, `&`, `&&`, `%`, and `%%` can be prefix operators or infix operators.</span></span> <span data-ttu-id="0b39d-144">La versione di prefisso di questi operatori è distinguere dalla versione di infisso aggiungendo un `~` all'inizio di un operatore prefisso quando è definito.</span><span class="sxs-lookup"><span data-stu-id="0b39d-144">You distinguish the prefix version of these operators from the infix version by adding a `~` at the beginning of a prefix operator when it is defined.</span></span> <span data-ttu-id="0b39d-145">Il `~` non viene utilizzato quando si utilizza l'operatore, solo quando è definito.</span><span class="sxs-lookup"><span data-stu-id="0b39d-145">The `~` is not used when you use the operator, only when it is defined.</span></span>

## <a name="example"></a><span data-ttu-id="0b39d-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b39d-146">Example</span></span>

<span data-ttu-id="0b39d-147">Il codice seguente viene illustrato l'utilizzo dell'operatore di overload per implementare una frazione di tipo.</span><span class="sxs-lookup"><span data-stu-id="0b39d-147">The following code illustrates the use of operator overloading to implement a fraction type.</span></span> <span data-ttu-id="0b39d-148">Una frazione è rappresentata da un numeratore e un denominatore.</span><span class="sxs-lookup"><span data-stu-id="0b39d-148">A fraction is represented by a numerator and a denominator.</span></span> <span data-ttu-id="0b39d-149">La funzione `hcf` viene utilizzato per determinare il fattore comune più elevato, viene utilizzato per ridurre le frazioni di secondo.</span><span class="sxs-lookup"><span data-stu-id="0b39d-149">The function `hcf` is used to determine the highest common factor, which is used to reduce fractions.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4002.fs)]

<span data-ttu-id="0b39d-150">**Output:**</span><span class="sxs-lookup"><span data-stu-id="0b39d-150">**Output:**</span></span>

```
3/4 + 1/2 = 5/4
3/4 - 1/2 = 1/4
3/4 * 1/2 = 3/8
3/4 / 1/2 = 3/2
3/4 + 1 = 7/4
```

## <a name="operators-at-the-global-level"></a><span data-ttu-id="0b39d-151">Operatori a livello globale</span><span class="sxs-lookup"><span data-stu-id="0b39d-151">Operators at the Global Level</span></span>
<span data-ttu-id="0b39d-152">È inoltre possibile definire operatori a livello globale.</span><span class="sxs-lookup"><span data-stu-id="0b39d-152">You can also define operators at the global level.</span></span> <span data-ttu-id="0b39d-153">Il codice seguente definisce un operatore `+?`.</span><span class="sxs-lookup"><span data-stu-id="0b39d-153">The following code defines an operator `+?`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4003.fs)]

<span data-ttu-id="0b39d-154">L'output del codice sopra riportato è `12`.</span><span class="sxs-lookup"><span data-stu-id="0b39d-154">The output of the above code is `12`.</span></span>

<span data-ttu-id="0b39d-155">È possibile ridefinire gli operatori aritmetici regolari in questo modo perché le regole di ambito per F # prevedono che gli operatori appena definiti hanno la precedenza sugli operatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="0b39d-155">You can redefine the regular arithmetic operators in this manner because the scoping rules for F# dictate that newly defined operators take precedence over the built-in operators.</span></span>

<span data-ttu-id="0b39d-156">La parola chiave `inline` viene spesso usato con gli operatori globali, che spesso sono piccole funzioni che si integrano meglio nel codice chiamante.</span><span class="sxs-lookup"><span data-stu-id="0b39d-156">The keyword `inline` is often used with global operators, which are often small functions that are best integrated into the calling code.</span></span> <span data-ttu-id="0b39d-157">Apportato operatore funzioni inline consente di utilizzare i parametri di tipo risolti staticamente per produrre codice generico risolto in modo statico.</span><span class="sxs-lookup"><span data-stu-id="0b39d-157">Making operator functions inline also enables them to work with statically resolved type parameters to produce statically resolved generic code.</span></span> <span data-ttu-id="0b39d-158">Per ulteriori informazioni, vedere [funzioni Inline](functions/inline-functions.md) e [parametri tipo risolti staticamente](generics/statically-resolved-type-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0b39d-158">For more information, see [Inline Functions](functions/inline-functions.md) and [Statically Resolved Type Parameters](generics/statically-resolved-type-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b39d-159">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0b39d-159">See Also</span></span>
[<span data-ttu-id="0b39d-160">Membri</span><span class="sxs-lookup"><span data-stu-id="0b39d-160">Members</span></span>](members/index.md)