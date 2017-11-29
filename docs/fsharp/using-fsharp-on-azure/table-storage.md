---
title: 'Introduzione all''archiviazione tabelle di Azure con F #'
description: Archiviare dati strutturati nel cloud tramite l'archiviazione tabelle di Azure, un archivio dati NoSQL.
keywords: "Visual f #, f #, funzionalità di programmazione, .NET, .NET Core, Azure"
author: sylvanc
ms.author: phcart
ms.date: 09/20/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 9e5d6cea-a98c-461e-a5cc-75f1d154eafd
ms.openlocfilehash: bf833a96809768011f26df35332ab2372ced2aaf
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="get-started-with-azure-table-storage-using-f"></a><span data-ttu-id="86b53-104">Introduzione all'archiviazione tabelle di Azure con F #</span><span class="sxs-lookup"><span data-stu-id="86b53-104">Get started with Azure Table storage using F#</span></span> #

<span data-ttu-id="86b53-105">Archiviazione tabelle di Azure è un servizio che archivia dati NoSQL strutturati nel cloud.</span><span class="sxs-lookup"><span data-stu-id="86b53-105">Azure Table storage is a service that stores structured NoSQL data in the cloud.</span></span> <span data-ttu-id="86b53-106">Archiviazione tabelle è un archivio o l'attributo chiave con una progettazione schemaless.</span><span class="sxs-lookup"><span data-stu-id="86b53-106">Table storage is a key/attribute store with a schemaless design.</span></span> <span data-ttu-id="86b53-107">Poiché l'archiviazione tabelle è schemaless, è facile adattare i dati come le esigenze di evolve l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-107">Because Table storage is schemaless, it's easy to adapt your data as the needs of your application evolve.</span></span> <span data-ttu-id="86b53-108">Accesso ai dati è veloce e conveniente per tutti i tipi di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="86b53-108">Access to data is fast and cost-effective for all kinds of applications.</span></span> <span data-ttu-id="86b53-109">Archiviazione tabelle è in genere notevolmente inferiore costo SQL tradizionale per i volumi di dati simili.</span><span class="sxs-lookup"><span data-stu-id="86b53-109">Table storage is typically significantly lower in cost than traditional SQL for similar volumes of data.</span></span>

<span data-ttu-id="86b53-110">È possibile utilizzare l'archiviazione tabelle per archiviare i set di dati flessibile, ad esempio i dati utente per applicazioni web, rubriche, informazioni sul dispositivo e qualsiasi altro tipo di metadati che richiede il servizio.</span><span class="sxs-lookup"><span data-stu-id="86b53-110">You can use Table storage to store flexible datasets, such as user data for web applications, address books, device information, and any other type of metadata that your service requires.</span></span> <span data-ttu-id="86b53-111">È possibile archiviare qualsiasi numero di entità in una tabella e un account di archiviazione può contenere qualsiasi numero di tabelle, fino al limite di capacità dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-111">You can store any number of entities in a table, and a storage account may contain any number of tables, up to the capacity limit of the storage account.</span></span>

### <a name="about-this-tutorial"></a><span data-ttu-id="86b53-112">Su questa esercitazione</span><span class="sxs-lookup"><span data-stu-id="86b53-112">About this tutorial</span></span>

<span data-ttu-id="86b53-113">In questa esercitazione viene illustrato come scrivere codice F # per eseguire alcune attività comuni utilizzando l'archiviazione tabelle di Azure, inclusa la creazione e l'eliminazione di una tabella e inserimento, aggiornamento, eliminazione e query sui dati di tabella.</span><span class="sxs-lookup"><span data-stu-id="86b53-113">This tutorial shows how to write F# code to do some common tasks using Azure Table storage, including creating and deleting a table and inserting, updating, deleting, and querying table data.</span></span>

<span data-ttu-id="86b53-114">Per una panoramica concettuale dell'archiviazione tabelle, vedere [la Guida di .NET per l'archiviazione tabelle](/azure/storage/storage-dotnet-how-to-use-tables)</span><span class="sxs-lookup"><span data-stu-id="86b53-114">For a conceptual overview of table storage, please see [the .NET guide for table storage](/azure/storage/storage-dotnet-how-to-use-tables)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86b53-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="86b53-115">Prerequisites</span></span>

