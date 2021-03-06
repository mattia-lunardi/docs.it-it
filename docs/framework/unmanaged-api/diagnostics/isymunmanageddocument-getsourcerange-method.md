---
title: Metodo ISymUnmanagedDocument::GetSourceRange
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a89c706ece0949ffa3c182d53b57221acf81b18d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515070"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a>Metodo ISymUnmanagedDocument::GetSourceRange
Restituisce l'intervallo specificato dell'origine incorporata al buffer specificato. Il buffer deve essere sufficientemente grande da contenere l'origine.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
#### <a name="parameters"></a>Parametri  
 `startLine`  
 [in] La riga iniziale del documento corrente.  
  
 `startColumn`  
 [in] La colonna iniziale del documento corrente.  
  
 `endLine`  
 [in] La riga finale nel documento corrente.  
  
 `endColumn`  
 [in] La colonna finale del documento corrente.  
  
 `cSourceBytes`  
 [in] Le dimensioni dell'origine, in byte.  
  
 `pcSourceBytes`  
 [out] Puntatore a una variabile che riceve le dimensioni di origine.  
  
 `source`  
 [out] Le dimensioni e la lunghezza dell'intervallo specificato del documento di origine, in byte.  
  
## <a name="return-value"></a>Valore restituito  
 S_OK se il metodo ha esito positivo.  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia ISymUnmanagedDocument](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
