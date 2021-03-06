---
title: Funzione CreateApplicationContext
ms.date: 03/30/2017
api_name:
- CreateApplicationContext
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateApplicationContext
helpviewer_keywords:
- CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 709769c336d875ee5ddd00b4e1cf919c61e2c394
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54746622"
---
# <a name="createapplicationcontext-function"></a>Funzione CreateApplicationContext
Questa funzione supporta l'infrastruttura .NET Framework e non deve essere usato direttamente dal codice.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
#### <a name="parameters"></a>Parametri  
 `pName`  
 [in] Un puntatore a un nome descrittivo.  
  
 `ppCtx`  
 [out] Un puntatore a un contesto dell'applicazione.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Fusion. h  
  
 **Libreria:** Inclusa come risorsa in Fusion  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia IAssemblyCache](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
- [Funzioni statiche globali Fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
- [Global Assembly Cache](../../../../docs/framework/app-domains/gac.md)
