---
title: Metodo ICorPublishProcess::IsManaged
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::IsManaged
helpviewer_keywords:
- IsManaged method, ICorPublishProcess interface [.NET Framework debugging]
- ICorPublishProcess::IsManaged method [.NET Framework debugging]
ms.assetid: 06b1f7cc-acdf-47a6-9d53-d9dec2424152
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b57a8bcc584ffd209def5a84a99b15daa7480ee6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534943"
---
# <a name="icorpublishprocessismanaged-method"></a>Metodo ICorPublishProcess::IsManaged
Ottiene un valore che indica se il processo di cui viene fatto riferimento da questo [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) è noto al codice gestito.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT IsManaged (  
    [out] BOOL   *pbManaged  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pbManaged`  
 [out] Un puntatore a un valore booleano che indica se il processo con codice gestito. Il valore è `true` se il processo dispone di codice gestito; in caso contrario, `false`.  
  
## <a name="remarks"></a>Note  
 Poiché la versione corrente di `ICorPublishProcess` consenta l'accesso solo ai processi con codice gestito, `IsManaged` restituisce sempre `true`.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** CorPub.idl, CorPub.h  
  
 **Libreria:** CorGuids.lib  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