<span data-ttu-id="86b53-116">Per usare questa Guida, è innanzitutto necessario [creare un account di archiviazione di Azure](/azure/storage/storage-create-storage-account).</span><span class="sxs-lookup"><span data-stu-id="86b53-116">To use this guide, you must first [create an Azure storage account](/azure/storage/storage-create-storage-account).</span></span>
<span data-ttu-id="86b53-117">Per questo account, è necessario anche la chiave di accesso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-117">You'll also need your storage access key for this account.</span></span>

## <a name="create-an-f-script-and-start-f-interactive"></a><span data-ttu-id="86b53-118">Creare un Script F # e avvio di F # Interactive</span><span class="sxs-lookup"><span data-stu-id="86b53-118">Create an F# Script and Start F# Interactive</span></span>

<span data-ttu-id="86b53-119">Gli esempi in questo articolo è utilizzabile in un'applicazione di F # o uno script F #.</span><span class="sxs-lookup"><span data-stu-id="86b53-119">The samples in this article can be used in either an F# application or an F# script.</span></span> <span data-ttu-id="86b53-120">Per creare uno script F #, creare un file con il `.fsx` estensione, ad esempio `tables.fsx`, nell'ambiente di sviluppo F #.</span><span class="sxs-lookup"><span data-stu-id="86b53-120">To create an F# script, create a file with the `.fsx` extension, for example `tables.fsx`, in your F# development environment.</span></span>

<span data-ttu-id="86b53-121">Successivamente, utilizzare un [Gestione pacchetti](package-management.md) , ad esempio [Paket](https://fsprojects.github.io/Paket/) o [NuGet](https://www.nuget.org/) per installare il `WindowsAzure.Storage` pacchetto e riferimento `WindowsAzure.Storage.dll` nello script utilizzando un `#r`direttiva.</span><span class="sxs-lookup"><span data-stu-id="86b53-121">Next, use a [package manager](package-management.md) such as [Paket](https://fsprojects.github.io/Paket/) or [NuGet](https://www.nuget.org/) to install the `WindowsAzure.Storage` package and reference `WindowsAzure.Storage.dll` in your script using a `#r` directive.</span></span> <span data-ttu-id="86b53-122">Eseguire nuovamente per 'Microsoft.WindowsAzure.ConfigurationManager' per ottenere lo spazio dei nomi Microsoft.Azure.</span><span class="sxs-lookup"><span data-stu-id="86b53-122">Do it again for \`Microsoft.WindowsAzure.ConfigurationManager' in order to get the Microsoft.Azure namespace.</span></span>

### <a name="add-namespace-declarations"></a><span data-ttu-id="86b53-123">Aggiungere le dichiarazioni dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="86b53-123">Add namespace declarations</span></span>

<span data-ttu-id="86b53-124">Aggiungere il seguente `open` istruzioni all'inizio di `tables.fsx` file:</span><span class="sxs-lookup"><span data-stu-id="86b53-124">Add the following `open` statements to the top of the `tables.fsx` file:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L1-L5)]

### <a name="get-your-connection-string"></a><span data-ttu-id="86b53-125">Ottenere la stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="86b53-125">Get your connection string</span></span>

<span data-ttu-id="86b53-126">Una stringa di connessione di archiviazione di Azure è necessario per questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-126">You'll need an Azure Storage connection string for this tutorial.</span></span> <span data-ttu-id="86b53-127">Per ulteriori informazioni sulle stringhe di connessione, vedere [configurare stringhe di connessione di archiviazione](/azure/storage/storage-configure-connection-string).</span><span class="sxs-lookup"><span data-stu-id="86b53-127">For more information about connection strings, see [Configure Storage Connection Strings](/azure/storage/storage-configure-connection-string).</span></span>

<span data-ttu-id="86b53-128">Per l'esercitazione, si immetteranno la stringa di connessione nello script, simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="86b53-128">For the tutorial, you'll enter your connection string in your script, like this:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L11-L11)]

