---
title: Enumerazione CorNotificationForTokenMovement
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorNotificationForTokenMovement
api_location: mscoree.dll
api_type: COM
f1_keywords: CorNotificationForTokenMovement
helpviewer_keywords: CorNotificationForTokenMovement enumeration [.NET Framework metadata]
ms.assetid: 1edd1670-976a-4fc8-bef7-7c41e60ad989
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 60d6c56394952fca84b45ba042f7d45a1dec6b1c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="cornotificationfortokenmovement-enumeration"></a><span data-ttu-id="80eb0-102">Enumerazione CorNotificationForTokenMovement</span><span class="sxs-lookup"><span data-stu-id="80eb0-102">CorNotificationForTokenMovement Enumeration</span></span>
<span data-ttu-id="80eb0-103">Specifica le notifiche che verranno inviate al client API dei metadati quando si verifica una modifica del mapping dei token.</span><span class="sxs-lookup"><span data-stu-id="80eb0-103">Specifies the notifications that will be sent to the metadata API client when a token remap occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80eb0-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80eb0-104">Syntax</span></span>  
  
```  
typedef enum CorNotificationForTokenMovement {  
  
    MDNotifyDefault             = 0x0000000f,  
    MDNotifyAll                 = 0xffffffff,  
    MDNotifyNone                = 0x00000000,  
    MDNotifyMethodDef           = 0x00000001,  
    MDNotifyMemberRef           = 0x00000002,  
    MDNotifyFieldDef            = 0x00000004,  
    MDNotifyTypeRef             = 0x00000008,  
  
    MDNotifyTypeDef             = 0x00000010,  
    MDNotifyParamDef            = 0x00000020,  
    MDNotifyInterfaceImpl       = 0x00000040,  
    MDNotifyProperty            = 0x00000080,  
    MDNotifyEvent               = 0x00000100,  
    MDNotifySignature           = 0x00000200,  
    MDNotifyTypeSpec            = 0x00000400,  
    MDNotifyCustomAttribute     = 0x00000800,  
    MDNotifySecurityValue       = 0x00001000,  
    MDNotifyPermission          = 0x00002000,  
    MDNotifyModuleRef           = 0x00004000,  
  
    MDNotifyNameSpace           = 0x00008000,  
  
    MDNotifyAssemblyRef         = 0x01000000,  
    MDNotifyFile                = 0x02000000,  
    MDNotifyExportedType        = 0x04000000,  
    MDNotifyResource            = 0x08000000  
  
} CorNotificationForTokenMovement;  
```  
  
## <a name="members"></a><span data-ttu-id="80eb0-105">Membri</span><span class="sxs-lookup"><span data-stu-id="80eb0-105">Members</span></span>  
  
