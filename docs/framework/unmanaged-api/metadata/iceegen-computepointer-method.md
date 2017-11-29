---
title: Metodo ICeeGen::ComputePointer
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICeeGen.ComputePointer
api_location: mscoree.dll
api_type: COM
f1_keywords: ICeeGen::ComputePointer
helpviewer_keywords:
- ICeeGen::ComputePointer method [.NET Framework metadata]
- ComputePointer method [.NET Framework metadata]
ms.assetid: b6b95c04-0f2c-4fcc-a8bc-3b1dcbdba731
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c1f5f1c0ea5672812fca387b34238ada2a109938
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iceegencomputepointer-method"></a><span data-ttu-id="f1997-102">Metodo ICeeGen::ComputePointer</span><span class="sxs-lookup"><span data-stu-id="f1997-102">ICeeGen::ComputePointer Method</span></span>
<span data-ttu-id="f1997-103">Determina il buffer per la sezione di codice specificato.</span><span class="sxs-lookup"><span data-stu-id="f1997-103">Determines the buffer for the specified code section.</span></span>  
  
 <span data-ttu-id="f1997-104">Questo metodo è obsoleto e non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f1997-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1997-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1997-105">Syntax</span></span>  
  
```  
HRESULT ComputePointer (  
    [in]  HCEESECTION  section,  
    [in]  ULONG        RVA,   
    [out] UCHAR        **lpBuffer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f1997-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1997-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="f1997-107">[in] La sezione di codice per il quale restituire un buffer.</span><span class="sxs-lookup"><span data-stu-id="f1997-107">[in] The code section for which to return a buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="f1997-108">[in] L'indirizzo virtuale relativo del metodo per il quale ottenere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="f1997-108">[in] The relative virtual address of the method for which to get a pointer.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="f1997-109">[out] Puntatore al buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="f1997-109">[out] A pointer to the returned buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1997-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1997-110">Requirements</span></span>  
 <span data-ttu-id="f1997-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f1997-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1997-112">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="f1997-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f1997-113">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f1997-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f1997-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1997-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1997-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f1997-115">See Also</span></span>  
 [<span data-ttu-id="f1997-116">ICeeGen (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f1997-116">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)