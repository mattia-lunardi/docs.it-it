---
title: Metodo ICorDebugFrame::GetStackRange
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetStackRange
helpviewer_keywords:
- GetStackRange method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetStackRange method [.NET Framework debugging]
ms.assetid: fab037cb-fda6-40fb-9367-921e435dd5a0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5da87071bc23ac17a3077049cd77f0fb8611439f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413020"
---
# <a name="icordebugframegetstackrange-method"></a>Metodo ICorDebugFrame::GetStackRange
Ottiene l'intervallo di indirizzi assoluti dello stack frame corrente.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,   
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pStart`  
 [out] Un puntatore a un `CORDB_ADDRESS` che specifica l'indirizzo iniziale dello stack frame rappresentato da questo `ICorDebugFrame` oggetto.  
  
 `pEnd`  
 [out] Un puntatore a un `CORDB_ADDRESS` che specifica l'indirizzo finale dello stack frame rappresentato da questo `ICorDebugFrame` oggetto.  
  
## <a name="remarks"></a>Note  
 L'intervallo di indirizzi dello stack è utile per riunire le tracce dello stack con interfoliazione raccolte da più motori di debug. L'intervallo numerico non fornisce informazioni sul contenuto del frame dello stack. È significativo solo per il confronto di percorsi dello stack frame.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Cordebug. idl, Cordebug. H  
  
 **Libreria:** CorGuids. lib  
  
 **Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