<span data-ttu-id="86b53-129">Si tratta tuttavia **non è consigliabile** di progetti.</span><span class="sxs-lookup"><span data-stu-id="86b53-129">However, this is **not recommended** for real projects.</span></span> <span data-ttu-id="86b53-130">La chiave di account di archiviazione è simile a quella radice per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-130">Your storage account key is similar to the root password for your storage account.</span></span> <span data-ttu-id="86b53-131">Prestare sempre attenzione proteggere la chiave di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-131">Always be careful to protect your storage account key.</span></span> <span data-ttu-id="86b53-132">Evitare di distribuirlo ad altri utenti, a livello di codice, o il salvataggio in un file di testo che è accessibile ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="86b53-132">Avoid distributing it to other users, hard-coding it, or saving it in a plain-text file that is accessible to others.</span></span> <span data-ttu-id="86b53-133">È possibile rigenerare la chiave tramite il portale di Azure, se si ritiene che potrebbero essere state compromesse.</span><span class="sxs-lookup"><span data-stu-id="86b53-133">You can regenerate your key using the Azure Portal if you believe it may have been compromised.</span></span>

<span data-ttu-id="86b53-134">In applicazioni reali, il modo migliore per gestire la stringa di connessione di archiviazione è in un file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-134">For real applications, the best way to maintain your storage connection string is in a configuration file.</span></span> <span data-ttu-id="86b53-135">Per recuperare la stringa di connessione da un file di configurazione, è possibile farlo:</span><span class="sxs-lookup"><span data-stu-id="86b53-135">To fetch the connection string from a configuration file, you can do this:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L13-L15)]

<span data-ttu-id="86b53-136">Utilizzando Gestione configurazione di Azure è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="86b53-136">Using Azure Configuration Manager is optional.</span></span> <span data-ttu-id="86b53-137">È inoltre possibile utilizzare un'API, ad esempio di .NET Framework `ConfigurationManager` tipo.</span><span class="sxs-lookup"><span data-stu-id="86b53-137">You can also use an API such as the .NET Framework's `ConfigurationManager` type.</span></span>

### <a name="parse-the-connection-string"></a><span data-ttu-id="86b53-138">Analizzare la stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="86b53-138">Parse the connection string</span></span>

<span data-ttu-id="86b53-139">Per analizzare la stringa di connessione, utilizzare:</span><span class="sxs-lookup"><span data-stu-id="86b53-139">To parse the connection string, use:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L21-L22)]

<span data-ttu-id="86b53-140">Verrà restituito un `CloudStorageAccount`.</span><span class="sxs-lookup"><span data-stu-id="86b53-140">This will return a `CloudStorageAccount`.</span></span>

### <a name="create-the-table-service-client"></a><span data-ttu-id="86b53-141">Creare il client del servizio tabelle</span><span class="sxs-lookup"><span data-stu-id="86b53-141">Create the Table service client</span></span>

<span data-ttu-id="86b53-142">La `CloudTableClient` classe consente di recuperare tabelle ed entità archiviate nell'archiviazione tabelle.</span><span class="sxs-lookup"><span data-stu-id="86b53-142">The `CloudTableClient` class enables you to retrieve tables and entities stored in Table storage.</span></span> <span data-ttu-id="86b53-143">Ecco un modo per creare il client del servizio:</span><span class="sxs-lookup"><span data-stu-id="86b53-143">Here's one way to create the service client:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L28-L29)]

<span data-ttu-id="86b53-144">A questo punto si è pronti a scrivere codice che legge i dati da e scrive i dati in archiviazione tabelle.</span><span class="sxs-lookup"><span data-stu-id="86b53-144">Now you are ready to write code that reads data from and writes data to Table storage.</span></span>

## <a name="create-a-table"></a><span data-ttu-id="86b53-145">Creare una tabella</span><span class="sxs-lookup"><span data-stu-id="86b53-145">Create a table</span></span>

<span data-ttu-id="86b53-146">In questo esempio viene illustrato come creare una tabella se non esiste già:</span><span class="sxs-lookup"><span data-stu-id="86b53-146">This example shows how to create a table if it does not already exist:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L35-L39)]

