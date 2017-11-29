---
title: Metodo IMetaDataEmit::DefineProperty
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DefineProperty
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: fc0403fd51f028510eb60d93ff96fc7d05606366
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitdefineproperty-method"></a><span data-ttu-id="e506b-102">Metodo IMetaDataEmit::DefineProperty</span><span class="sxs-lookup"><span data-stu-id="e506b-102">IMetaDataEmit::DefineProperty Method</span></span>
<span data-ttu-id="e506b-103">Crea una definizione di proprietà per il tipo specificato, con l'oggetto specificato `get` e `set` funzioni di accesso, metodo e ottiene un token per tale definizione.</span><span class="sxs-lookup"><span data-stu-id="e506b-103">Creates a property definition for the specified type, with the specified `get` and `set` method accessors, and gets a token to that property definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e506b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e506b-104">Syntax</span></span>  
  
```  
HRESULT DefineProperty (   
    [in]  mdTypeDef          td,   
    [in]  LPCWSTR            szProperty,   
    [in]  DWORD              dwPropFlags,   
    [in]  PCCOR_SIGNATURE    pvSig,   
    [in]  ULONG              cbSig,   
    [in]  DWORD              dwCPlusTypeFlag,   
    [in]  void const         *pValue,   
    [in]  ULONG              cchValue,   
    [in]  mdMethodDef        mdSetter,   
    [in]  mdMethodDef        mdGetter,   
    [in]  mdMethodDef        rmdOtherMethods[],   
    [out] mdProperty         *pmdProp   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e506b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e506b-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="e506b-106">[in] Il token per la classe o interfaccia in cui la proprietà è definita.</span><span class="sxs-lookup"><span data-stu-id="e506b-106">[in] The token for class or interface on which the property is being defined.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="e506b-107">[in] Il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-107">[in] The name of the property.</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="e506b-108">[in] Flag della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-108">[in] The property flags.</span></span>  
  
 `pvSig`  
 <span data-ttu-id="e506b-109">[in] Firma della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-109">[in] The property signature.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="e506b-110">[in] Il numero di byte in `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="e506b-110">[in] The count of bytes in `pvSig`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="e506b-111">[in] Il tipo di valore predefinito della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-111">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="e506b-112">[in] Il valore predefinito per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-112">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="e506b-113">[in] Il conteggio dei (Unicode) i caratteri `pValue`.</span><span class="sxs-lookup"><span data-stu-id="e506b-113">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="e506b-114">[in] Il metodo che imposta il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-114">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="e506b-115">[in] Il metodo che ottiene il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-115">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="e506b-116">[in] Matrice di altri metodi associato alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="e506b-116">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="e506b-117">Terminare la matrice con un `mdTokenNil`.</span><span class="sxs-lookup"><span data-stu-id="e506b-117">Terminate the array with an `mdTokenNil`.</span></span>  
  
 `pmdProp`  
 <span data-ttu-id="e506b-118">[out] Il `mdProperty` token assegnato.</span><span class="sxs-lookup"><span data-stu-id="e506b-118">[out] The `mdProperty` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e506b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e506b-119">Requirements</span></span>  
 <span data-ttu-id="e506b-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e506b-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e506b-121">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="e506b-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e506b-122">**Libreria:** usata come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e506b-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e506b-123">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e506b-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e506b-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e506b-124">See Also</span></span>  
 [<span data-ttu-id="e506b-125">IMetaDataEmit (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="e506b-125">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="e506b-126">Interfaccia IMetaDataEmit2</span><span class="sxs-lookup"><span data-stu-id="e506b-126">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)