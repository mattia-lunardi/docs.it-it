---
title: Metodo ISymUnmanagedMethod::GetSourceStartEnd
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSourceStartEnd
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSourceStartEnd
helpviewer_keywords:
- GetSourceStartEnd method [.NET Framework debugging]
- ISymUnmanagedMethod::GetSourceStartEnd method [.NET Framework debugging]
ms.assetid: 2a420900-01f1-4461-8777-3a34a6dc1426
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ecb726f275a694fded2c486448a60b28fadb168
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561868"
---
# <a name="isymunmanagedmethodgetsourcestartend-method"></a>Metodo ISymUnmanagedMethod::GetSourceStartEnd
Ottiene le posizioni del documento iniziale e finale per l'origine di questo metodo. La prima posizione della matrice è l'inizio e la seconda posizione matrice corrisponde alla fine.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetSourceStartEnd(  
    [in]  ISymUnmanagedDocument  *docs[2],  
    [in]  ULONG32                lines[2],  
    [in]  ULONG32                columns[2],  
    [out] BOOL                   *pRetVal);  
```  
  
#### <a name="parameters"></a>Parametri  
 `docs`  
 [in] Le iniziali e finali documenti di origine.  
  
 `lines`  
 [in] Le righe iniziali e finali nel corrispondente dei documenti di origine.  
  
 `columns`  
 [in] Le colonne iniziali e finali nel corrispondente dei documenti di origine.  
  
 `pRetVal`  
 [out] `true` se le posizioni sono state definite; in caso contrario, `false`.  
  
## <a name="return-value"></a>Valore restituito  
 S_OK se il metodo ha esito positivo; in caso contrario, E_FAIL o qualche altro codice di errore.  
  
## <a name="requirements"></a>Requisiti  
 **Intestazione:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
