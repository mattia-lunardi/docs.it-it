---
title: Metodo IMetaDataImport::GetUserString
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetUserString
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetUserString
helpviewer_keywords:
- IMetaDataImport::GetUserString method [.NET Framework metadata]
- GetUserString method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 0fd3bb47-58b5-4083-b241-b9719df7a285
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 340d5cdfcb218f74a43ed6e88f5175a1d215a1b9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportgetuserstring-method"></a><span data-ttu-id="afa03-102">Metodo IMetaDataImport::GetUserString</span><span class="sxs-lookup"><span data-stu-id="afa03-102">IMetaDataImport::GetUserString Method</span></span>
<span data-ttu-id="afa03-103">Ottiene la stringa letterale rappresentata dal token di metadati specificato.</span><span class="sxs-lookup"><span data-stu-id="afa03-103">Gets the literal string represented by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="afa03-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afa03-104">Syntax</span></span>  
  
```  
HRESULT GetUserString (  
   [in]   mdString    stk,  
   [out]  LPWSTR      szString,  
   [in]   ULONG       cchString,  
   [out]  ULONG       *pchString  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="afa03-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="afa03-105">Parameters</span></span>  
 `stk`  
 <span data-ttu-id="afa03-106">[in] Il token di stringa per restituire la stringa associata.</span><span class="sxs-lookup"><span data-stu-id="afa03-106">[in] The String token to return the associated string for.</span></span>  
  
 `szString`  
 <span data-ttu-id="afa03-107">[out] Una copia della stringa di richiesta.</span><span class="sxs-lookup"><span data-stu-id="afa03-107">[out] A copy of the requested string.</span></span>  
  
 `cchString`  
 <span data-ttu-id="afa03-108">[in] La dimensione massima in caratteri wide richiesti `szString`.</span><span class="sxs-lookup"><span data-stu-id="afa03-108">[in] The maximum size in wide characters of the requested `szString`.</span></span>  
  
 `pchString`  
 <span data-ttu-id="afa03-109">[out] La dimensione in caratteri "wide" dell'oggetto restituito `szString`.</span><span class="sxs-lookup"><span data-stu-id="afa03-109">[out] The size in wide characters of the returned `szString`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="afa03-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afa03-110">Requirements</span></span>  
 <span data-ttu-id="afa03-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="afa03-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="afa03-112">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="afa03-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="afa03-113">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="afa03-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="afa03-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="afa03-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afa03-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="afa03-115">See Also</span></span>  
 [<span data-ttu-id="afa03-116">IMetaDataImport (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="afa03-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="afa03-117">IMetaDataImport2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="afa03-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)