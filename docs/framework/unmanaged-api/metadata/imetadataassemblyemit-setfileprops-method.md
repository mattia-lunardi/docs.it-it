---
title: Metodo IMetaDataAssemblyEmit::SetFileProps
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetFileProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetFileProps
helpviewer_keywords:
- IMetaDataAssemblyEmit::SetFileProps method [.NET Framework metadata]
- SetFileProps method [.NET Framework metadata]
ms.assetid: 85667d38-611c-45a9-938d-930ac7a7b681
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 203c31129218be585960e771b1d7e669defd8cde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743296"
---
# <a name="imetadataassemblyemitsetfileprops-method"></a>Metodo IMetaDataAssemblyEmit::SetFileProps
Modifica la struttura dei metadati `File` specificata.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT SetFileProps (  
    [in] mdFile        file,  
    [in] const void    *pbHashValue,   
    [in] ULONG         cbHashValue,  
    [in] DWORD         dwFileFlags  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `file`  
 [in] Il token di metadati che specifica il `File` modifica della struttura dei metadati.  
  
 `pbHashValue`  
 [in] Un puntatore per il valore hash dei dati associato al file.  
  
 `cbHashValue`  
 [in] La dimensione in byte di `pbHashValue`.  
  
 `dwFileFlags`  
 [in] Una combinazione bit per bit di [CorFileFlags](../../../../docs/framework/unmanaged-api/metadata/corfileflags-enumeration.md) valori che specificano vari attributi del file.  
  
## <a name="remarks"></a>Note  
 Per creare un `File` struttura dei metadati, usare il [IMetaDataAssemblyEmit:: DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md) (metodo).  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** Vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Cor. h  
  
 **Libreria:** Usato come risorsa in Mscoree. dll  
  
 **Versioni di .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche
- [Interfaccia IMetaDataAssemblyEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
