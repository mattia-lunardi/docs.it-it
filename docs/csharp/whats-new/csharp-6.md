---
title: "Novità di c# 6 - Guida per c#"
description: "Informazioni sulle nuove funzionalità di C# versione 6"
keywords: .NET, .NET Core
author: BillWagner
ms.date: 09/22/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: 4d879f69-f889-4d3f-a781-75194e143400
ms.openlocfilehash: f3e7a515b1dde52461ab6abf8a9adbe84d27b7c1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="whats-new-in-c-6"></a><span data-ttu-id="727fc-104">Novità di C# 6</span><span class="sxs-lookup"><span data-stu-id="727fc-104">What's New in C# 6</span></span>

<span data-ttu-id="727fc-105">La versione 6.0 di C# contiene molte funzionalità che consentono agli sviluppatori di migliorare la produttività.</span><span class="sxs-lookup"><span data-stu-id="727fc-105">The 6.0 release of C# contained many features that improve productivity for developers.</span></span> <span data-ttu-id="727fc-106">Di seguito sono riportate alcune funzionalità incluse in questa versione:</span><span class="sxs-lookup"><span data-stu-id="727fc-106">Features in this release include:</span></span>

* <span data-ttu-id="727fc-107">[Proprietà automatiche di sola lettura](#read-only-auto-properties):</span><span class="sxs-lookup"><span data-stu-id="727fc-107">[Read-only Auto-properties](#read-only-auto-properties):</span></span>
    - <span data-ttu-id="727fc-108">È possibile creare proprietà automatiche di sola che possono essere impostate solo nei costruttori.</span><span class="sxs-lookup"><span data-stu-id="727fc-108">You can create read-only auto-properties that can be set only in constructors.</span></span>
* <span data-ttu-id="727fc-109">[Inizializzatori di proprietà automatiche](#auto-property-initializers):</span><span class="sxs-lookup"><span data-stu-id="727fc-109">[Auto-Property Initializers](#auto-property-initializers):</span></span>
    - <span data-ttu-id="727fc-110">È possibile scrivere espressioni di inizializzazione per impostare il valore iniziale di una proprietà automatica.</span><span class="sxs-lookup"><span data-stu-id="727fc-110">You can write initialization expressions to set the initial value of an auto-property.</span></span>
* <span data-ttu-id="727fc-111">[Membri di funzione con corpo di espressione](#expression-bodied-function-members):</span><span class="sxs-lookup"><span data-stu-id="727fc-111">[Expression-bodied function members](#expression-bodied-function-members):</span></span>
    - <span data-ttu-id="727fc-112">È possibile creare metodi di una riga usando le espressioni lambda.</span><span class="sxs-lookup"><span data-stu-id="727fc-112">You can author one-line methods using lambda expressions.</span></span>
* <span data-ttu-id="727fc-113">[using static](#using-static):</span><span class="sxs-lookup"><span data-stu-id="727fc-113">[using static](#using-static):</span></span>
    - <span data-ttu-id="727fc-114">È possibile importare tutti i metodi di una singola classe nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="727fc-114">You can import all the methods of a single class into the current namespace.</span></span>
* <span data-ttu-id="727fc-115">[Operatori condizionali Null](#null-conditional-operators):</span><span class="sxs-lookup"><span data-stu-id="727fc-115">[Null - conditional operators](#null-conditional-operators):</span></span>
    - <span data-ttu-id="727fc-116">È possibile accedere ai membri di un oggetto in modo conciso e sicuro durante la ricerca di Null con l'operatore condizionale Null.</span><span class="sxs-lookup"><span data-stu-id="727fc-116">You can concisely and safely access members of an object while still checking for null with the null conditional operator.</span></span>
* <span data-ttu-id="727fc-117">[Interpolazione di stringhe](#string-interpolation):</span><span class="sxs-lookup"><span data-stu-id="727fc-117">[String Interpolation](#string-interpolation):</span></span>
    - <span data-ttu-id="727fc-118">È possibile scrivere espressioni di formattazione delle stringhe usando espressioni inline anziché argomenti posizionali.</span><span class="sxs-lookup"><span data-stu-id="727fc-118">You can write string formatting expressions using inline expressions instead of positional arguments.</span></span>
* <span data-ttu-id="727fc-119">[Filtri eccezioni](#exception-filters):</span><span class="sxs-lookup"><span data-stu-id="727fc-119">[Exception filters](#exception-filters):</span></span>
    - <span data-ttu-id="727fc-120">È possibile intercettare le espressioni in base alle proprietà dell'eccezione o di un altro stato del programma.</span><span class="sxs-lookup"><span data-stu-id="727fc-120">You can catch expressions based on properties of the exception or other program state.</span></span> 
* <span data-ttu-id="727fc-121">[Espressioni nameof](#nameof-expressions):</span><span class="sxs-lookup"><span data-stu-id="727fc-121">[nameof Expressions](#nameof-expressions):</span></span>
    - <span data-ttu-id="727fc-122">È possibile consentire al compilatore di generare rappresentazioni di stringa dei simboli.</span><span class="sxs-lookup"><span data-stu-id="727fc-122">You can let the compiler generate string representations of symbols.</span></span>
* <span data-ttu-id="727fc-123">[Await nei blocchi catch e finally](#await-in-catch-and-finally-blocks):</span><span class="sxs-lookup"><span data-stu-id="727fc-123">[await in catch and finally blocks](#await-in-catch-and-finally-blocks):</span></span>
    - <span data-ttu-id="727fc-124">È possibile usare le espressioni `await` in posizioni che in precedenza non le consentivano.</span><span class="sxs-lookup"><span data-stu-id="727fc-124">You can use `await` expressions in locations that previously disallowed them.</span></span>
* <span data-ttu-id="727fc-125">[Inizializzatori di indice](#index-initializers):</span><span class="sxs-lookup"><span data-stu-id="727fc-125">[index initializers](#index-initializers):</span></span>
    - <span data-ttu-id="727fc-126">È possibile creare espressioni di inizializzazione per i contenitori associativi, nonché per i contenitori sequenziali.</span><span class="sxs-lookup"><span data-stu-id="727fc-126">You can author initialization expressions for associative containers as well as sequence containers.</span></span>
* <span data-ttu-id="727fc-127">[Metodi di estensione per gli inizializzatori di insieme](#extension-add-methods-in-collection-initializers):</span><span class="sxs-lookup"><span data-stu-id="727fc-127">[Extension methods for collection initializers](#extension-add-methods-in-collection-initializers):</span></span>
    - <span data-ttu-id="727fc-128">Gli inizializzatori di insieme possono basarsi su metodi di estensione accessibili, oltre ai metodi membro.</span><span class="sxs-lookup"><span data-stu-id="727fc-128">Collection initializers can rely on accessible extension methods, in addition to member methods.</span></span>
* <span data-ttu-id="727fc-129">[Risoluzione dell'overload migliorata](#improved-overload-resolution):</span><span class="sxs-lookup"><span data-stu-id="727fc-129">[Improved overload resolution](#improved-overload-resolution):</span></span>
    - <span data-ttu-id="727fc-130">Alcuni costrutti che in precedenza generavano chiamate ambigue al metodo ora risolvono correttamente.</span><span class="sxs-lookup"><span data-stu-id="727fc-130">Some constructs that previously generated ambiguous method calls now resolve correctly.</span></span>

<span data-ttu-id="727fc-131">L'effetto generale di queste funzionalità è che il codice che si scrive è più conciso e anche più leggibile.</span><span class="sxs-lookup"><span data-stu-id="727fc-131">The overall effect of these features is that you write more concise code that is also more readable.</span></span> <span data-ttu-id="727fc-132">La sintassi è più semplice e lineare per molte delle procedure più comuni.</span><span class="sxs-lookup"><span data-stu-id="727fc-132">The syntax contains less ceremony for many common practices.</span></span> <span data-ttu-id="727fc-133">È più facile visualizzare le finalità di progettazione se la sintassi è più snella.</span><span class="sxs-lookup"><span data-stu-id="727fc-133">It's easier to see the design intent with less ceremony.</span></span> <span data-ttu-id="727fc-134">È importante acquisire dimestichezza con queste funzionalità per essere più produttivi, scrivere codice più leggibile e concentrarsi maggiormente sulle funzionalità principali e meno sui costrutti del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="727fc-134">Learn these features well, and you'll be more productive, write more readable code, and concentrate more on your core features than on the constructs of the language.</span></span>

<span data-ttu-id="727fc-135">Nelle altre sezioni di questo argomento sono disponibili informazioni dettagliate su ognuna di queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="727fc-135">The remainder of this topic provides details on each of these features.</span></span>

## <a name="auto-property-enhancements"></a><span data-ttu-id="727fc-136">Miglioramenti delle proprietà automatiche</span><span class="sxs-lookup"><span data-stu-id="727fc-136">Auto-Property enhancements</span></span> 

<span data-ttu-id="727fc-137">La sintassi per le proprietà implementate automaticamente, in genere definite "proprietà automatiche", ha semplificato notevolmente la creazione delle proprietà con semplici funzioni di accesso get e set:</span><span class="sxs-lookup"><span data-stu-id="727fc-137">The syntax for automatically implemented properties (usually referred to as 'auto-properties') made it very easy to create properties that had simple get and set accessors:</span></span>

[!code-csharp[ClassicAutoProperty](../../../samples/snippets/csharp/new-in-6/oldcode.cs#ClassicAutoProperty)]

<span data-ttu-id="727fc-138">Tuttavia, la sintassi semplice ha limitato i tipi di progetti che è possibile supportare usando le proprietà automatiche.</span><span class="sxs-lookup"><span data-stu-id="727fc-138">However, this simple syntax limited the kinds of designs you could support using auto-properties.</span></span> <span data-ttu-id="727fc-139">C# 6 migliora le funzionalità delle proprietà automatiche in modo che sia possibile usarle in più situazioni.</span><span class="sxs-lookup"><span data-stu-id="727fc-139">C# 6 improves the auto-properties capabilities so that you can use them in more scenarios.</span></span> <span data-ttu-id="727fc-140">Non è necessario ricorrere spesso alla sintassi più dettagliata per la dichiarazione e la modifica manuale del campo sottostante.</span><span class="sxs-lookup"><span data-stu-id="727fc-140">You won't need to fall back on the more verbose syntax of declaring and manipulating the backing field by hand so often.</span></span>

<span data-ttu-id="727fc-141">La nuova sintassi illustrati gli scenari per le proprietà di sola lettura e per l'inizializzazione di archiviazione della variabile dietro una proprietà automatica.</span><span class="sxs-lookup"><span data-stu-id="727fc-141">The new syntax addresses scenarios for read-only properties, and for initializing the variable storage behind an auto-property.</span></span>

### <a name="read-only-auto-properties"></a><span data-ttu-id="727fc-142">Proprietà automatiche di sola lettura</span><span class="sxs-lookup"><span data-stu-id="727fc-142">Read-only auto-properties</span></span>

<span data-ttu-id="727fc-143">Le *proprietà automatiche di sola lettura* offrono una sintassi più concisa per creare i tipi non modificabili.</span><span class="sxs-lookup"><span data-stu-id="727fc-143">*Read-only auto-properties* provide a more concise syntax to create immutable types.</span></span> <span data-ttu-id="727fc-144">Nelle versioni precedenti di C# il massimo che è possibile ottenere per i tipi non modificabili è dichiarare setter privati:</span><span class="sxs-lookup"><span data-stu-id="727fc-144">The closest you could get to immutable types in earlier versions of C# was to declare private setters:</span></span>

[!code-csharp[ClassicReadOnlyAutoProperty](../../../samples/snippets/csharp/new-in-6/oldcode.cs#ClassicReadOnlyAutoProperty)]
 
<span data-ttu-id="727fc-145">Con questa sintassi il compilatore non verifica che il tipo sia effettivamente non modificabile.</span><span class="sxs-lookup"><span data-stu-id="727fc-145">Using this syntax, the compiler doesn't ensure that the type really is immutable.</span></span> <span data-ttu-id="727fc-146">Si limita a imporre che le proprietà `FirstName` e `LastName` non vengano modificate da qualsiasi codice all'esterno della classe.</span><span class="sxs-lookup"><span data-stu-id="727fc-146">It only enforces that the `FirstName` and `LastName` properties are not modified from any code outside the class.</span></span>

<span data-ttu-id="727fc-147">Le proprietà automatiche di sola lettura abilitano un vero comportamento di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="727fc-147">Read-only auto-properties enable true read-only behavior.</span></span> <span data-ttu-id="727fc-148">Si dichiara la proprietà automatica solo con una funzione di accesso get:</span><span class="sxs-lookup"><span data-stu-id="727fc-148">You declare the auto-property with only a get accessor:</span></span>

[!code-csharp[ReadOnlyAutoProperty](../../../samples/snippets/csharp/new-in-6/newcode.cs#ReadOnlyAutoProperty)]

<span data-ttu-id="727fc-149">Le proprietà `FirstName` e `LastName` possono essere impostate solo nel corpo di un costruttore:</span><span class="sxs-lookup"><span data-stu-id="727fc-149">The `FirstName` and `LastName` properties can be set only in the body of a constructor:</span></span>

[!code-csharp[ReadOnlyAutoPropertyConstructor](../../../samples/snippets/csharp/new-in-6/newcode.cs#ReadOnlyAutoPropertyConstructor)]

<span data-ttu-id="727fc-150">Tentare di impostare `LastName` in un altro metodo genera un errore di compilazione `CS0200`:</span><span class="sxs-lookup"><span data-stu-id="727fc-150">Trying to set `LastName` in another method generates a `CS0200` compilation error:</span></span>

```csharp
public class Student
{
    public string LastName { get;  }

    public void ChangeName(string newLastName)
    {
        // Generates CS0200: Property or indexer cannot be assigned to -- it is read only
        LastName = newLastName;
    }
}
```

<span data-ttu-id="727fc-151">Questa funzionalità abilita un effettivo supporto del linguaggio per la creazione di tipi non modificabili e l'uso della sintassi più concisa e pratica per le proprietà automatiche.</span><span class="sxs-lookup"><span data-stu-id="727fc-151">This feature enables true language support for creating immutable types and using the more concise and convenient auto-property syntax.</span></span>

### <a name="auto-property-initializers"></a><span data-ttu-id="727fc-152">Inizializzatori di proprietà automatiche</span><span class="sxs-lookup"><span data-stu-id="727fc-152">Auto-Property Initializers</span></span>

<span data-ttu-id="727fc-153">Gli *inizializzatori di proprietà automatiche* consentono di dichiarare il valore iniziale per una proprietà automatica come parte della dichiarazione di proprietà.</span><span class="sxs-lookup"><span data-stu-id="727fc-153">*Auto-Property Initializers* let you declare the initial value for an auto-property as part of the property declaration.</span></span>  <span data-ttu-id="727fc-154">Nelle versioni precedenti queste proprietà dovevano avere dei setter che era necessario usare per inizializzare l'archiviazione dei dati usata dal campo sottostante.</span><span class="sxs-lookup"><span data-stu-id="727fc-154">In earlier versions, these properties would need to have setters and you would need to use that setter to initialize the data storage used by the backing field.</span></span> <span data-ttu-id="727fc-155">La classe dell'esempio seguente contiene il nome di uno studente e un elenco dei suoi voti:</span><span class="sxs-lookup"><span data-stu-id="727fc-155">Consider this class for a student that contains the name and a list of the student's grades:</span></span>

[!code-csharp[Construction](../../../samples/snippets/csharp/new-in-6/oldcode.cs#Construction)]
 
<span data-ttu-id="727fc-156">Man mano che la classe aumenta, è possibile includere altri costruttori.</span><span class="sxs-lookup"><span data-stu-id="727fc-156">As this class grows, you may include other constructors.</span></span> <span data-ttu-id="727fc-157">Ogni costruttore deve inizializzare questo campo oppure verranno introdotti errori.</span><span class="sxs-lookup"><span data-stu-id="727fc-157">Each constructor needs to initialize this field, or you'll introduce errors.</span></span>

<span data-ttu-id="727fc-158">C# 6 consente di assegnare un valore iniziale per la memoria usata da una proprietà automatica nella dichiarazione di proprietà automatica:</span><span class="sxs-lookup"><span data-stu-id="727fc-158">C# 6 enables you to assign an initial value for the storage used by an auto-property in the auto-property declaration:</span></span>

[!code-csharp[Initialization](../../../samples/snippets/csharp/new-in-6/newcode.cs#Initialization)]

<span data-ttu-id="727fc-159">Il membro `Grades` viene inizializzato dove è dichiarato.</span><span class="sxs-lookup"><span data-stu-id="727fc-159">The `Grades` member is initialized where it is declared.</span></span> <span data-ttu-id="727fc-160">Ciò rende più semplice eseguire l'inizializzazione esattamente una sola volta.</span><span class="sxs-lookup"><span data-stu-id="727fc-160">That makes it easier to perform the initialization exactly once.</span></span> <span data-ttu-id="727fc-161">L'inizializzazione fa parte della dichiarazione di proprietà e rende più semplice l'equivalenza tra l'allocazione di memoria e l'interfaccia pubblica per gli oggetti `Student`.</span><span class="sxs-lookup"><span data-stu-id="727fc-161">The initialization is part of the property declaration, making it easier to equate the storage allocation with public interface for `Student` objects.</span></span>

<span data-ttu-id="727fc-162">Inizializzatori di proprietà utilizzabile con le proprietà di lettura/scrittura, nonché le proprietà di sola lettura, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="727fc-162">Property Initializers can be used with read/write properties as well as read-only properties, as shown here.</span></span>

[!code-csharp[ReadWriteInitialization](../../../samples/snippets/csharp/new-in-6/newcode.cs#ReadWriteInitialization)]

## <a name="expression-bodied-function-members"></a><span data-ttu-id="727fc-163">Membri di funzione con corpo di espressione</span><span class="sxs-lookup"><span data-stu-id="727fc-163">Expression-bodied function members</span></span>

<span data-ttu-id="727fc-164">Il corpo di molti membri che si scrivono è costituito da un'unica istruzione che può essere rappresentata come un'espressione.</span><span class="sxs-lookup"><span data-stu-id="727fc-164">The body of a lot of members that we write consist of only one statement that can be represented as an expression.</span></span> <span data-ttu-id="727fc-165">È possibile ridurre la sintassi scrivendo in alternativa un membro con corpo di espressione.</span><span class="sxs-lookup"><span data-stu-id="727fc-165">You can reduce that syntax by writing an expression-bodied member instead.</span></span> <span data-ttu-id="727fc-166">Funziona per i metodi e proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="727fc-166">It works for methods and read-only properties.</span></span> <span data-ttu-id="727fc-167">Ad esempio, un override di `ToString()` è spesso un ottimo candidato:</span><span class="sxs-lookup"><span data-stu-id="727fc-167">For example, an override of `ToString()` is often a great candidate:</span></span>

[!code-csharp[ToStringExpressionMember](../../../samples/snippets/csharp/new-in-6/newcode.cs#ToStringExpressionMember)]

<span data-ttu-id="727fc-168">È inoltre possibile utilizzare membri densi espressione in nonché le proprietà di sola lettura:</span><span class="sxs-lookup"><span data-stu-id="727fc-168">You can also use expression-bodied members in read-only properties as well:</span></span>

[!code-csharp[FullNameExpressionMember](../../../samples/snippets/csharp/new-in-6/newcode.cs#FullNameExpressionMember)]

## <a name="using-static"></a><span data-ttu-id="727fc-169">using static</span><span class="sxs-lookup"><span data-stu-id="727fc-169">using static</span></span>

<span data-ttu-id="727fc-170">L'elemento *using static* consente di importare i metodi statici di una singola classe.</span><span class="sxs-lookup"><span data-stu-id="727fc-170">The *using static* enhancement enables you to import the static methods of a single class.</span></span> <span data-ttu-id="727fc-171">In precedenza l'istruzione `using` importava tutti i tipi in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="727fc-171">Previously, the `using` statement imported all types in a namespace.</span></span> 

<span data-ttu-id="727fc-172">Spesso i metodi statici di una classe vengono usati in tutto il codice.</span><span class="sxs-lookup"><span data-stu-id="727fc-172">Often we use a class' static methods throughout our code.</span></span> <span data-ttu-id="727fc-173">Digitare ripetutamente il nome della classe può nascondere il significato del codice.</span><span class="sxs-lookup"><span data-stu-id="727fc-173">Repeatedly typing the class name can obscure the meaning of your code.</span></span> <span data-ttu-id="727fc-174">Un esempio comune è quando si scrivono le classi che eseguono molti calcoli numerici.</span><span class="sxs-lookup"><span data-stu-id="727fc-174">A common example is when you write classes that perform many numeric calculations.</span></span>
<span data-ttu-id="727fc-175">Il codice verrà riempito di <xref:System.Math.Sin%2A>, <xref:System.Math.Sqrt%2A> e altre chiamate a metodi diversi nella classe <xref:System.Math>.</span><span class="sxs-lookup"><span data-stu-id="727fc-175">Your code will be littered with <xref:System.Math.Sin%2A>, <xref:System.Math.Sqrt%2A> and other calls to different methods in the <xref:System.Math> class.</span></span> <span data-ttu-id="727fc-176">La nuova sintassi di `using static` può rendere le classi molto più facili da leggere.</span><span class="sxs-lookup"><span data-stu-id="727fc-176">The new `using static` syntax can make these classes much cleaner to read.</span></span> <span data-ttu-id="727fc-177">Specificare la classe in uso:</span><span class="sxs-lookup"><span data-stu-id="727fc-177">You specify the class you're using:</span></span>

[!code-csharp[UsingStaticMath](../../../samples/snippets/csharp/new-in-6/newcode.cs#UsingStaticMath)]

<span data-ttu-id="727fc-178">A questo punto è possibile usare qualsiasi metodo statico nella classe <xref:System.Math> senza qualificare la classe <xref:System.Math>.</span><span class="sxs-lookup"><span data-stu-id="727fc-178">And now, you can use any static method in the <xref:System.Math> class without qualifying the <xref:System.Math> class.</span></span> <span data-ttu-id="727fc-179">La classe <xref:System.Math> è un caso di utilizzo ideale per questa funzionalità perché non contiene alcun metodo di istanza.</span><span class="sxs-lookup"><span data-stu-id="727fc-179">The <xref:System.Math> class is a great use case for this feature because it does not contain any instance methods.</span></span> <span data-ttu-id="727fc-180">È possibile usare `using static` anche per importare i metodi statici di una classe per una classe con metodi sia statici che di istanza.</span><span class="sxs-lookup"><span data-stu-id="727fc-180">You can also use `using static` to import a class' static methods for a class that has both static and instance methods.</span></span> <span data-ttu-id="727fc-181">Uno degli esempi più utili è <xref:System.String>:</span><span class="sxs-lookup"><span data-stu-id="727fc-181">One of the most useful examples is <xref:System.String>:</span></span>

[!code-csharp[UsingStatic](../../../samples/snippets/csharp/new-in-6/newcode.cs#UsingStatic)]

> [!NOTE]
> <span data-ttu-id="727fc-182">È necessario usare il nome completo della classe, `System.String`, in un'istruzione static using.</span><span class="sxs-lookup"><span data-stu-id="727fc-182">You must use the fully qualified class name, `System.String` in a static using statement.</span></span> <span data-ttu-id="727fc-183">Non è invece possibile usare la parola chiave `string`.</span><span class="sxs-lookup"><span data-stu-id="727fc-183">You cannot use the `string` keyword instead.</span></span> 

<span data-ttu-id="727fc-184">È ora possibile chiamare i metodi statici definiti nella classe <xref:System.String> senza qualificare tali metodi come membri della classe:</span><span class="sxs-lookup"><span data-stu-id="727fc-184">You can now call static methods defined in the <xref:System.String> class without qualifying those methods as members of that class:</span></span>

[!code-csharp[UsingStaticString](../../../samples/snippets/csharp/new-in-6/newcode.cs#UsingStaticString)]

<span data-ttu-id="727fc-185">La funzionalità `static using` e i metodi di estensione interagiscono in modi interessanti e la progettazione del linguaggio include alcune regole che riguardano espressamente tali interazioni.</span><span class="sxs-lookup"><span data-stu-id="727fc-185">The `static using` feature and extension methods interact in interesting ways, and the language design included some rules that specifically address those interactions.</span></span> <span data-ttu-id="727fc-186">L'obiettivo è ridurre al minimo le probabilità di modifiche di rilievo nelle codebase esistenti, inclusa quella in uso.</span><span class="sxs-lookup"><span data-stu-id="727fc-186">The goal is to minimize any chances of breaking changes in existing codebases, including yours.</span></span>

<span data-ttu-id="727fc-187">I metodi di estensione sono nell'ambito solo se vengono chiamati usando la sintassi di chiamata al metodo di estensione, non se vengono chiamati come metodo statico.</span><span class="sxs-lookup"><span data-stu-id="727fc-187">Extension methods are only in scope when called using the extension method invocation syntax, not when called as a static method.</span></span>
<span data-ttu-id="727fc-188">Questa situazione si verifica spesso nelle query LINQ.</span><span class="sxs-lookup"><span data-stu-id="727fc-188">You'll often see this in LINQ queries.</span></span> <span data-ttu-id="727fc-189">È possibile importare il modello LINQ importando <xref:System.Linq.Enumerable>.</span><span class="sxs-lookup"><span data-stu-id="727fc-189">You can import the LINQ pattern by importing <xref:System.Linq.Enumerable>.</span></span>

[!code-csharp[UsingStaticLinq](../../../samples/snippets/csharp/new-in-6/newcode.cs#usingStaticLinq)]

<span data-ttu-id="727fc-190">In questo modo tutti i metodi vengono importati nella classe <xref:System.Linq.Enumerable>.</span><span class="sxs-lookup"><span data-stu-id="727fc-190">This imports all the methods in the <xref:System.Linq.Enumerable> class.</span></span>
<span data-ttu-id="727fc-191">Tuttavia, i metodi di estensione sono nell'ambito solo quando vengono chiamati come metodi di estensione.</span><span class="sxs-lookup"><span data-stu-id="727fc-191">However, the extension methods are only in scope when called as extension methods.</span></span> <span data-ttu-id="727fc-192">Non sono nell'ambito se vengono chiamati usando la sintassi del metodo statico:</span><span class="sxs-lookup"><span data-stu-id="727fc-192">They are not in scope if they are called using the static method syntax:</span></span>

[!code-csharp[UsingStaticLinqMethod](../../../samples/snippets/csharp/new-in-6/newcode.cs#UsingStaticLinkMethod)]

<span data-ttu-id="727fc-193">Questa decisione è dovuta al fatto che i metodi di estensione di solito vengono chiamati usando espressioni di chiamata al metodo di estensione.</span><span class="sxs-lookup"><span data-stu-id="727fc-193">This decision is because extension methods are typically called using extension method invocation expressions.</span></span> <span data-ttu-id="727fc-194">Nel caso improbabile in cui vengano chiamati usando la sintassi di chiamata al metodo statico il motivo è che deve essere risolta l'ambiguità.</span><span class="sxs-lookup"><span data-stu-id="727fc-194">In the rare case where they are called using the static method call syntax it is to resolve ambiguity.</span></span>
<span data-ttu-id="727fc-195">Richiedere il nome della classe come parte della chiamata è una scelta opportuna.</span><span class="sxs-lookup"><span data-stu-id="727fc-195">Requiring the class name as part of the invocation seems wise.</span></span>

<span data-ttu-id="727fc-196">Esiste un'ultima funzionalità di `static using`.</span><span class="sxs-lookup"><span data-stu-id="727fc-196">There's one last feature of `static using`.</span></span> <span data-ttu-id="727fc-197">La direttiva `static using` importa anche tutti i tipi annidati.</span><span class="sxs-lookup"><span data-stu-id="727fc-197">The `static using` directive also imports any nested types.</span></span> <span data-ttu-id="727fc-198">Ciò consente di fare riferimento a tutti i tipi annidati senza qualifica.</span><span class="sxs-lookup"><span data-stu-id="727fc-198">That enables you to reference any nested types without qualification.</span></span>

## <a name="null-conditional-operators"></a><span data-ttu-id="727fc-199">Operatori condizionali Null</span><span class="sxs-lookup"><span data-stu-id="727fc-199">Null-conditional operators</span></span>

<span data-ttu-id="727fc-200">I valori Null complicano il codice.</span><span class="sxs-lookup"><span data-stu-id="727fc-200">Null values complicate code.</span></span> <span data-ttu-id="727fc-201">È necessario controllare ogni accesso delle variabili per verificare che non vi sia dereferenziazione di `null`.</span><span class="sxs-lookup"><span data-stu-id="727fc-201">You need to check every access of variables to ensure you are not dereferencing `null`.</span></span> <span data-ttu-id="727fc-202">L'*operatore condizionale Null* rende tali controlli molto più semplici e fluidi.</span><span class="sxs-lookup"><span data-stu-id="727fc-202">The *null conditional operator* makes those checks much easier and fluid.</span></span>

<span data-ttu-id="727fc-203">È sufficiente sostituire l'accesso ai membri `.` con `?.`:</span><span class="sxs-lookup"><span data-stu-id="727fc-203">Simply replace the member access `.` with `?.`:</span></span>

[!code-csharp[NullConditional](../../../samples/snippets/csharp/new-in-6/program.cs#NullConditional)]

<span data-ttu-id="727fc-204">Nell'esempio precedente alla variabile `first` è assegnato `null` se l'oggetto person è `null`.</span><span class="sxs-lookup"><span data-stu-id="727fc-204">In the preceding example, the variable `first` is assigned `null` if the person object is `null`.</span></span> <span data-ttu-id="727fc-205">In caso contrario, viene assegnato il valore della proprietà `FirstName`.</span><span class="sxs-lookup"><span data-stu-id="727fc-205">Otherwise, it gets assigned the value of the `FirstName` property.</span></span> <span data-ttu-id="727fc-206">In particolare, il carattere `?.` indica che questa riga di codice non genera `NullReferenceException` quando la variabile `person` è `null`.</span><span class="sxs-lookup"><span data-stu-id="727fc-206">Most importantly, the `?.` means that this line of code does not generate a `NullReferenceException` when the `person` variable is `null`.</span></span> <span data-ttu-id="727fc-207">Provoca invece un corto circuito e produce `null`.</span><span class="sxs-lookup"><span data-stu-id="727fc-207">Instead, it short-circuits and produces `null`.</span></span>

<span data-ttu-id="727fc-208">Inoltre, tenere presente che questa espressione restituisce un oggetto `string`, indipendentemente dal valore di `person`.</span><span class="sxs-lookup"><span data-stu-id="727fc-208">Also, note that this expression returns a `string`, regardless of the value of `person`.</span></span>
<span data-ttu-id="727fc-209">In caso di operazioni di corto circuito, il valore `null` restituito è tipizzato in modo da corrispondere all'espressione completa.</span><span class="sxs-lookup"><span data-stu-id="727fc-209">In the case of short circuiting, the `null` value returned is typed to match the full expression.</span></span>

<span data-ttu-id="727fc-210">Spesso è possibile usare questo costrutto con l'operatore *Null ridondante* per assegnare valori predefiniti quando una delle proprietà è `null`:</span><span class="sxs-lookup"><span data-stu-id="727fc-210">You can often use this construct with the *null coalescing* operator to assign default values when one of the properties are `null`:</span></span>

[!code-csharp[NullCoalescing](../../../samples/snippets/csharp/new-in-6/program.cs#NullCoalescing)]

<span data-ttu-id="727fc-211">L'operando di destra dell'operatore `?.` non è limitato ai campi o alle proprietà.</span><span class="sxs-lookup"><span data-stu-id="727fc-211">The right hand side operand of the `?.` operator is not limited to properties or fields.</span></span>
<span data-ttu-id="727fc-212">È possibile usarlo anche per richiamare i metodi in modo condizionale.</span><span class="sxs-lookup"><span data-stu-id="727fc-212">You can also use it to conditionally invoke methods.</span></span> <span data-ttu-id="727fc-213">L'uso più comune delle funzioni membro con l'operatore condizionale Null è richiamare in modo sicuro i delegati (o i gestori di eventi) che possono essere `null`.</span><span class="sxs-lookup"><span data-stu-id="727fc-213">The most common use of member functions with the null conditional operator is to safely invoke delegates (or event handlers) that may be `null`.</span></span>  <span data-ttu-id="727fc-214">Questa operazione si esegue chiamando il metodo `Invoke` del delegato usando l'operatore `?.` per accedere al membro.</span><span class="sxs-lookup"><span data-stu-id="727fc-214">You'll do this by calling the delegate's `Invoke` method using the `?.` operator to access the member.</span></span> <span data-ttu-id="727fc-215">È disponibile un esempio nell'argomento</span><span class="sxs-lookup"><span data-stu-id="727fc-215">You can see an example in the</span></span>  
<span data-ttu-id="727fc-216">relativo ai [modelli di delegato](../delegates-patterns.md#handling-null-delegates).</span><span class="sxs-lookup"><span data-stu-id="727fc-216">[delegate patterns](../delegates-patterns.md#handling-null-delegates) topic.</span></span>

<span data-ttu-id="727fc-217">Le regole dell'operatore `?.` garantiscono che il lato sinistro dell'operatore venga valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="727fc-217">The rules of the `?.` operator ensure that the left-hand side of the operator is evaluated only once.</span></span> <span data-ttu-id="727fc-218">Questo è importante e abilita molti idiomi, incluso l'esempio che usa i gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="727fc-218">This is important and enables many idioms, including the example using event handlers.</span></span> <span data-ttu-id="727fc-219">Iniziamo con l'uso del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="727fc-219">Let's start with the event handler usage.</span></span> <span data-ttu-id="727fc-220">Nelle versioni precedenti di C# l'utente era invitato a scrivere codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="727fc-220">In previous versions of C#, you were encouraged to write code like this:</span></span>

```csharp
var handler = this.SomethingHappened;
if (handler != null)
    handler(this, eventArgs);
```

<span data-ttu-id="727fc-221">Si preferiva questo codice a una sintassi più semplice:</span><span class="sxs-lookup"><span data-stu-id="727fc-221">This was preferred over a simpler syntax:</span></span>

```csharp
// Not recommended
if (this.SomethingHappened != null)
    this.SomethingHappened(this, eventArgs);
```

> [!IMPORTANT]
> <span data-ttu-id="727fc-222">L'esempio precedente introduce una race condition.</span><span class="sxs-lookup"><span data-stu-id="727fc-222">The preceding example introduces a race condition.</span></span> <span data-ttu-id="727fc-223">L'evento `SomethingHappened` può presentare dei sottoscrittori quando viene confrontato con `null` e tali sottoscrittori possono essere stati rimossi prima della generazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="727fc-223">The `SomethingHappened` event may have subscribers when checked against `null`, and those subscribers may have been removed before the event is raised.</span></span> <span data-ttu-id="727fc-224">Questo può causare la generazione di <xref:System.NullReferenceException>.</span><span class="sxs-lookup"><span data-stu-id="727fc-224">That would cause a <xref:System.NullReferenceException> to be thrown.</span></span>

<span data-ttu-id="727fc-225">In questa seconda versione il gestore dell'evento `SomethingHappened` potrebbe non essere Null durante il test, ma se un altro codice rimuove un gestore, potrebbe essere ancora Null quando viene chiamato il gestore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="727fc-225">In this second version, the `SomethingHappened` event handler might be non-null when tested, but if other code removes a handler, it could still be null when the event handler was called.</span></span>

<span data-ttu-id="727fc-226">Il compilatore genera codice per l'operatore `?.` che garantisce che il lato sinistro (`this.SomethingHappened`) dell'espressione `?.` venga valutato una sola volta e che il risultato sia memorizzato nella cache:</span><span class="sxs-lookup"><span data-stu-id="727fc-226">The compiler generates code for the `?.` operator that ensures the left side (`this.SomethingHappened`) of the `?.` expression is evaluated once, and the result is cached:</span></span>

```csharp
// preferred in C# 6:
this.SomethingHappened?.Invoke(this, eventArgs);
```

<span data-ttu-id="727fc-227">Verificare che il lato sinistro venga valutato una sola volta consente inoltre di usare qualsiasi espressione, comprese le chiamate ai metodi, sul lato sinistro di `?.` Anche se hanno effetti collaterali, i valori vengono valutati una volta, quindi gli effetti collaterali si verificano una sola volta.</span><span class="sxs-lookup"><span data-stu-id="727fc-227">Ensuring that the left side is evaluated only once also enables you to use any expression, including method calls, on the left side of the `?.` Even if these have side-effects, they are evaluated once, so the side effects occur only once.</span></span> <span data-ttu-id="727fc-228">È possibile vedere un esempio nell'argomento relativo agli [eventi](../events-overview.md#language-support-for-events).</span><span class="sxs-lookup"><span data-stu-id="727fc-228">You can see an example in our content on [events](../events-overview.md#language-support-for-events).</span></span>

## <a name="string-interpolation"></a><span data-ttu-id="727fc-229">Interpolazione di stringhe</span><span class="sxs-lookup"><span data-stu-id="727fc-229">String Interpolation</span></span>

<span data-ttu-id="727fc-230">C# 6 contiene una nuova sintassi per la composizione di stringhe da una stringa di formato e di espressioni che possono essere valutate per produrre altri valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="727fc-230">C# 6 contains new syntax for composing strings from a format string and expressions that can be evaluated to produce other string values.</span></span>

<span data-ttu-id="727fc-231">Di solito era necessario usare parametri posizionali in un metodo come `string.Format`:</span><span class="sxs-lookup"><span data-stu-id="727fc-231">Traditionally, you needed to use positional parameters in a method like `string.Format`:</span></span>

[!code-csharp[stringFormat](../../../samples/snippets/csharp/new-in-6/oldcode.cs#stringFormat)]

<span data-ttu-id="727fc-232">Con C# 6 la nuova funzionalità di interpolazione delle stringhe consente di incorporare le espressioni nella stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="727fc-232">With C# 6, the new string interpolation feature enables you to embed the expressions in the format string.</span></span> <span data-ttu-id="727fc-233">Basta far precedere la stringa da `$`:</span><span class="sxs-lookup"><span data-stu-id="727fc-233">Simple preface the string with `$`:</span></span>

[!code-csharp[stringInterpolation](../../../samples/snippets/csharp/new-in-6/newcode.cs#FullNameExpressionMember)]

<span data-ttu-id="727fc-234">In questo esempio sono state usate espressioni variabili per le espressioni sostituite.</span><span class="sxs-lookup"><span data-stu-id="727fc-234">This initial example used variable expressions for the substituted expressions.</span></span> <span data-ttu-id="727fc-235">È possibile espandere questa sintassi per usare qualsiasi espressione.</span><span class="sxs-lookup"><span data-stu-id="727fc-235">You can expand on this syntax to use any expression.</span></span> <span data-ttu-id="727fc-236">Ad esempio, è possibile calcolare la media dei voti di uno studente come parte dell'interpolazione:</span><span class="sxs-lookup"><span data-stu-id="727fc-236">For example, you could compute a student's grade point average as part of the interpolation:</span></span>

[!code-csharp[stringInterpolationExpression](../../../samples/snippets/csharp/new-in-6/newcode.cs#stringInterpolationExpression)]

<span data-ttu-id="727fc-237">Eseguendo l'esempio precedente si può vedere che l'output per `Grades.Average()` potrebbe avere più posizioni decimali del necessario.</span><span class="sxs-lookup"><span data-stu-id="727fc-237">Running the preceding example, you would find that the output for `Grades.Average()` might have more decimal places than you would like.</span></span> <span data-ttu-id="727fc-238">La sintassi di interpolazione delle stringhe supporta tutte le stringhe di formato disponibili usando i metodi di formattazione precedenti.</span><span class="sxs-lookup"><span data-stu-id="727fc-238">The string interpolation syntax supports all the format strings available using earlier formatting methods.</span></span> <span data-ttu-id="727fc-239">Aggiungere le stringhe di formato tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="727fc-239">You add the format strings inside the braces.</span></span> <span data-ttu-id="727fc-240">Aggiungere `:` dopo l'espressione da formattare:</span><span class="sxs-lookup"><span data-stu-id="727fc-240">Add a `:` following the expression to format:</span></span>

[!code-csharp[stringInterpolationFormat](../../../samples/snippets/csharp/new-in-6/newcode.cs#stringInterpolationFormat)]

<span data-ttu-id="727fc-241">La riga di codice precedente formatterà il valore per `Grades.Average()` come numero a virgola mobile con due cifre decimali.</span><span class="sxs-lookup"><span data-stu-id="727fc-241">The preceding line of code will format the value for `Grades.Average()` as a floating-point number with two decimal places.</span></span>

<span data-ttu-id="727fc-242">Il carattere `:` viene sempre interpretato come separatore tra l'espressione da formattare e la stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="727fc-242">The `:` is always interpreted as the separator between the expression being formatted and the format string.</span></span> <span data-ttu-id="727fc-243">Questo può causare problemi quando l'espressione usa il carattere `:` in altro modo, ad esempio come operatore condizionale:</span><span class="sxs-lookup"><span data-stu-id="727fc-243">This can introduce problems when your expression uses a `:` in another way, such as a conditional operator:</span></span>

```csharp
public string GetGradePointPercentages() =>
    $"Name: {LastName}, {FirstName}. G.P.A: {Grades.Any() ? Grades.Average() : double.NaN:F2}";
```

<span data-ttu-id="727fc-244">Nell'esempio precedente il carattere `:` viene analizzato come inizio della stringa di formato, non come parte dell'operatore condizionale.</span><span class="sxs-lookup"><span data-stu-id="727fc-244">In the preceding example, the `:` is parsed as the beginning of the format string, not part of the conditional operator.</span></span> <span data-ttu-id="727fc-245">In tutti i casi in cui ciò accade è possibile racchiudere l'espressione tra parentesi per indurre il compilatore a interpretare l'espressione come previsto:</span><span class="sxs-lookup"><span data-stu-id="727fc-245">In all cases where this happens, you can surround the expression with parentheses to force the compiler to interpret the expression as you intend:</span></span>

[!code-csharp[stringInterpolationConditional](../../../samples/snippets/csharp/new-in-6/newcode.cs#stringInterpolationConditional)]

<span data-ttu-id="727fc-246">Non vi sono limitazioni per le espressioni che si possono inserire tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="727fc-246">There aren't any limitations on the expressions you can place between the braces.</span></span> <span data-ttu-id="727fc-247">È possibile eseguire una query LINQ complessa all'interno di una stringa interpolata per effettuare calcoli e visualizzare il risultato:</span><span class="sxs-lookup"><span data-stu-id="727fc-247">You can execute a complex LINQ query inside an interpolated string to perform computations and display the result:</span></span>

[!code-csharp[stringInterpolationLinq](../../../samples/snippets/csharp/new-in-6/newcode.cs#stringInterpolationLinq)]

<span data-ttu-id="727fc-248">Da questo esempio risulta che è anche possibile annidare un'espressione di interpolazione di stringhe all'interno di un'altra espressione di interpolazione di stringhe.</span><span class="sxs-lookup"><span data-stu-id="727fc-248">You can see from this sample that you can even nest a string interpolation expression inside another string interpolation expression.</span></span> <span data-ttu-id="727fc-249">Questo esempio è probabilmente più complesso del necessario nel codice di produzione,</span><span class="sxs-lookup"><span data-stu-id="727fc-249">This example is very likely more complex than you would want in production code.</span></span>
<span data-ttu-id="727fc-250">ma illustra in modo efficace la portata della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="727fc-250">Rather, it is illustrative of the breadth of the feature.</span></span> <span data-ttu-id="727fc-251">Qualsiasi espressione C# può essere inserita tra parentesi graffe in una stringa interpolata.</span><span class="sxs-lookup"><span data-stu-id="727fc-251">Any C# expression can be placed between the curly braces of an interpolated string.</span></span>

### <a name="string-interpolation-and-specific-cultures"></a><span data-ttu-id="727fc-252">Interpolazione delle stringhe e impostazioni cultura specifiche</span><span class="sxs-lookup"><span data-stu-id="727fc-252">String interpolation and specific cultures</span></span>

<span data-ttu-id="727fc-253">Tutti gli esempi illustrati nella sezione precedente formattano le stringhe usando la lingua e le impostazioni cultura correnti del computer in cui viene eseguito il codice.</span><span class="sxs-lookup"><span data-stu-id="727fc-253">All the examples shown in the preceding section will format the strings using the current culture and language on the machine where the code executes.</span></span> <span data-ttu-id="727fc-254">Spesso può essere necessario formattare la stringa prodotta usando impostazioni cultura specifiche.</span><span class="sxs-lookup"><span data-stu-id="727fc-254">Often you may need to format the string produced using a specific culture.</span></span>
<span data-ttu-id="727fc-255">L'oggetto prodotto da un'interpolazione di stringhe è un tipo con conversione implicita a <xref:System.String> o <xref:System.FormattableString>.</span><span class="sxs-lookup"><span data-stu-id="727fc-255">The object produced from a string interpolation is a type that has an implicit conversion to either <xref:System.String> or <xref:System.FormattableString>.</span></span>

<span data-ttu-id="727fc-256">Il tipo <xref:System.FormattableString> contiene la stringa di formato e i risultati della valutazione degli argomenti prima della conversione degli stessi in stringhe.</span><span class="sxs-lookup"><span data-stu-id="727fc-256">The <xref:System.FormattableString> type contains the format string, and the results of evaluating the arguments before converting them to strings.</span></span> <span data-ttu-id="727fc-257">È possibile usare i metodi pubblici di <xref:System.FormattableString> per specificare le impostazioni cultura quando si formatta una stringa.</span><span class="sxs-lookup"><span data-stu-id="727fc-257">You can use public methods of <xref:System.FormattableString> to specify the culture when formatting a string.</span></span> <span data-ttu-id="727fc-258">Ad esempio, il codice seguente produce una stringa utilizzando il tedesco come lingua e impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="727fc-258">For example, the following will produce a string using German as the language and culture.</span></span> <span data-ttu-id="727fc-259">Verrà usato il carattere ',' come separatore decimale e il carattere '.' come separatore delle migliaia.</span><span class="sxs-lookup"><span data-stu-id="727fc-259">(It will use the ',' character for the decimal separator, and the '.' character as the thousands separator.)</span></span>

```csharp
FormattableString str = $"Average grade is {s.Grades.Average()}";
var gradeStr = string.Format(null, 
    System.Globalization.CultureInfo.CreateSpecificCulture("de-de"),
    str.GetFormat(), str.GetArguments());
```

> [!NOTE]
> <span data-ttu-id="727fc-260">L'esempio precedente non è supportato in .NET Core versione 1.0.1.</span><span class="sxs-lookup"><span data-stu-id="727fc-260">The preceding example is not supported in .NET Core version 1.0.1.</span></span> <span data-ttu-id="727fc-261">È supportato solo in .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="727fc-261">It is only supported in the .NET Framework.</span></span>

<span data-ttu-id="727fc-262">In generale, le espressioni di interpolazione di stringhe producono stringhe come output.</span><span class="sxs-lookup"><span data-stu-id="727fc-262">In general, string interpolation expressions produce strings as their output.</span></span> <span data-ttu-id="727fc-263">Tuttavia, per avere un maggiore controllo sulle impostazioni cultura usate per formattare la stringa, è possibile definire un output specifico.</span><span class="sxs-lookup"><span data-stu-id="727fc-263">However, when you want greater control over the culture used to format the string, you can specify a specific output.</span></span>  <span data-ttu-id="727fc-264">Se è spesso necessario usare questa funzionalità, è possibile creare metodi pratici, come i metodi di estensione, per abilitare la formattazione semplice con impostazioni cultura specifiche.</span><span class="sxs-lookup"><span data-stu-id="727fc-264">If this is a capability you often need, you can create convenience methods, as extension methods, to enable easy formatting with specific cultures.</span></span>

## <a name="exception-filters"></a><span data-ttu-id="727fc-265">Filtri eccezioni</span><span class="sxs-lookup"><span data-stu-id="727fc-265">Exception Filters</span></span>

<span data-ttu-id="727fc-266">Un'altra nuova funzionalità di C# 6 sono i *filtri eccezioni*.</span><span class="sxs-lookup"><span data-stu-id="727fc-266">Another new feature in C# 6 is *exception filters*.</span></span> <span data-ttu-id="727fc-267">I filtri eccezioni sono clausole che determinano quando deve essere applicata una determinata clausola catch.</span><span class="sxs-lookup"><span data-stu-id="727fc-267">Exception Filters are clauses that determine when a given catch clause should be applied.</span></span>
<span data-ttu-id="727fc-268">Se l'espressione usata per un filtro eccezioni restituisce `true`, la clausola catch esegue la normale elaborazione per un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="727fc-268">If the expression used for an exception filter evaluates to `true`, the catch clause performs its normal processing on an exception.</span></span> <span data-ttu-id="727fc-269">Se l'espressione restituisce `false`, la clausola `catch` viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="727fc-269">If the expression evaluates to `false`, then the `catch` clause is skipped.</span></span>

<span data-ttu-id="727fc-270">Un utilizzo consiste nell'esaminare le informazioni relative a un'eccezione per determinare se una clausola `catch` può elaborare l'eccezione:</span><span class="sxs-lookup"><span data-stu-id="727fc-270">One use is to examine information about an exception to determine if a `catch` clause can process the exception:</span></span>

[!code-csharp[ExceptionFilter](../../../samples/snippets/csharp/new-in-6/NetworkClient.cs#ExceptionFilter)]

<span data-ttu-id="727fc-271">Il codice generato dai filtri eccezioni offre informazioni più complete su un'eccezione generata e non elaborata.</span><span class="sxs-lookup"><span data-stu-id="727fc-271">The code generated by exception filters provides better information about an exception that is thrown and not processed.</span></span> <span data-ttu-id="727fc-272">Prima di aggiungere filtri eccezioni al linguaggio, è necessario creare un codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="727fc-272">Before exception filters were added to the language, you would need to create code like the following:</span></span>

[!code-csharp[ExceptionFilterOld](../../../samples/snippets/csharp/new-in-6/NetworkClient.cs#ExceptionFilterOld)]

<span data-ttu-id="727fc-273">Il punto in cui viene generata l'eccezione cambia da un esempio all'altro.</span><span class="sxs-lookup"><span data-stu-id="727fc-273">The point where the exception is thrown changes between these two examples.</span></span>
<span data-ttu-id="727fc-274">Nel codice precedente, dove viene usata una clausola `throw`, qualsiasi analisi dello stack o esame dei dettagli di arresto anomalo del sistema indicherà che l'eccezione è stata generata dall'istruzione `throw` nella clausola catch.</span><span class="sxs-lookup"><span data-stu-id="727fc-274">In the previous code, where a `throw` clause is used, any stack trace analysis or examination of crash dumps will show that the exception was thrown from the `throw` statement in your catch clause.</span></span> <span data-ttu-id="727fc-275">L'oggetto eccezione effettivo contiene lo stack di chiamate originale, ma tutte le altre informazioni sulle variabili dello stack di chiamate tra questo punto di generazione e la posizione del punto di generazione originale sono state perse.</span><span class="sxs-lookup"><span data-stu-id="727fc-275">The actual exception object will contain the original call stack, but all other information about any variables in the call stack between this throw point and the location of the original throw point has been lost.</span></span> 

<span data-ttu-id="727fc-276">Se si confronta questa situazione con il modo in cui viene elaborato il codice che usa un filtro eccezioni, si vedrà che l'espressione del filtro eccezioni restituisce `false`.</span><span class="sxs-lookup"><span data-stu-id="727fc-276">Contrast that with how the code using an exception filter is processed: the exception filter expression evaluates to `false`.</span></span> <span data-ttu-id="727fc-277">Di conseguenza, l'esecuzione non usa mai la clausola `catch`.</span><span class="sxs-lookup"><span data-stu-id="727fc-277">Therefore, execution never enters the `catch` clause.</span></span> <span data-ttu-id="727fc-278">Poiché la clausola `catch` non viene eseguita, non avviene alcuna rimozione dello stack.</span><span class="sxs-lookup"><span data-stu-id="727fc-278">Because the `catch` clause does not execute, no stack unwinding takes place.</span></span> <span data-ttu-id="727fc-279">Ciò significa che il percorso di generazione originale viene mantenuto per tutte le attività di debug eseguite successivamente.</span><span class="sxs-lookup"><span data-stu-id="727fc-279">That means the original throw location is preserved for any debugging activities that would take place later.</span></span>

<span data-ttu-id="727fc-280">Ogni volta che è necessario valutare i campi o le proprietà di un'eccezione, anziché basarsi esclusivamente sul tipo di eccezione, usare un filtro eccezioni per conservare più informazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="727fc-280">Whenever you need to evaluate fields or properties of an exception, instead of relying solely on the exception type, use an exception filter to preserve more debugging information.</span></span>

<span data-ttu-id="727fc-281">Un altro modello consigliato con i filtri eccezioni è l'uso dei filtri per la registrazione delle routine.</span><span class="sxs-lookup"><span data-stu-id="727fc-281">Another recommended pattern with exception filters is to use them for logging routines.</span></span> <span data-ttu-id="727fc-282">In questo caso si sfrutta anche il modo in cui viene mantenuto il punto di generazione delle eccezioni quando un filtro eccezioni restituisce `false`.</span><span class="sxs-lookup"><span data-stu-id="727fc-282">This usage also leverages the manner in which the exception throw point is preserved when an exception filter evaluates to `false`.</span></span>

<span data-ttu-id="727fc-283">Un metodo di registrazione sarebbe un metodo il cui argomento è l'eccezione che restituisce in modo non condizionale `false`:</span><span class="sxs-lookup"><span data-stu-id="727fc-283">A logging method would be a method whose argument is the exception that unconditionally returns `false`:</span></span>

[!code-csharp[ExceptionFilterLogging](../../../samples/snippets/csharp/new-in-6/ExceptionFilterHelpers.cs#ExceptionFilterLogging)]

<span data-ttu-id="727fc-284">Ogni volta che si vuole registrare un'eccezione, è possibile aggiungere una clausola catch e usare questo metodo come filtro eccezioni:</span><span class="sxs-lookup"><span data-stu-id="727fc-284">Whenever you want to log an exception, you can add a catch clause, and use this method as the exception filter:</span></span>

[!code-csharp[LogException](../../../samples/snippets/csharp/new-in-6/program.cs#LogException)]

<span data-ttu-id="727fc-285">Le eccezioni non vengono mai intercettate perché il metodo `LogException` restituisce sempre `false`.</span><span class="sxs-lookup"><span data-stu-id="727fc-285">The exceptions are never caught, because the `LogException` method always returns `false`.</span></span> <span data-ttu-id="727fc-286">Il filtro eccezioni sempre false indica che è possibile inserire questo gestore di registrazione prima di eventuali altri gestori di eccezioni:</span><span class="sxs-lookup"><span data-stu-id="727fc-286">That always false exception filter means that you can place this logging handler before any other exception handlers:</span></span>

[!code-csharp[LogExceptionRecovery](../../../samples/snippets/csharp/new-in-6/program.cs#LogExceptionRecovery)]

<span data-ttu-id="727fc-287">Nell'esempio precedente viene evidenziato un aspetto molto importante dei filtri eccezioni.</span><span class="sxs-lookup"><span data-stu-id="727fc-287">The preceding example highlights a very important facet of exception filters.</span></span>
<span data-ttu-id="727fc-288">I filtri eccezioni consentono scenari in cui una clausola catch delle eccezioni più generale può apparire prima di una clausola più specifica.</span><span class="sxs-lookup"><span data-stu-id="727fc-288">The exception filters enable scenarios where a more general exception catch clause may appear before a more specific one.</span></span> <span data-ttu-id="727fc-289">È anche possibile visualizzare lo stesso tipo di eccezione in più clausole catch:</span><span class="sxs-lookup"><span data-stu-id="727fc-289">It's also possible to have the same exception type appear in multiple catch clauses:</span></span>

[!code-csharp[HandleNotChanged](../../../samples/snippets/csharp/new-in-6/NetworkClient.cs#HandleNotChanged)]

<span data-ttu-id="727fc-290">Un altro modello consigliato consente di impedire alle clausole catch di elaborare le eccezioni quando viene collegato un debugger.</span><span class="sxs-lookup"><span data-stu-id="727fc-290">Another recommended pattern helps prevent catch clauses from processing exceptions when a debugger is attached.</span></span> <span data-ttu-id="727fc-291">Questa tecnica consente di eseguire un'applicazione con il debugger e arrestare l'esecuzione quando viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="727fc-291">This technique enables you to run an application with the debugger, and stop execution when an exception is thrown.</span></span>

<span data-ttu-id="727fc-292">Nel codice aggiungere un filtro eccezioni in modo tale che l'eventuale codice di ripristino venga eseguito solo quando non è collegato un debugger:</span><span class="sxs-lookup"><span data-stu-id="727fc-292">In your code, add an exception filter so that any recovery code executes only when a debugger is not attached:</span></span>

[!code-csharp[LogExceptionDebugger](../../../samples/snippets/csharp/new-in-6/program.cs#LogExceptionDebugger)]

<span data-ttu-id="727fc-293">Dopo aver aggiunto questo elemento al codice impostare il debugger in modo da interrompere tutte le eccezioni non gestite.</span><span class="sxs-lookup"><span data-stu-id="727fc-293">After adding this in code, you set your debugger to break on all unhandled exceptions.</span></span> <span data-ttu-id="727fc-294">Eseguire il programma nel debugger e il debugger si interrompe ogni volta che `PerformFailingOperation()` genera `RecoverableException`.</span><span class="sxs-lookup"><span data-stu-id="727fc-294">Run the program under the debugger, and the debugger breaks whenever `PerformFailingOperation()` throws a `RecoverableException`.</span></span>
<span data-ttu-id="727fc-295">Il debugger interrompe il programma perché la clausola catch non verrà eseguita a causa del filtro eccezioni che restituisce false.</span><span class="sxs-lookup"><span data-stu-id="727fc-295">The debugger breaks your program, because the catch clause won't be executed due to the false-returning exception filter.</span></span>

## <a name="nameof-expressions"></a><span data-ttu-id="727fc-296">Espressioni `nameof`</span><span class="sxs-lookup"><span data-stu-id="727fc-296">`nameof` Expressions</span></span>

<span data-ttu-id="727fc-297">L'espressione `nameof` restituisce il nome di un simbolo.</span><span class="sxs-lookup"><span data-stu-id="727fc-297">The `nameof` expression evaluates to the name of a symbol.</span></span> <span data-ttu-id="727fc-298">È un sistema efficace per garantire il funzionamento degli strumenti ogni volta che è necessario il nome di una variabile, una proprietà o un campo membro.</span><span class="sxs-lookup"><span data-stu-id="727fc-298">It's a great way to get tools working whenever you need the name of a variable, a property, or a member field.</span></span>

<span data-ttu-id="727fc-299">Uno degli usi più comuni di `nameof` è specificare il nome di un simbolo che ha causato un'eccezione:</span><span class="sxs-lookup"><span data-stu-id="727fc-299">One of the most common uses for `nameof` is to provide the name of a symbol that caused an exception:</span></span>

[!code-csharp[nameof](../../../samples/snippets/csharp/new-in-6/NewCode.cs#UsingStaticString)]

<span data-ttu-id="727fc-300">Un altro uso è con le applicazioni basate su XAML che implementano l'interfaccia `INotifyPropertyChanged`:</span><span class="sxs-lookup"><span data-stu-id="727fc-300">Another use is with XAML based applications that implement the `INotifyPropertyChanged` interface:</span></span>

[!code-csharp[nameofNotify](../../../samples/snippets/csharp/new-in-6/viewmodel.cs#nameofNotify)]

<span data-ttu-id="727fc-301">Il vantaggio dell'uso dell'operatore `nameof` per una stringa costante è che gli strumenti sono in grado di interpretare il simbolo.</span><span class="sxs-lookup"><span data-stu-id="727fc-301">The advantage of using the `nameof` operator over a constant string is that tools can understand the symbol.</span></span> <span data-ttu-id="727fc-302">Se si usano strumenti di refactoring per rinominare il simbolo, verrà rinominato nell'espressione `nameof`.</span><span class="sxs-lookup"><span data-stu-id="727fc-302">If you use refactoring tools to rename the symbol, it will rename it in the `nameof` expression.</span></span> <span data-ttu-id="727fc-303">Le stringhe costanti non offrono tale vantaggio.</span><span class="sxs-lookup"><span data-stu-id="727fc-303">Constant strings don't have that advantage.</span></span> <span data-ttu-id="727fc-304">Provare a rinominare una variabile nell'editor preferito: tutte le espressioni `nameof` verranno a loro volta aggiornate.</span><span class="sxs-lookup"><span data-stu-id="727fc-304">Try it yourself in your favorite editor: rename a variable, and any `nameof` expressions will update as well.</span></span>

<span data-ttu-id="727fc-305">L'espressione `nameof` produce il nome non qualificato del proprio argomento (`LastName` negli esempi precedenti) anche se si usa il nome completo dell'argomento:</span><span class="sxs-lookup"><span data-stu-id="727fc-305">The `nameof` expression produces the unqualified name of its argument (`LastName` in the previous examples) even if you use the fully qualified name for the argument:</span></span>

[!code-csharp[QualifiedNameofNotify](../../../samples/snippets/csharp/new-in-6/viewmodel.cs#QualifiedNameofNotify)]

<span data-ttu-id="727fc-306">Questa espressione `nameof` produce `FirstName`, non `UXComponents.ViewModel.FirstName`.</span><span class="sxs-lookup"><span data-stu-id="727fc-306">This `nameof` expression produces `FirstName`, not `UXComponents.ViewModel.FirstName`.</span></span>

## <a name="await-in-catch-and-finally-blocks"></a><span data-ttu-id="727fc-307">Await nei blocchi catch e finally</span><span class="sxs-lookup"><span data-stu-id="727fc-307">Await in Catch and Finally blocks</span></span>

<span data-ttu-id="727fc-308">C# 5 presentava diverse limitazioni riguardo al punto in cui posizionare le espressioni `await`.</span><span class="sxs-lookup"><span data-stu-id="727fc-308">C# 5 had several limitations around where you could place `await` expressions.</span></span>
<span data-ttu-id="727fc-309">Una di esse è stata rimossa in C# 6.</span><span class="sxs-lookup"><span data-stu-id="727fc-309">One of those has been removed in C# 6.</span></span> <span data-ttu-id="727fc-310">È ora possibile usare `await` nelle espressioni `catch` o `finally`.</span><span class="sxs-lookup"><span data-stu-id="727fc-310">You can now use `await` in `catch` or `finally` expressions.</span></span> 

<span data-ttu-id="727fc-311">Può sembrare che l'aggiunta di espressioni await nei blocchi catch e finally complichi il modo in cui i blocchi vengono elaborati.</span><span class="sxs-lookup"><span data-stu-id="727fc-311">The addition of await expressions in catch and finally blocks may appear to complicate how those are processed.</span></span> <span data-ttu-id="727fc-312">Vediamo un esempio per chiarire questo aspetto.</span><span class="sxs-lookup"><span data-stu-id="727fc-312">Let's add an example to discuss how this appears.</span></span> <span data-ttu-id="727fc-313">In qualsiasi metodo asincrono è possibile usare un'espressione await in una clausola finally.</span><span class="sxs-lookup"><span data-stu-id="727fc-313">In any async method, you can use an await expression in a finally clause.</span></span>

<span data-ttu-id="727fc-314">Con C# 6 è anche possibile usare await nelle espressioni catch.</span><span class="sxs-lookup"><span data-stu-id="727fc-314">With C# 6, you can also await in catch expressions.</span></span> <span data-ttu-id="727fc-315">Questo uso è più frequente negli scenari di registrazione:</span><span class="sxs-lookup"><span data-stu-id="727fc-315">This is most often used with logging scenarios:</span></span>

[!code-csharp[AwaitFinally](../../../samples/snippets/csharp/new-in-6/NetworkClient.cs#AwaitFinally)]

<span data-ttu-id="727fc-316">I dettagli sull'implementazione per l'aggiunta del supporto `await` all'interno delle clausole `catch` e `finally` assicura che il comportamento sia coerente con il comportamento per il codice sincrono.</span><span class="sxs-lookup"><span data-stu-id="727fc-316">The implementation details for adding `await` support inside `catch` and `finally` clauses ensures that the behavior is consistent with the behavior for synchronous code.</span></span> <span data-ttu-id="727fc-317">Quando il codice eseguito in una clausola `catch` o `finally` genera un elemento, l'esecuzione cerca una clausola `catch` appropriata nel successivo blocco circostante.</span><span class="sxs-lookup"><span data-stu-id="727fc-317">When code executed in a `catch` or `finally` clause throws, execution looks for a suitable `catch` clause in the next surrounding block.</span></span> <span data-ttu-id="727fc-318">Se si è verificata un'eccezione, tale eccezione viene persa.</span><span class="sxs-lookup"><span data-stu-id="727fc-318">If there was a current exception, that exception is lost.</span></span> <span data-ttu-id="727fc-319">Lo stesso accade con le espressioni attese nelle clausole `catch` e `finally`: viene cercato un valore `catch` appropriato e l'eccezione corrente, se presente, viene persa.</span><span class="sxs-lookup"><span data-stu-id="727fc-319">The same happens with awaited expressions in `catch` and `finally` clauses: a suitable `catch` is searched for, and the current exception, if any, is lost.</span></span>  

> [!NOTE]
> <span data-ttu-id="727fc-320">Questo comportamento è il motivo per cui è consigliabile scrivere le clausole `catch` e `finally` con attenzione, per evitare l'introduzione di nuove eccezioni.</span><span class="sxs-lookup"><span data-stu-id="727fc-320">This behavior is the reason it's recommended to write `catch` and `finally` clauses carefully, to avoid introducing new exceptions.</span></span>

## <a name="index-initializers"></a><span data-ttu-id="727fc-321">Inizializzatori di indice.</span><span class="sxs-lookup"><span data-stu-id="727fc-321">Index Initializers</span></span>

<span data-ttu-id="727fc-322">Gli *inizializzatori di indice* rappresentano una delle due funzionalità che rendono gli inizializzatori di insieme più coerenti.</span><span class="sxs-lookup"><span data-stu-id="727fc-322">*Index Initializers* is one of two features that make collection initializers more consistent.</span></span> <span data-ttu-id="727fc-323">Nelle versioni precedenti di C# gli *inizializzatori di insieme* potevano essere usati solo con le raccolte di stili di sequenza:</span><span class="sxs-lookup"><span data-stu-id="727fc-323">In earlier releases of C#, you could use *collection initializers* only with sequence style collections:</span></span>

[!code-csharp[ListInitializer](../../../samples/snippets/csharp/new-in-6/initializers.cs#ListInitializer)]

<span data-ttu-id="727fc-324">Ora è possibile usarli anche con le raccolte <xref:System.Collections.Generic.Dictionary%602> e tipi simili:</span><span class="sxs-lookup"><span data-stu-id="727fc-324">Now, you can also use them with <xref:System.Collections.Generic.Dictionary%602> collections and similar types:</span></span>

[!code-csharp[DictionaryInitializer](../../../samples/snippets/csharp/new-in-6/initializers.cs#DictionaryInitializer)]

<span data-ttu-id="727fc-325">Questa funzionalità significa che i contenitori associativi possono essere inizializzati usando una sintassi simile a ciò che è stato usato per i contenitori sequenziali in diverse versioni.</span><span class="sxs-lookup"><span data-stu-id="727fc-325">This feature means that associative containers can be initialized using syntax similar to what's been in place for sequence containers for several versions.</span></span>

### <a name="extension-add-methods-in-collection-initializers"></a><span data-ttu-id="727fc-326">Metodi di estensione `Add` negli inizializzatori di insieme</span><span class="sxs-lookup"><span data-stu-id="727fc-326">Extension `Add` methods in collection initializers</span></span>

<span data-ttu-id="727fc-327">Un'altra funzionalità che semplifica l'inizializzazione della raccolta è la possibilità di usare un *metodo di estensione* per il metodo `Add`.</span><span class="sxs-lookup"><span data-stu-id="727fc-327">Another feature that makes collection initialization easier is the ability to use an *extension method* for the `Add` method.</span></span> <span data-ttu-id="727fc-328">Questa funzionalità è stata aggiunta per la parità con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="727fc-328">This feature was added for parity with Visual Basic.</span></span> 

<span data-ttu-id="727fc-329">La funzionalità è particolarmente utile quando si usa una classe di raccolta personalizzata con un metodo di nome diverso per aggiungere semanticamente nuovi elementi.</span><span class="sxs-lookup"><span data-stu-id="727fc-329">The feature is most useful when you have a custom collection class that has a method with a different name to semantically add new items.</span></span>

<span data-ttu-id="727fc-330">Si consideri ad esempio una raccolta di studenti come questa:</span><span class="sxs-lookup"><span data-stu-id="727fc-330">For example, consider a collection of students like this:</span></span>

[!code-csharp[Enrollment](../../../samples/snippets/csharp/new-in-6/enrollment.cs#Enrollment)]

<span data-ttu-id="727fc-331">Il metodo `Enroll` aggiunge uno studente.</span><span class="sxs-lookup"><span data-stu-id="727fc-331">The `Enroll` method adds a student.</span></span> <span data-ttu-id="727fc-332">Ma non è conforme al modello `Add`.</span><span class="sxs-lookup"><span data-stu-id="727fc-332">But it doesn't follow the `Add` pattern.</span></span>
<span data-ttu-id="727fc-333">Nelle versioni precedenti di C# non era possibile usare gli inizializzatori di insieme con un oggetto `Enrollment`:</span><span class="sxs-lookup"><span data-stu-id="727fc-333">In previous versions of C#, you could not use collection initializers with an `Enrollment` object:</span></span>

[!code-csharp[InitializeEnrollment](../../../samples/snippets/csharp/new-in-6/classList.cs#InitializeEnrollment)]

<span data-ttu-id="727fc-334">Ora è possibile, ma solo se si crea un metodo di estensione che esegue il mapping di `Add` a `Enroll`:</span><span class="sxs-lookup"><span data-stu-id="727fc-334">Now you can, but only if you create an extension method that maps `Add` to `Enroll`:</span></span>

[!code-csharp[ExtensionAdd](../../../samples/snippets/csharp/new-in-6/classList.cs#ExtensionAdd)]

<span data-ttu-id="727fc-335">L'uso di questa funzionalità consente di eseguire il mapping di qualsiasi metodo che aggiunge elementi a una raccolta a un metodo denominato `Add` creando un metodo di estensione:</span><span class="sxs-lookup"><span data-stu-id="727fc-335">What you are doing with this feature is to map whatever method adds items to a collection to a method named `Add` by creating an extension method:</span></span> 

[!code-csharp[Enrollment](../../../samples/snippets/csharp/new-in-6/enrollment.cs#Enrollment)]
[!code-csharp[ExtensionAddSample](../../../samples/snippets/csharp/new-in-6/classList.cs#ExtensionAddSample)]

## <a name="improved-overload-resolution"></a><span data-ttu-id="727fc-336">Risoluzione dell'overload migliorata</span><span class="sxs-lookup"><span data-stu-id="727fc-336">Improved overload resolution</span></span>

<span data-ttu-id="727fc-337">Quest'ultima funzionalità probabilmente non viene notata.</span><span class="sxs-lookup"><span data-stu-id="727fc-337">This last feature is one you probably won't notice.</span></span> <span data-ttu-id="727fc-338">Esistevano costrutti in cui la versione precedente del compilatore C# poteva rilevare alcune chiamate al metodo che includevano espressioni lambda ambigue.</span><span class="sxs-lookup"><span data-stu-id="727fc-338">There were constructs where the previous version of the C# compiler may have found some method calls involving lambda expressions ambiguous.</span></span> <span data-ttu-id="727fc-339">Si consideri il metodo seguente:</span><span class="sxs-lookup"><span data-stu-id="727fc-339">Consider this method:</span></span>

[!code-csharp[AsyncMethod](../../../samples/snippets/csharp/new-in-6/overloads.cs#AsyncMethod)]

<span data-ttu-id="727fc-340">Nelle versioni precedenti di C# una chiamata a tale metodo usando la sintassi del gruppo di metodi avrebbe esito negativo:</span><span class="sxs-lookup"><span data-stu-id="727fc-340">In earlier versions of C#, calling that method using the method group syntax would fail:</span></span>

[!code-csharp[MethodGroup](../../../samples/snippets/csharp/new-in-6/overloads.cs#MethodGroup)]
 
<span data-ttu-id="727fc-341">Il compilatore precedente non era in grado di distinguere correttamente `Task.Run(Action)` da `Task.Run(Func<Task>())`.</span><span class="sxs-lookup"><span data-stu-id="727fc-341">The earlier compiler could not distinguish correctly between `Task.Run(Action)` and `Task.Run(Func<Task>())`.</span></span> <span data-ttu-id="727fc-342">Nelle versioni precedenti è necessario usare un'espressione lambda come argomento:</span><span class="sxs-lookup"><span data-stu-id="727fc-342">In previous versions, you'd need to use a lambda expression as an argument:</span></span>

[!code-csharp[Lambda](../../../samples/snippets/csharp/new-in-6/overloads.cs#Lambda)]

<span data-ttu-id="727fc-343">Il compilatore C# 6 determina correttamente che `Task.Run(Func<Task>())` è una scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="727fc-343">The C# 6 compiler correctly determines that `Task.Run(Func<Task>())` is a better choice.</span></span>