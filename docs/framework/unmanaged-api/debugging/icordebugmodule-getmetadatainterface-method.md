---
title: Metodo ICorDebugModule::GetMetaDataInterface
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugModule.GetMetaDataInterface
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugModule::GetMetaDataInterface
helpviewer_keywords:
- ICorDebugModule::GetMetaDatainterface method [.NET Framework debugging]
- GetMetaDatainterface method [.NET Framework debugging]
ms.assetid: 30d906f2-cf35-4fa9-9d4c-0c31b58c9f3a
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f4b1944c68db0cbdd8eb49e10433defc953e4494
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugmodulegetmetadatainterface-method"></a><span data-ttu-id="eef9b-102">Metodo ICorDebugModule::GetMetaDataInterface</span><span class="sxs-lookup"><span data-stu-id="eef9b-102">ICorDebugModule::GetMetaDataInterface Method</span></span>
<span data-ttu-id="eef9b-103">Ottiene un oggetto di interfaccia di metadati che può essere utilizzato per esaminare i metadati per il modulo.</span><span class="sxs-lookup"><span data-stu-id="eef9b-103">Gets a metadata interface object that can be used to examine the metadata for the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eef9b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eef9b-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataInterface (  
    [in] REFIID      riid,  
    [out] IUnknown **ppObj  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="eef9b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="eef9b-105">Parameters</span></span>  
 `riid`  
 <span data-ttu-id="eef9b-106">[in] L'ID di riferimento che specifica l'interfaccia dei metadati.</span><span class="sxs-lookup"><span data-stu-id="eef9b-106">[in] The reference ID that specifies the metadata interface.</span></span>  
  
 `ppObj`  
 <span data-ttu-id="eef9b-107">[out] Un puntatore all'indirizzo di un `T:IUnknown` oggetto che è uno del [interfacce di metadati](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="eef9b-107">[out] A pointer to the address of an `T:IUnknown` object that is one of the [metadata interfaces](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eef9b-108">Note</span><span class="sxs-lookup"><span data-stu-id="eef9b-108">Remarks</span></span>  
 <span data-ttu-id="eef9b-109">Il debugger può utilizzare il `GetMetaDataInterface` metodo per creare una copia dei metadati originali di un modulo, per modificare tale modulo.</span><span class="sxs-lookup"><span data-stu-id="eef9b-109">The debugger can use the `GetMetaDataInterface` method to make a copy of the original metadata for a module, which it must do in order to edit that module.</span></span> <span data-ttu-id="eef9b-110">Il debugger chiama `GetMetaDataInterface` per ottenere un [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) oggetto di interfaccia per il modulo, quindi chiama [IMetaDataEmit:: SaveToMemory](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-savetomemory-method.md) per salvare una copia dei metadati del modulo in memoria.</span><span class="sxs-lookup"><span data-stu-id="eef9b-110">The debugger calls `GetMetaDataInterface` to get an [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface object for the module, then calls [IMetaDataEmit::SaveToMemory](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-savetomemory-method.md) to save a copy of the module's metadata to memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eef9b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eef9b-111">Requirements</span></span>  
 <span data-ttu-id="eef9b-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eef9b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eef9b-113">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="eef9b-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eef9b-114">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eef9b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eef9b-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eef9b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eef9b-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eef9b-116">See Also</span></span>  
 [<span data-ttu-id="eef9b-117">Metadati</span><span class="sxs-lookup"><span data-stu-id="eef9b-117">Metadata</span></span>](../../../../docs/framework/unmanaged-api/metadata/index.md)