---
title: Interfaccia ICorDebugILCode2
ms.date: 03/30/2017
api_name:
- ICorDebugILCode2
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: f9dc2afd-df8a-464d-bdbf-5af0a1d4bf85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d511999cac312c785e528cda24c215555a62ae76
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491168"
---
# <a name="icordebugilcode2-interface"></a>Interfaccia ICorDebugILCode2
[Supportato in .NET Framework 4.5.2 e versioni successive]  
  
 Estende logicamente il [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) interfaccia per fornire i metodi che restituiscono il token di firma della variabile locale di una funzione e che eseguire il mapping di linguaggio intermedio instrumentato del profiler (IL) agli offset linguaggio intermedio del metodo originale viene eseguito l'offset.  
  
## <a name="methods"></a>Metodi  
  
|Metodo|Descrizione|  
|------------|-----------------|  
|[Metodo GetInstrumentedILMap](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md)|Restituisce una mappa dagli offset IL instrumentati dal profiler agli offset IL elaborati con il metodo originale per l'istanza corrente.|  
|[Metodo GetLocalVarSigToken](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getlocalvarsigtoken-method.md)|Ottiene il token di metadati per la firma di una variabile locale della funzione rappresentata da questa istanza.|  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** CorDebug.idl, CorDebug.h  
  
 **Libreria:** CorGuids.lib  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)
- [Interfacce di debug](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Debug](../../../../docs/framework/unmanaged-api/debugging/index.md)
