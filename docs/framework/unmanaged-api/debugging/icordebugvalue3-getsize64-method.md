---
title: Metodo ICorDebugValue3::GetSize64
ms.date: 03/30/2017
api_name:
- ICorDebugValue3::GetSize64
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue3::GetSize64
helpviewer_keywords:
- GetSize64 method, ICorDebugValue3 interface [.NET Framework debugging]
- ICorDebugValue3::GetSize64 method [.NET Framework debugging]
ms.assetid: fee56a29-3154-4192-958d-71da2ced3740
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f56e9fef64a08be311d66845e42887a6aa821f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720002"
---
# <a name="icordebugvalue3getsize64-method"></a>Metodo ICorDebugValue3::GetSize64
Ottiene la dimensione, espressa in byte, di questo [ICorDebugValue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md) oggetto.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetSize64(  
    [out] ULONG64 *pSize  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 pSize  
 [out] Un puntatore alla dimensione, espressa in byte, di questo oggetto.  
  
## <a name="remarks"></a>Note  
 Se questo tipo di valore è un tipo riferimento, questo metodo restituisce la dimensione del puntatore anziché le dimensioni dell'oggetto.  
  
 Il `ICorDebugValue3::GetSize` metodo si differenzia dal [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md) metodo nel tipo del relativo parametro di output. Nelle [ICorDebugValue](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md), il parametro di output è un `ULONG32`; nella `ICorDebugValue3::GetSize`, è un `ULONG64`. In questo modo, il [ICorDebugValue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md) interfaccia per segnalare le dimensioni delle matrici che superano 2 GB.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** CorDebug.idl, CorDebug.h  
  
 **Libreria:** CorGuids.lib  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ICorDebugValue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
- [Interfacce di debug](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
