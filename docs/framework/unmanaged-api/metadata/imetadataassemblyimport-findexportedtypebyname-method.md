---
title: Metodo IMetaDataAssemblyImport::FindExportedTypeByName
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataAssemblyImport.FindExportedTypeByName
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataAssemblyImport::FindExportedTypeByName
helpviewer_keywords:
- FindExportedTypeByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindExportedTypeByName method [.NET Framework metadata]
ms.assetid: 46264b2c-574d-4dde-aafc-77187a104fdd
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: b7ef0e09cb5a44e612e545fc4ee7278c2d128174
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataassemblyimportfindexportedtypebyname-method"></a><span data-ttu-id="e0613-102">Metodo IMetaDataAssemblyImport::FindExportedTypeByName</span><span class="sxs-lookup"><span data-stu-id="e0613-102">IMetaDataAssemblyImport::FindExportedTypeByName Method</span></span>
<span data-ttu-id="e0613-103">Ottiene un puntatore a un tipo esportato, dato il nome e il tipo di inclusione.</span><span class="sxs-lookup"><span data-stu-id="e0613-103">Gets a pointer to an exported type, given its name and enclosing type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0613-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0613-104">Syntax</span></span>  
  
```  
HRESULT FindExportedTypeByName (  
    [in]  LPCWSTR           szName,   
    [in]  mdToken           mdtExportedType,   
    [out] mdExportedType    *ptkExportedType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e0613-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0613-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="e0613-106">[in] Il nome del tipo esportato.</span><span class="sxs-lookup"><span data-stu-id="e0613-106">[in] The name of the exported type.</span></span>  
  
 `mdtExportedType`  
 <span data-ttu-id="e0613-107">[in] Il token di metadati per la classe contenitore del tipo esportato.</span><span class="sxs-lookup"><span data-stu-id="e0613-107">[in] The metadata token for the enclosing class of the exported type.</span></span> <span data-ttu-id="e0613-108">Questo valore è `mdExportedTypeNil` se esportato richiesto tipo non è un tipo annidato.</span><span class="sxs-lookup"><span data-stu-id="e0613-108">This value is `mdExportedTypeNil` if the requested exported type is not a nested type.</span></span>  
  
 `ptkExportedType`  
 <span data-ttu-id="e0613-109">[out] Un puntatore al `mdExportedType` token che rappresenta il tipo esportato.</span><span class="sxs-lookup"><span data-stu-id="e0613-109">[out] A pointer to the `mdExportedType` token that represents the exported type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e0613-110">Note</span><span class="sxs-lookup"><span data-stu-id="e0613-110">Remarks</span></span>  
 <span data-ttu-id="e0613-111">Il `FindExportedTypeByName` metodo utilizza le regole standard utilizzate da common language runtime per la risoluzione dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="e0613-111">The `FindExportedTypeByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e0613-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0613-112">Requirements</span></span>  
 <span data-ttu-id="e0613-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e0613-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0613-114">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="e0613-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e0613-115">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e0613-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e0613-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e0613-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0613-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e0613-117">See Also</span></span>  
 [<span data-ttu-id="e0613-118">IMetaDataAssemblyImport (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="e0613-118">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)  
 [<span data-ttu-id="e0613-119">Come il runtime individua gli assembly</span><span class="sxs-lookup"><span data-stu-id="e0613-119">How the Runtime Locates Assemblies</span></span>](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)