---
title: Metodo ISymUnmanagedWriter::SetScopeRange
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetScopeRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetScopeRange
helpviewer_keywords:
- SetScopeRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetScopeRange method [.NET Framework debugging]
ms.assetid: d4d98676-444b-46ca-bfe6-0d827385cd22
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: da50542d9f57e008b31ce2e6ed9698df1275d5eb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618808"
---
# <a name="isymunmanagedwritersetscoperange-method"></a>Metodo ISymUnmanagedWriter::SetScopeRange
Definisce l'intervallo di offset per l'ambito lessicale specificato. L'ambito diventa il nuovo ambito corrente e viene inserito nello stack di ambiti. Gli ambiti devono formare una gerarchia. Elementi di pari livello non possono sovrapporsi.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT OpenScope(  
    [in] ULONG32  scopeID,  
    [in] ULONG32  startOffset,  
    [in] ULONG32  endOffset);  
```  
  
#### <a name="parameters"></a>Parametri  
 `scopeId`  
 [in] L'identificatore di ambito per l'ambito.  
  
 `startOffset`  
 [in] Offset, in byte, della prima istruzione dell'ambito lessicale a partire dall'inizio del metodo.  
  
 `endOffset`  
 [in] Offset, in byte, dell'ultima istruzione nell'ambito lessicale a partire dall'inizio del metodo.  
  
## <a name="return-value"></a>Valore restituito  
 S_OK se il metodo ha esito positivo; in caso contrario, E_FAIL o qualche altro codice di errore.  
  
## <a name="remarks"></a>Note  
 [ISymUnmanagedWriter:: OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) restituisce un identificatore di ambito opaco che può essere usato con `ISymUnmanagedWriter::SetScopeRange` per definire un ambito dell'offset iniziale e finale in un secondo momento. In questo caso, gli offset passati a `ISymUnmanagedWriter::OpenScope` e [CloseScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md) vengono ignorati. Gli identificatori di ambito solo sono validi nel metodo corrente.  
  
## <a name="requirements"></a>Requisiti  
 **Intestazione:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
