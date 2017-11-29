---
title: Metodo IMetaDataImport::GetTypeDefProps
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetTypeDefProps
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetTypeDefProps
helpviewer_keywords:
- GetTypeDefProps method [.NET Framework metadata]
- IMetaDataImport::GetTypeDefProps method [.NET Framework metadata]
ms.assetid: 00061a25-ba05-47a7-b984-fd916b06b149
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 1025ffde2bd066c81c4c562c0dd86e829fc2aef3
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportgettypedefprops-method"></a><span data-ttu-id="a6d78-102">Metodo IMetaDataImport::GetTypeDefProps</span><span class="sxs-lookup"><span data-stu-id="a6d78-102">IMetaDataImport::GetTypeDefProps Method</span></span>
<span data-ttu-id="a6d78-103">Restituisce informazioni sui metadati per il <xref:System.Type> rappresentato dal token TypeDef specificato.</span><span class="sxs-lookup"><span data-stu-id="a6d78-103">Returns metadata information for the <xref:System.Type> represented by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6d78-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6d78-104">Syntax</span></span>  
  
```  
HRESULT GetTypeDefProps (  
   [in]  mdTypeDef   td,  
   [out] LPWSTR      szTypeDef,  
   [in]  ULONG       cchTypeDef,  
   [out] ULONG       *pchTypeDef,  
   [out] DWORD       *pdwTypeDefFlags,  
   [out] mdToken     *ptkExtends  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a6d78-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6d78-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="a6d78-106">[in] Il token TypeDef che rappresenta il tipo da restituire i metadati.</span><span class="sxs-lookup"><span data-stu-id="a6d78-106">[in] The TypeDef token that represents the type to return metadata for.</span></span>  
  
 `szTypeDef`  
 <span data-ttu-id="a6d78-107">[out] Un buffer contenente il nome del tipo.</span><span class="sxs-lookup"><span data-stu-id="a6d78-107">[out] A buffer containing the type name.</span></span>  
  
 `cchTypeDef`  
 <span data-ttu-id="a6d78-108">[in] La dimensione in caratteri "wide" di `szTypeDef`.</span><span class="sxs-lookup"><span data-stu-id="a6d78-108">[in] The size in wide characters of `szTypeDef`.</span></span>  
  
 `pchTypeDef`  
 <span data-ttu-id="a6d78-109">[out] Il numero di caratteri "wide" restituiti in `szTypeDef`.</span><span class="sxs-lookup"><span data-stu-id="a6d78-109">[out] The number of wide characters returned in `szTypeDef`.</span></span>  
  
 `pdwTypeDefFlags`  
 <span data-ttu-id="a6d78-110">[out] Puntatore a qualsiasi flag che modificano la definizione del tipo.</span><span class="sxs-lookup"><span data-stu-id="a6d78-110">[out] A pointer to any flags that modify the type definition.</span></span> <span data-ttu-id="a6d78-111">Questo valore è una maschera di bit di [CorTypeAttr](../../../../docs/framework/unmanaged-api/metadata/cortypeattr-enumeration.md) enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a6d78-111">This value is a bitmask from the [CorTypeAttr](../../../../docs/framework/unmanaged-api/metadata/cortypeattr-enumeration.md) enumeration.</span></span>  
  
 `ptkExtends`  
 <span data-ttu-id="a6d78-112">[out] Token di metadati TypeDef o TypeRef che rappresenta il tipo di base del tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="a6d78-112">[out] A TypeDef or TypeRef metadata token that represents the base type of the requested type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6d78-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6d78-113">Requirements</span></span>  
 <span data-ttu-id="a6d78-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a6d78-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6d78-115">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="a6d78-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a6d78-116">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a6d78-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a6d78-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6d78-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6d78-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a6d78-118">See Also</span></span>  
 [<span data-ttu-id="a6d78-119">IMetaDataImport (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="a6d78-119">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="a6d78-120">IMetaDataImport2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="a6d78-120">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)