## <a name="add-an-entity-to-a-table"></a><span data-ttu-id="86b53-147">Aggiungere un'entità a una tabella</span><span class="sxs-lookup"><span data-stu-id="86b53-147">Add an entity to a table</span></span>

<span data-ttu-id="86b53-148">Un'entità deve disporre di un tipo che eredita da `TableEntity`.</span><span class="sxs-lookup"><span data-stu-id="86b53-148">An entity has to have a type that inherits from `TableEntity`.</span></span> <span data-ttu-id="86b53-149">È possibile estendere `TableEntity` nel modo desiderato, ma il tipo di *deve* dispone di un costruttore senza parametri.</span><span class="sxs-lookup"><span data-stu-id="86b53-149">You can extend `TableEntity` in any way you like, but your type *must* have a parameter-less constructor.</span></span> <span data-ttu-id="86b53-150">Solo le proprietà che hanno entrambi `get` e `set` verranno archiviati nella tabella di Azure.</span><span class="sxs-lookup"><span data-stu-id="86b53-150">Only properties that have both `get` and `set` will be stored in your Azure Table.</span></span>

<span data-ttu-id="86b53-151">Chiave di riga e di partizione dell'entità è necessario identificare in modo univoco l'entità nella tabella.</span><span class="sxs-lookup"><span data-stu-id="86b53-151">An entity's partition and row key uniquely identify the entity in the table.</span></span> <span data-ttu-id="86b53-152">Le entità con la stessa chiave di partizione è possibile eseguire query più velocemente rispetto a quelle con le chiavi di partizione diverso, ma con le chiavi di partizione diverse consente una maggiore scalabilità di operazioni parallele.</span><span class="sxs-lookup"><span data-stu-id="86b53-152">Entities with the same partition key can be queried faster than those with different partition keys, but using diverse partition keys allows for greater scalability of parallel operations.</span></span>

<span data-ttu-id="86b53-153">Di seguito è riportato un esempio di un `Customer` che utilizza il `lastName` come chiave di partizione e `firstName` come chiave di riga.</span><span class="sxs-lookup"><span data-stu-id="86b53-153">Here's an example of a `Customer` that uses the `lastName` as the partition key and the `firstName` as the row key.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L45-L52)]

<span data-ttu-id="86b53-154">Ora verrà aggiunto il nostro `Customer` alla tabella.</span><span class="sxs-lookup"><span data-stu-id="86b53-154">Now we'll add our `Customer` to the table.</span></span> <span data-ttu-id="86b53-155">A tale scopo, si crea un `TableOperation` che verrà eseguita sulla tabella.</span><span class="sxs-lookup"><span data-stu-id="86b53-155">To do so, you create a `TableOperation` that will execute on the table.</span></span> <span data-ttu-id="86b53-156">In questo caso, si crea un `Insert` operazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-156">In this case, you create an `Insert` operation.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L54-L55)]

## <a name="insert-a-batch-of-entities"></a><span data-ttu-id="86b53-157">Inserire un batch di entità</span><span class="sxs-lookup"><span data-stu-id="86b53-157">Insert a batch of entities</span></span>

<span data-ttu-id="86b53-158">È possibile inserire un batch di entità in una tabella utilizzando una sola operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="86b53-158">You can insert a batch of entities into a table using a single write operation.</span></span> <span data-ttu-id="86b53-159">Operazioni batch consentono di combinare operazioni in una singola esecuzione, ma presentano alcune restrizioni:</span><span class="sxs-lookup"><span data-stu-id="86b53-159">Batch operations allow you to combine operations into a single execution, but they have some restrictions:</span></span>

- <span data-ttu-id="86b53-160">È possibile eseguire aggiornamenti, Elimina e lo inserisce nella stessa operazione batch.</span><span class="sxs-lookup"><span data-stu-id="86b53-160">You can perform updates, deletes, and inserts in the same batch operation.</span></span>
- <span data-ttu-id="86b53-161">Un'operazione batch può includere fino a 100 entità.</span><span class="sxs-lookup"><span data-stu-id="86b53-161">A batch operation can include up to 100 entities.</span></span>
- <span data-ttu-id="86b53-162">Tutte le entità in un'operazione batch devono avere la stessa chiave di partizione.</span><span class="sxs-lookup"><span data-stu-id="86b53-162">All entities in a batch operation must have the same partition key.</span></span>
- <span data-ttu-id="86b53-163">Sebbene sia possibile eseguire una query in un'operazione batch, deve essere l'unica operazione nel batch.</span><span class="sxs-lookup"><span data-stu-id="86b53-163">While it is possible to perform a query in a batch operation, it must be the only operation in the batch.</span></span>

