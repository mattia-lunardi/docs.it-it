---
title: Metodo ISymUnmanagedSourceServerModule::GetSourceServerData
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedSourceServerModule.GetSourceServerData
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedSourceServerModule::GetSourceServerData
helpviewer_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData method [.NET Framework debugging]
- GetSourceServerData method [.NET Framework debugging]
ms.assetid: 20bdf8ff-2d15-4c64-8950-6888f642d6c0
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5774e46f69a7c38943314697575c7aef67b96693
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedsourceservermodulegetsourceserverdata-method"></a><span data-ttu-id="e4a63-102">Metodo ISymUnmanagedSourceServerModule::GetSourceServerData</span><span class="sxs-lookup"><span data-stu-id="e4a63-102">ISymUnmanagedSourceServerModule::GetSourceServerData Method</span></span>
<span data-ttu-id="e4a63-103">Restituisce i dati del server di origine per il modulo.</span><span class="sxs-lookup"><span data-stu-id="e4a63-103">Returns the source server data for the module.</span></span> <span data-ttu-id="e4a63-104">Il chiamante deve liberare risorse mediante `CoTaskMemFree`.</span><span class="sxs-lookup"><span data-stu-id="e4a63-104">The caller must free resources by using `CoTaskMemFree`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4a63-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4a63-105">Syntax</span></span>  
  
```  
HRESULT GetSourceServerData(  
    [out] ULONG* pDataByteCount,   
    [out, size_is (, *pDataByteCount)] BYTE** ppData);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e4a63-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4a63-106">Parameters</span></span>  
 `pDataByteCount`  
 <span data-ttu-id="e4a63-107">[out] Un puntatore a un `ULONG32` che riceve le dimensioni, in byte, dei dati di server di origine.</span><span class="sxs-lookup"><span data-stu-id="e4a63-107">[out] A pointer to a `ULONG32` that receives the size, in bytes, of the source server data.</span></span>  
  
 `ppData`  
 <span data-ttu-id="e4a63-108">[out] Un puntatore all'oggetto restituito `pDataByteCount` valore.</span><span class="sxs-lookup"><span data-stu-id="e4a63-108">[out] A pointer to the returned `pDataByteCount` value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4a63-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4a63-109">Return Value</span></span>  
 <span data-ttu-id="e4a63-110">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="e4a63-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4a63-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4a63-111">Requirements</span></span>  
 <span data-ttu-id="e4a63-112">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e4a63-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4a63-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e4a63-113">See Also</span></span>  
 [<span data-ttu-id="e4a63-114">ISymUnmanagedSourceServerModule (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="e4a63-114">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)