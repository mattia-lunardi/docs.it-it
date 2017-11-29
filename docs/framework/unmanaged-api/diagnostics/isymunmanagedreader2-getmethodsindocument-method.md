---
title: Metodo ISymUnmanagedReader2::GetMethodsInDocument
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedReader2.GetMethodsInDocument
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedReader2::GetMethodsInDocument
helpviewer_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument method [.NET Framework debugging]
- GetMethodsInDocument method [.NET Framework debugging]
ms.assetid: c7ae84d6-81e8-4cb7-a1f9-d48b6cde5d79
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 15053aeb3febd533a6977ef446fc1aa3bd8a92b8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedreader2getmethodsindocument-method"></a><span data-ttu-id="3e66d-102">Metodo ISymUnmanagedReader2::GetMethodsInDocument</span><span class="sxs-lookup"><span data-stu-id="3e66d-102">ISymUnmanagedReader2::GetMethodsInDocument Method</span></span>
<span data-ttu-id="3e66d-103">Ottiene i metodi che contiene informazioni sulla riga del documento specificato.</span><span class="sxs-lookup"><span data-stu-id="3e66d-103">Gets every method that has line information in the provided document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e66d-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e66d-104">Syntax</span></span>  
  
```  
HRESULT GetMethodsInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is(cMethod),  
        length_is(*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3e66d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e66d-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="3e66d-106">[in] Puntatore al documento.</span><span class="sxs-lookup"><span data-stu-id="3e66d-106">[in] A pointer to the document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="3e66d-107">[in] Oggetto `ULONG32` che indica le dimensioni del `pRetVal` matrice.</span><span class="sxs-lookup"><span data-stu-id="3e66d-107">[in] A `ULONG32` that indicates the size of the  `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="3e66d-108">[out] Un puntatore a un `ULONG32` che riceve le dimensioni del buffer necessaria per contenere i metodi.</span><span class="sxs-lookup"><span data-stu-id="3e66d-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the methods.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="3e66d-109">[out] Puntatore al buffer che riceve i metodi.</span><span class="sxs-lookup"><span data-stu-id="3e66d-109">[out] A pointer to the buffer that receives the methods.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e66d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e66d-110">Return Value</span></span>  
 <span data-ttu-id="3e66d-111">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="3e66d-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e66d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e66d-112">Requirements</span></span>  
 <span data-ttu-id="3e66d-113">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3e66d-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e66d-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3e66d-114">See Also</span></span>  
 [<span data-ttu-id="3e66d-115">ISymUnmanagedReader2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3e66d-115">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)