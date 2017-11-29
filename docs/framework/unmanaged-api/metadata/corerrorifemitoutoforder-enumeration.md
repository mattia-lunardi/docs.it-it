---
title: Enumerazione CorErrorIfEmitOutOfOrder
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorErrorIfEmitOutOfOrder
api_location: mscoree.dll
api_type: COM
f1_keywords: CorErrorIfEmitOutOfOrder
helpviewer_keywords: CorErrorIfEmitOutOfOrder enumeration [.NET Framework metadata]
ms.assetid: 6d758aad-29a7-44fe-9481-bbff5b799a32
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d2cf80375622912c6bb9a59696f37aed2d594253
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corerrorifemitoutoforder-enumeration"></a><span data-ttu-id="7747b-102">Enumerazione CorErrorIfEmitOutOfOrder</span><span class="sxs-lookup"><span data-stu-id="7747b-102">CorErrorIfEmitOutOfOrder Enumeration</span></span>
<span data-ttu-id="7747b-103">Contiene valori di flag che indicano in quali condizioni è necessario generare un messaggio di errore per notificare che i metadati sono stati emessi senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-103">Contains flag values that indicate the conditions under which an error message should be generated when metadata is emitted out of order.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7747b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7747b-104">Syntax</span></span>  
  
```  
typedef enum CorErrorIfEmitOutOfOrder {  
  
    MDErrorOutOfOrderDefault    = 0x00000000,  
    MDErrorOutOfOrderNone       = 0x00000000,  
    MDErrorOutOfOrderAll        = 0xffffffff,  
    MDMethodOutOfOrder          = 0x00000001,  
    MDFieldOutOfOrder           = 0x00000002,  
    MDParamOutOfOrder           = 0x00000004,  
    MDPropertyOutOfOrder        = 0x00000008,  
    MDEventOutOfOrder           = 0x00000010  
  
} CorErrorIfEmitOutOfOrder;  
```  
  
## <a name="members"></a><span data-ttu-id="7747b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="7747b-105">Members</span></span>  
  
|<span data-ttu-id="7747b-106">Membro</span><span class="sxs-lookup"><span data-stu-id="7747b-106">Member</span></span>|<span data-ttu-id="7747b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7747b-107">Description</span></span>|  
|------------|-----------------|  
|`MDErrorOutOfOrderDefault`|<span data-ttu-id="7747b-108">Indica il comportamento predefinito, che non genera messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="7747b-108">Indicates the default behavior, which does not generate error messages.</span></span>|  
|`MDErrorOutOfOrderNone`|<span data-ttu-id="7747b-109">Indica che il compilatore non deve generare messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="7747b-109">Indicates that the compiler should not generate error messages.</span></span>|  
|`MDErrorOutOfOrderAll`|<span data-ttu-id="7747b-110">Indica che il compilatore deve generare un messaggio di errore quando un campo, proprietà, evento, un metodo, o parametro è emesso senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-110">Indicates that the compiler should generate an error message when a field, property, event, method, or parameter is emitted out of order.</span></span>|  
|`MDMethodOutOfOrder`|<span data-ttu-id="7747b-111">Indica che il compilatore deve generare un messaggio di errore quando un metodo è emesso senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-111">Indicates that the compiler should generate an error message when a method is emitted out of order.</span></span>|  
|`MDFieldOutOfOrder`|<span data-ttu-id="7747b-112">Indica che il compilatore deve generare un messaggio di errore quando un campo è emesso senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-112">Indicates that the compiler should generate an error message when a field is emitted out of order.</span></span>|  
|`MDParamOutOfOrder`|<span data-ttu-id="7747b-113">Indica che il compilatore deve generare un messaggio di errore quando un parametro è emesso senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-113">Indicates that the compiler should generate an error message when a parameter is emitted out of order.</span></span>|  
|`MDPropertyOutOfOrder`|<span data-ttu-id="7747b-114">Indica che il compilatore deve generare un messaggio di errore quando una proprietà è emesso senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-114">Indicates that the compiler should generate an error message when a property is emitted out of order.</span></span>|  
|`MDEventOutOfOrder`|<span data-ttu-id="7747b-115">Indica che il compilatore deve generare un messaggio di errore quando un evento è emesso senza ordine.</span><span class="sxs-lookup"><span data-stu-id="7747b-115">Indicates that the compiler should generate an error message when an event is emitted out of order.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7747b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7747b-116">Requirements</span></span>  
 <span data-ttu-id="7747b-117">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7747b-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7747b-118">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="7747b-118">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="7747b-119">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7747b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7747b-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7747b-120">See Also</span></span>  
 [<span data-ttu-id="7747b-121">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="7747b-121">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)