<span data-ttu-id="86b53-164">Ecco alcuni codice che combina due istruzioni INSERT in un'operazione batch:</span><span class="sxs-lookup"><span data-stu-id="86b53-164">Here's some code that combines two inserts into a batch operation:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L62-L71)]

## <a name="retrieve-all-entities-in-a-partition"></a><span data-ttu-id="86b53-165">Recuperare tutte le entità in una partizione</span><span class="sxs-lookup"><span data-stu-id="86b53-165">Retrieve all entities in a partition</span></span>

<span data-ttu-id="86b53-166">Per una query sulla tabella per tutte le entità in una partizione, utilizzare un `TableQuery` oggetto.</span><span class="sxs-lookup"><span data-stu-id="86b53-166">To query a table for all entities in a partition, use a `TableQuery` object.</span></span> <span data-ttu-id="86b53-167">In questo caso, è applicare un filtro per le entità in cui "Buster" è la chiave di partizione.</span><span class="sxs-lookup"><span data-stu-id="86b53-167">Here, you filter for entities where "Buster" is the partition key.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L77-L80)]

<span data-ttu-id="86b53-168">È ora possibile stampare i risultati:</span><span class="sxs-lookup"><span data-stu-id="86b53-168">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L84-L85)]


## <a name="retrieve-a-range-of-entities-in-a-partition"></a><span data-ttu-id="86b53-169">Recuperare un intervallo di entità in una partizione</span><span class="sxs-lookup"><span data-stu-id="86b53-169">Retrieve a range of entities in a partition</span></span>

<span data-ttu-id="86b53-170">Se non si desidera eseguire una query di tutte le entità in una partizione, è possibile specificare un intervallo combinando il filtro di chiave di partizione con un filtro di riga di chiave.</span><span class="sxs-lookup"><span data-stu-id="86b53-170">If you don't want to query all the entities in a partition, you can specify a range by combining the partition key filter with a row key filter.</span></span> <span data-ttu-id="86b53-171">In questo caso, utilizzare due filtri per ottenere tutte le entità nella partizione "Buster" in cui la chiave di riga (nome) inizia con una lettera precedente a "M" nell'alfabeto.</span><span class="sxs-lookup"><span data-stu-id="86b53-171">Here, you use two filters to get all entities in the "Buster" partition where the row key (first name) starts with a letter earlier than "M" in the alphabet.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L91-L100)]

<span data-ttu-id="86b53-172">È ora possibile stampare i risultati:</span><span class="sxs-lookup"><span data-stu-id="86b53-172">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L102-L103)]

## <a name="retrieve-a-single-entity"></a><span data-ttu-id="86b53-173">Recuperare una singola entità</span><span class="sxs-lookup"><span data-stu-id="86b53-173">Retrieve a single entity</span></span>

<span data-ttu-id="86b53-174">È possibile scrivere una query per recuperare un'entità singola e specifica.</span><span class="sxs-lookup"><span data-stu-id="86b53-174">You can write a query to retrieve a single, specific entity.</span></span> <span data-ttu-id="86b53-175">In questo caso, si utilizza un `TableOperation` per specificare il cliente "Larry Buster".</span><span class="sxs-lookup"><span data-stu-id="86b53-175">Here, you use a `TableOperation` to specify the customer "Larry Buster".</span></span> <span data-ttu-id="86b53-176">Invece di una raccolta, verrà restituito un `Customer`.</span><span class="sxs-lookup"><span data-stu-id="86b53-176">Instead of a collection, you get back a `Customer`.</span></span> <span data-ttu-id="86b53-177">Specifica la chiave di partizione sia la chiave di riga in una query è il modo più rapido per recuperare una singola entità dal servizio tabelle.</span><span class="sxs-lookup"><span data-stu-id="86b53-177">Specifying both the partition key and the row key in a query is the fastest way to retrieve a single entity from the Table service.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L109-L111)]

