---
title: Metodo ICeeGen::GetSectionCreate
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICeeGen.GetSectionCreate
api_location: mscoree.dll
api_type: COM
f1_keywords: ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type: apiref
caps.latest.revision: "15"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 2ea9cb20b62e1b1fa8e726ba0c49c5e24202530c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iceegengetsectioncreate-method"></a><span data-ttu-id="f12c8-102">Metodo ICeeGen::GetSectionCreate</span><span class="sxs-lookup"><span data-stu-id="f12c8-102">ICeeGen::GetSectionCreate Method</span></span>
<span data-ttu-id="f12c8-103">Genera l'errore e ottiene una sezione di codice utilizzando il nome specificato e i valori di flag.</span><span class="sxs-lookup"><span data-stu-id="f12c8-103">Generates and gets a code section using the specified name and flag values.</span></span>  
  
 <span data-ttu-id="f12c8-104">Questo metodo è obsoleto e non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f12c8-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f12c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f12c8-105">Syntax</span></span>  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f12c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f12c8-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="f12c8-107">[in] Un puntatore a una stringa che specifica il nome della sezione da creare.</span><span class="sxs-lookup"><span data-stu-id="f12c8-107">[in] A pointer to a string that specifies the name of the section to be created.</span></span>  
  
 `flags`  
 <span data-ttu-id="f12c8-108">[in] Flag che specificano le opzioni.</span><span class="sxs-lookup"><span data-stu-id="f12c8-108">[in] Flags that specify options.</span></span>  
  
 `section`  
 <span data-ttu-id="f12c8-109">[out] Puntatore alla sezione di codice appena creato.</span><span class="sxs-lookup"><span data-stu-id="f12c8-109">[out] A pointer to the newly created code section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f12c8-110">Note</span><span class="sxs-lookup"><span data-stu-id="f12c8-110">Remarks</span></span>  
 <span data-ttu-id="f12c8-111">Chiamare `GetSectionCreate` solo se sono necessari requisiti speciali di sezione che non sono gestiti da altri metodi.</span><span class="sxs-lookup"><span data-stu-id="f12c8-111">Call `GetSectionCreate` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f12c8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f12c8-112">Requirements</span></span>  
 <span data-ttu-id="f12c8-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f12c8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f12c8-114">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="f12c8-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f12c8-115">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f12c8-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f12c8-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f12c8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f12c8-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f12c8-117">See Also</span></span>  
 [<span data-ttu-id="f12c8-118">ICeeGen (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f12c8-118">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)