---
title: Metodo GetScope2
ms.date: 03/30/2017
api_name:
- IALink2.GetScope2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope2
helpviewer_keywords:
- GetScope2 method
ms.assetid: 49435665-6f5a-4acd-9034-8c9244a04a63
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cc986dc27deb08f779a9654324e6832d8420554a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587134"
---
# <a name="getscope2-method"></a>Metodo GetScope2
Ottiene un ambito di importazione.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetScope2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport2** ppImportScope  
) PURE;   
```  
  
#### <a name="parameters"></a>Parametri  
 `AssemblyID`  
 ID dell'assembly di destinazione.  
  
 `FileToken`  
 ID del file da cui importare.  
  
 `dwScope`  
 Ambito in base zero da importare.  
  
 `ppImportScope`  
 Riceve il puntatore alla [interfaccia IMetaDataImport2](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interfaccia per l'ambito indicato.  
  
## <a name="return-value"></a>Valore restituito  
 Restituisce S_OK se il metodo ha esito positivo.  
  
## <a name="requirements"></a>Requisiti  
 Richiede alink.h.  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia IALink2](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [Interfaccia IALink](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [Alink (API)](../../../../docs/framework/unmanaged-api/alink/index.md)