<span data-ttu-id="86b53-178">È ora possibile stampare i risultati:</span><span class="sxs-lookup"><span data-stu-id="86b53-178">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L113-L115)]


## <a name="replace-an-entity"></a><span data-ttu-id="86b53-179">Sostituire un'entità</span><span class="sxs-lookup"><span data-stu-id="86b53-179">Replace an entity</span></span>

<span data-ttu-id="86b53-180">Per aggiornare un'entità, recuperarlo dal servizio tabelle, modificare l'oggetto entità e quindi salvare le modifiche al servizio tabella utilizzando un `Replace` operazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-180">To update an entity, retrieve it from the Table service, modify the entity object, and then save the changes back to the Table service using a `Replace` operation.</span></span> <span data-ttu-id="86b53-181">In questo modo l'entità da sostituire completamente nel server, a meno che l'entità nel server è stato modificato dopo che è stata recuperata, nel qual caso l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="86b53-181">This causes the entity to be fully replaced on the server, unless the entity on the server has changed since it was retrieved, in which case the operation will fail.</span></span> <span data-ttu-id="86b53-182">Questo errore consiste nell'impedire all'applicazione inavvertitamente sovrascrivendo le modifiche apportate da altre origini.</span><span class="sxs-lookup"><span data-stu-id="86b53-182">This failure is to prevent your application from inadvertently overwriting changes from other sources.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L121-L128)]

## <a name="insert-or-replace-an-entity"></a><span data-ttu-id="86b53-183">Inserire o sostituire un'entità</span><span class="sxs-lookup"><span data-stu-id="86b53-183">Insert-or-replace an entity</span></span>

<span data-ttu-id="86b53-184">In alcuni casi, è possibile capire se l'entità esiste nella tabella o non.</span><span class="sxs-lookup"><span data-stu-id="86b53-184">Sometimes, you don't know if the entity exists in the table or not.</span></span> <span data-ttu-id="86b53-185">E in tal caso, i valori correnti archiviati in essa contenuti non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="86b53-185">And if it does, the current values stored in it are no longer needed.</span></span> <span data-ttu-id="86b53-186">È possibile utilizzare `InsertOrReplace` per creare l'entità o sostituirlo se esiste, indipendentemente dal suo stato.</span><span class="sxs-lookup"><span data-stu-id="86b53-186">You can use `InsertOrReplace` to create the entity, or replace it if it exists, regardless of its state.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L134-L140)]

## <a name="query-a-subset-of-entity-properties"></a><span data-ttu-id="86b53-187">Query a un subset di proprietà dell'entità</span><span class="sxs-lookup"><span data-stu-id="86b53-187">Query a subset of entity properties</span></span>

<span data-ttu-id="86b53-188">Una query di tabella è possibile recuperare solo alcune proprietà di un'entità anziché tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="86b53-188">A table query can retrieve just a few properties from an entity instead of all of them.</span></span> <span data-ttu-id="86b53-189">Questa tecnica, denominata proiezione, è possibile migliorare le prestazioni delle query, in particolare per le entità di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="86b53-189">This technique, called projection, can improve query performance, especially for large entities.</span></span> <span data-ttu-id="86b53-190">In questo caso, si restituiscono gli indirizzi e-mail solo `DynamicTableEntity` e `EntityResolver`.</span><span class="sxs-lookup"><span data-stu-id="86b53-190">Here, you return only email addresses using `DynamicTableEntity` and `EntityResolver`.</span></span> <span data-ttu-id="86b53-191">Si noti che proiezione non è supportata nell'emulatore di archiviazione locale, pertanto questo codice viene eseguito solo quando si utilizza un account del servizio di tabella.</span><span class="sxs-lookup"><span data-stu-id="86b53-191">Note that projection is not supported on the local storage emulator, so this code runs only when you're using an account on the Table service.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L146-L157)]

