---
title: '&lt;rimuovere&gt; elemento per NameValueSectionHandler e DictionarySectionHandler'
ms.date: 05/01/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: article
f1_keywords: http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 8d8af7f5-26c9-4db9-bbe4-b2a4e6949568
author: guardrex
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: decf0ca5f9f743a2a2884c06777b7ee9d6d6a8ca
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="remove-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="82ebe-102">\<rimuovere > elemento per NameValueSectionHandler e DictionarySectionHandler</span><span class="sxs-lookup"><span data-stu-id="82ebe-102">\<remove> element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="82ebe-103">Rimuove un'impostazione definita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="82ebe-103">Removes a previously defined setting.</span></span>

<span data-ttu-id="82ebe-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="82ebe-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="82ebe-105">&nbsp;&nbsp;[**\<sectionName >**](~/docs/framework/configure-apps/file-schema/custom-element-2.md) </span><span class="sxs-lookup"><span data-stu-id="82ebe-105">&nbsp;&nbsp;[**\<sectionName>**](~/docs/framework/configure-apps/file-schema/custom-element-2.md) </span></span>  
<span data-ttu-id="82ebe-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<rimuovere >**</span><span class="sxs-lookup"><span data-stu-id="82ebe-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**</span></span>

## <a name="syntax"></a><span data-ttu-id="82ebe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82ebe-107">Syntax</span></span>

```xml
<add remove="key" />
```

## <a name="attribute"></a><span data-ttu-id="82ebe-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="82ebe-108">Attribute</span></span>

|           | <span data-ttu-id="82ebe-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82ebe-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="82ebe-110">**key**</span><span class="sxs-lookup"><span data-stu-id="82ebe-110">**key**</span></span>   | <span data-ttu-id="82ebe-111">Attributo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="82ebe-111">Required attribute.</span></span><br><br><span data-ttu-id="82ebe-112">Specifica il nome dell'impostazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="82ebe-112">Specifies the name of the setting to remove.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="82ebe-113">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="82ebe-113">Parent element</span></span>

| <span data-ttu-id="82ebe-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="82ebe-114">Element</span></span> | <span data-ttu-id="82ebe-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82ebe-115">Description</span></span> |
| ------- | ------------|
| [<span data-ttu-id="82ebe-116">**\<sectionName >** elemento</span><span class="sxs-lookup"><span data-stu-id="82ebe-116">**\<sectionName>** Element</span></span>](~/docs/framework/configure-apps/file-schema/custom-element-2.md) | <span data-ttu-id="82ebe-117">Definisce le impostazioni per le sezioni di configurazione personalizzate che utilizzano il <xref:System.Configuration.NameValueSectionHandler> e <xref:System.Configuration.DictionarySectionHandler> classi.</span><span class="sxs-lookup"><span data-stu-id="82ebe-117">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="82ebe-118">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="82ebe-118">Child elements</span></span>

<span data-ttu-id="82ebe-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82ebe-119">None</span></span>

## <a name="remarks"></a><span data-ttu-id="82ebe-120">Note</span><span class="sxs-lookup"><span data-stu-id="82ebe-120">Remarks</span></span>

<span data-ttu-id="82ebe-121">È possibile utilizzare il  **\<rimuovere >** elemento da rimuovere le impostazioni dall'applicazione che sono stati definiti a un livello superiore nella gerarchia di file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="82ebe-121">You can use the **\<remove>** element to remove settings from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="82ebe-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="82ebe-122">Example</span></span>

<span data-ttu-id="82ebe-123">Nell'esempio seguente viene illustrato come utilizzare il  **\<rimuovere >** elemento in un file di configurazione dell'applicazione per rimuovere le impostazioni definite in precedenza nel file di configurazione del computer.</span><span class="sxs-lookup"><span data-stu-id="82ebe-123">The following example shows how to use the **\<remove>** element in an application configuration file to remove settings previously defined in the machine configuration file.</span></span>

<span data-ttu-id="82ebe-124">Nel seguente codice di file di configurazione di computer viene dichiarata la sezione  **\<mySection >** e aggiunge due impostazioni, `key1` e `key2`, a esso:</span><span class="sxs-lookup"><span data-stu-id="82ebe-124">The following machine configuration file code declares the section **\<mySection>** and adds two settings, `key1` and `key2`, to it:</span></span>

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="mySection" type="System.Configuration.NameValueSectionHandler,System" />
  </configSections>
  <mySection>
    <add key="key1" value="value1" />
    <add key="key2" value="value2" />
  </mySection>
</configuration>
```

<span data-ttu-id="82ebe-125">Il seguente codice di file di configurazione dell'applicazione rimuove il `key2` impostazione dal  **\<mySection >**:</span><span class="sxs-lookup"><span data-stu-id="82ebe-125">The following application configuration file code removes the `key2` setting from **\<mySection>**:</span></span>

```xml
<!--Application configuration file -->
<configuration>
  <mySection>
    <remove key="key2" />
  </mySection>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="82ebe-126">File di configurazione</span><span class="sxs-lookup"><span data-stu-id="82ebe-126">Configuration file</span></span>

<span data-ttu-id="82ebe-127">Questo elemento può essere usato nel file di configurazione dell'applicazione, i file di configurazione macchina (*Machine. config*), e *Web. config* file che non sono a livello di directory dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82ebe-127">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="82ebe-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="82ebe-128">See also</span></span>

[<span data-ttu-id="82ebe-129">Schema di file di configurazione per .NET Framework</span><span class="sxs-lookup"><span data-stu-id="82ebe-129">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)