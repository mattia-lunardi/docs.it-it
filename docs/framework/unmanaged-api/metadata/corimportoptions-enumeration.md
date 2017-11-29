---
title: Enumerazione CorImportOptions
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorImportOptions
api_location: mscoree.dll
api_type: COM
f1_keywords: CorImportOptions
helpviewer_keywords: CorImportOptions enumeration [.NET Framework metadata]
ms.assetid: 4e5d03cb-97c9-4ff4-8dbd-17d94ee374d3
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 3e014443945574cff2733e5bc5d992691acc3fd9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corimportoptions-enumeration"></a><span data-ttu-id="0b0e3-102">Enumerazione CorImportOptions</span><span class="sxs-lookup"><span data-stu-id="0b0e3-102">CorImportOptions Enumeration</span></span>
<span data-ttu-id="0b0e3-103">Contiene valori di flag che controllano il comportamento durante l'importazione di un assembly esterno all'ambito corrente.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-103">Contains flag values that control the behavior during importation of an assembly outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b0e3-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b0e3-104">Syntax</span></span>  
  
```  
typedef enum CorImportOptions {  
  
    MDImportOptionDefault                = 0x00000000,  
    MDImportOptionAll                    = 0xFFFFFFFF,  
    MDImportOptionAllTypeDefs            = 0x00000001,  
    MDImportOptionAllMethodDefs          = 0x00000002,  
    MDImportOptionAllFieldDefs           = 0x00000004,  
    MDImportOptionAllProperties          = 0x00000008,  
    MDImportOptionAllEvents              = 0x00000010,  
    MDImportOptionAllCustomAttributes    = 0x00000020,  
    MDImportOptionAllExportedTypes       = 0x00000040  
  
} CorImportOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="0b0e3-105">Membri</span><span class="sxs-lookup"><span data-stu-id="0b0e3-105">Members</span></span>  
  
|<span data-ttu-id="0b0e3-106">Membro</span><span class="sxs-lookup"><span data-stu-id="0b0e3-106">Member</span></span>|<span data-ttu-id="0b0e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b0e3-107">Description</span></span>|  
|------------|-----------------|  
|`MDImportOptionDefault`|<span data-ttu-id="0b0e3-108">Indica il comportamento predefinito, ovvero ignorare i record eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-108">Indicates the default behavior, which is to skip deleted records.</span></span>|  
|`MDImportOptionAll`|<span data-ttu-id="0b0e3-109">Indica che tutti i metadati devono essere enumerati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-109">Indicates that all metadata should be enumerated.</span></span>|  
|`MDImportOptionAllTypeDefs`|<span data-ttu-id="0b0e3-110">Indica che devono essere enumerati tutti i typedef, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-110">Indicates that all TypeDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllMethodDefs`|<span data-ttu-id="0b0e3-111">Indica che devono essere enumerati tutti gli oggetti MethodDef, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-111">Indicates that all MethodDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllFieldDefs`|<span data-ttu-id="0b0e3-112">Indica che devono essere enumerati tutti gli oggetti FieldDef, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-112">Indicates that all FieldDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllProperties`|<span data-ttu-id="0b0e3-113">Indica che devono essere enumerati tutti gli oggetti PropertyDef, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-113">Indicates that all PropertyDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllEvents`|<span data-ttu-id="0b0e3-114">Indica che devono essere enumerati tutti gli oggetti EventDef, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-114">Indicates that all EventDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllCustomAttributes`|<span data-ttu-id="0b0e3-115">Indica che devono essere enumerati tutti gli attributi personalizzati, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-115">Indicates that all custom attributes, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllExportedTypes`|<span data-ttu-id="0b0e3-116">Indica che devono essere enumerati tutti i tipi esportati, inclusi quelli eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b0e3-116">Indicates that all exported types, including deleted ones, should be enumerated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0b0e3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b0e3-117">Requirements</span></span>  
 <span data-ttu-id="0b0e3-118">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0b0e3-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b0e3-119">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="0b0e3-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="0b0e3-120">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b0e3-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b0e3-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0b0e3-121">See Also</span></span>  
 [<span data-ttu-id="0b0e3-122">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="0b0e3-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)