|<span data-ttu-id="80eb0-106">Membro</span><span class="sxs-lookup"><span data-stu-id="80eb0-106">Member</span></span>|<span data-ttu-id="80eb0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80eb0-107">Description</span></span>|  
|------------|-----------------|  
|`MDNotifyDefault`|<span data-ttu-id="80eb0-108">Notificare quando `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, o `mdFieldDef` spostamento token.</span><span class="sxs-lookup"><span data-stu-id="80eb0-108">Notify when `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, or `mdFieldDef` tokens move.</span></span>|  
|`MDNotifyAll`|<span data-ttu-id="80eb0-109">Notificare quando si sposta tutti i token.</span><span class="sxs-lookup"><span data-stu-id="80eb0-109">Notify when any token moves.</span></span>|  
|`MDNotifyNone`|<span data-ttu-id="80eb0-110">Non notificare quando spostano i token.</span><span class="sxs-lookup"><span data-stu-id="80eb0-110">Do not notify when tokens move.</span></span>|  
|`MDNotifyMethodDef`|<span data-ttu-id="80eb0-111">Inviare una notifica quando un `mdMethodDef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-111">Notify when an `mdMethodDef` token moves.</span></span>|  
|`MDNotifyMemberRef`|<span data-ttu-id="80eb0-112">Inviare una notifica quando un `mdMemberRef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-112">Notify when an `mdMemberRef` token moves.</span></span>|  
|`MDNotifyFieldDef`|<span data-ttu-id="80eb0-113">Inviare una notifica quando un `mdFieldDef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-113">Notify when an `mdFieldDef` token moves.</span></span>|  
|`MDNotifyTypeRef`|<span data-ttu-id="80eb0-114">Inviare una notifica quando un `mdTypeRef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-114">Notify when an `mdTypeRef` token moves.</span></span>|  
|`MDNotifyTypeDef`|<span data-ttu-id="80eb0-115">Inviare una notifica quando un `mdTypeDef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-115">Notify when an `mdTypeDef` token moves.</span></span>|  
|`MDNotifyParamDef`|<span data-ttu-id="80eb0-116">Inviare una notifica quando un `mdParamDef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-116">Notify when an `mdParamDef` token moves.</span></span>|  
|`MDNotifyInterfaceImpl`|<span data-ttu-id="80eb0-117">Inviare una notifica quando un `mdInterfaceImpl` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-117">Notify when an `mdInterfaceImpl` token moves.</span></span>|  
|`MDNotifyProperty`|<span data-ttu-id="80eb0-118">Inviare una notifica quando un `mdProperty` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-118">Notify when an `mdProperty` token moves.</span></span>|  
|`MDNotifyEvent`|<span data-ttu-id="80eb0-119">Inviare una notifica quando un `mdEvent` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-119">Notify when an `mdEvent` token moves.</span></span>|  
|`MDNotifySignature`|<span data-ttu-id="80eb0-120">Inviare una notifica quando un `mdSignature` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-120">Notify when an `mdSignature` token moves.</span></span>|  
|`MDNotifyTypeSpec`|<span data-ttu-id="80eb0-121">Inviare una notifica quando un `mdTypeSpec` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-121">Notify when an `mdTypeSpec` token moves.</span></span>|  
|`MDNotifyCustomAttribute`|<span data-ttu-id="80eb0-122">Inviare una notifica quando un `mdCustomAttribute` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-122">Notify when an `mdCustomAttribute` token moves.</span></span>|  
|`MDNotifySecurityValue`|<span data-ttu-id="80eb0-123">Inviare una notifica quando un `mdSecurityValue` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-123">Notify when an `mdSecurityValue` token moves.</span></span>|  
|`MDNotifyPermission`|<span data-ttu-id="80eb0-124">Inviare una notifica quando un `mdPermission` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-124">Notify when an `mdPermission` token moves.</span></span>|  
|`MDNotifyModuleRef`|<span data-ttu-id="80eb0-125">Inviare una notifica quando un `mdModuleRef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-125">Notify when an `mdModuleRef` token moves.</span></span>|  
|`MDNotifyNameSpace`|<span data-ttu-id="80eb0-126">Inviare una notifica quando un `mdNameSpace` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-126">Notify when an `mdNameSpace` token moves.</span></span>|  
|`MDNotifyAssemblyRef`|<span data-ttu-id="80eb0-127">Inviare una notifica quando un `mdAssemblyRef` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-127">Notify when an `mdAssemblyRef` token moves.</span></span>|  
|`MDNotifyFile`|<span data-ttu-id="80eb0-128">Inviare una notifica quando un `mdFile` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-128">Notify when an `mdFile` token moves.</span></span>|  
|`MDNotifyExportedType`|<span data-ttu-id="80eb0-129">Inviare una notifica quando un `mdExportedType` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-129">Notify when an `mdExportedType` token moves.</span></span>|  
|`MDNotifyResource`|<span data-ttu-id="80eb0-130">Inviare una notifica quando un `mdManifestResource` token passa.</span><span class="sxs-lookup"><span data-stu-id="80eb0-130">Notify when an `mdManifestResource` token moves.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="80eb0-131">Note</span><span class="sxs-lookup"><span data-stu-id="80eb0-131">Remarks</span></span>  
 <span data-ttu-id="80eb0-132">Un token può essere mappato nuovamente (ovvero spostarlo) durante un'unione di metadati.</span><span class="sxs-lookup"><span data-stu-id="80eb0-132">A token may be re-mapped (that is, moved) during a metadata merge.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="80eb0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80eb0-133">Requirements</span></span>  
 <span data-ttu-id="80eb0-134">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="80eb0-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80eb0-135">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="80eb0-135">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="80eb0-136">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80eb0-136">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80eb0-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="80eb0-137">See Also</span></span>  
 [<span data-ttu-id="80eb0-138">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="80eb0-138">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)