## <a name="retrieve-entities-in-pages-asynchronously"></a><span data-ttu-id="86b53-192">Recuperare le entità in pagine in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="86b53-192">Retrieve entities in pages asynchronously</span></span>

<span data-ttu-id="86b53-193">Se si legge un numero elevato di entità e si desidera elaborarle quando vengono recuperate anziché attenderne tutte restituito, è possibile utilizzare una query segmentata.</span><span class="sxs-lookup"><span data-stu-id="86b53-193">If you are reading a large number of entities, and you want to process them as they are retrieved rather than waiting for them all to return, you can use a segmented query.</span></span> <span data-ttu-id="86b53-194">In questo caso, per restituire risultati nelle pagine utilizzando un flusso di lavoro asincroni in modo che non l'esecuzione viene bloccata durante l'attesa per un ampio set di risultati da restituire.</span><span class="sxs-lookup"><span data-stu-id="86b53-194">Here, you return results in pages by using an async workflow so that execution is not blocked while you're waiting for a large set of results to return.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L163-L177)]

<span data-ttu-id="86b53-195">È ora eseguire il calcolo in modo sincrono:</span><span class="sxs-lookup"><span data-stu-id="86b53-195">You now execute this computation synchronously:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L179-L179)]

## <a name="delete-an-entity"></a><span data-ttu-id="86b53-196">Eliminare un'entità</span><span class="sxs-lookup"><span data-stu-id="86b53-196">Delete an entity</span></span>

<span data-ttu-id="86b53-197">Dopo avere recuperato, è possibile eliminare un'entità.</span><span class="sxs-lookup"><span data-stu-id="86b53-197">You can delete an entity after you have retrieved it.</span></span> <span data-ttu-id="86b53-198">Come con l'aggiornamento di un'entità, l'operazione non riuscirà se l'entità è stata modificata dopo che è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="86b53-198">As with updating an entity, this will fail if the entity has changed since you retrieved it.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L185-L186)]

## <a name="delete-a-table"></a><span data-ttu-id="86b53-199">Eliminare una tabella</span><span class="sxs-lookup"><span data-stu-id="86b53-199">Delete a table</span></span>

<span data-ttu-id="86b53-200">È possibile eliminare una tabella da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-200">You can delete a table from a storage account.</span></span> <span data-ttu-id="86b53-201">Una tabella in cui è stata eliminata non sarà disponibile per essere ricreati per un periodo di tempo in seguito all'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="86b53-201">A table that has been deleted will be unavailable to be re-created for a period of time following the deletion.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L192-L192)]

## <a name="next-steps"></a><span data-ttu-id="86b53-202">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="86b53-202">Next steps</span></span>

<span data-ttu-id="86b53-203">Ora che si è appreso le nozioni di base dell'archiviazione tabelle, vedere i collegamenti seguenti per informazioni sulle attività più complesse di archiviazione:</span><span class="sxs-lookup"><span data-stu-id="86b53-203">Now that you've learned the basics of Table storage, follow these links to learn about more complex storage tasks:</span></span>

- [<span data-ttu-id="86b53-204">Libreria Client di archiviazione per il riferimento di .NET</span><span class="sxs-lookup"><span data-stu-id="86b53-204">Storage Client Library for .NET reference</span></span>](http://go.microsoft.com/fwlink/?LinkID=390731&clcid=0x409)
- [<span data-ttu-id="86b53-205">Provider di tipi di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="86b53-205">Azure Storage Type Provider</span></span>](http://fsprojects.github.io/AzureStorageTypeProvider/)
- [<span data-ttu-id="86b53-206">Blog del Team di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="86b53-206">Azure Storage Team Blog</span></span>](http://blogs.msdn.com/b/windowsazurestorage/)
- [<span data-ttu-id="86b53-207">Configurazione delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="86b53-207">Configuring Connection Strings</span></span>](http://msdn.microsoft.com/library/azure/ee758697.aspx)
- [<span data-ttu-id="86b53-208">Introduzione all'archiviazione tabelle di Azure in .NET</span><span class="sxs-lookup"><span data-stu-id="86b53-208">Getting Started with Azure Table Storage in .NET</span></span>](https://azure.microsoft.com/documentation/samples/storage-table-dotnet-getting-started/)