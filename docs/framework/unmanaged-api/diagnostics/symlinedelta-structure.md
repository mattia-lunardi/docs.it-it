---
title: Struttura SYMLINEDELTA
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: SYMLINEDELTA
api_location: diasymreader.dll
api_type: COM
f1_keywords: SYMLINEDELTA
helpviewer_keywords: SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: cbd83560516e946c03a0ea71cf79fe6d3396bacb
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="symlinedelta-structure"></a><span data-ttu-id="3cc34-102">Struttura SYMLINEDELTA</span><span class="sxs-lookup"><span data-stu-id="3cc34-102">SYMLINEDELTA Structure</span></span>
<span data-ttu-id="3cc34-103">Fornisce informazioni per il gestore dei simboli sui metodi che sono stati spostati in seguito a modifiche.</span><span class="sxs-lookup"><span data-stu-id="3cc34-103">Provides information to the symbol handler about methods that were moved as a result of edits.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cc34-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cc34-104">Syntax</span></span>  
  
```  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a><span data-ttu-id="3cc34-105">Membri</span><span class="sxs-lookup"><span data-stu-id="3cc34-105">Members</span></span>  
  
|<span data-ttu-id="3cc34-106">Membro</span><span class="sxs-lookup"><span data-stu-id="3cc34-106">Member</span></span>|<span data-ttu-id="3cc34-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cc34-107">Description</span></span>|  
|------------|-----------------|  
|`mdMethod`|<span data-ttu-id="3cc34-108">Token di metadati del metodo.</span><span class="sxs-lookup"><span data-stu-id="3cc34-108">The method's metadata token.</span></span>|  
|`delta`|<span data-ttu-id="3cc34-109">Il numero di righe, che il metodo è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="3cc34-109">The number of lines the method was moved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3cc34-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cc34-110">Requirements</span></span>  
 <span data-ttu-id="3cc34-111">**Intestazione:** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="3cc34-111">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3cc34-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3cc34-112">See Also</span></span>  
 [<span data-ttu-id="3cc34-113">Strutture di archivio dei simboli di diagnostica</span><span class="sxs-lookup"><span data-stu-id="3cc34-113">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)