---
title: Funzione CertTimestampAuthenticodeLicense
ms.date: 03/30/2017
api_name:
- CertTimestampAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d468325a-21c5-43ce-8567-84e342b22308
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9987640f988f2239a01d2dfdbcd6b1684579d8bc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54601507"
---
# <a name="certtimestampauthenticodelicense-function"></a>Funzione CertTimestampAuthenticodeLicense
Aggiunge un timestamp a una licenza Authenticode XrML.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT CertTimestampAuthenticodeLicense (  
    [in]  PCRYPT_DATA_BLOB   pSignedLicenseBlob,  
    [in]  LPCWSTR            pwszTimestampURI,  
    [out] PCRYPT_DATA_BLOB   pTimestampSignatureBlob  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pSignedLicenseBlob`  
 [in] Licenza Authenticode XrML firmata a cui aggiungere un timestamp. Vedere le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) struttura.  
  
 `pwszTimestampURI`  
 [in] URI del server di timestamp.  
  
 `pTimestampSignatureBlob`  
 [out] Puntatore a CRYPT_DATA_BLOB per ricevere la firma del timestamp con codifica base64. È responsabilità del chiamante liberare `pTimestampSignatureBlob` -> `pbData` con `HepFree()` dopo l'uso. Vedere le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) struttura.  
  
## <a name="remarks"></a>Note  
 La firma del timestamp è in realtà un messaggio SignedData PKCS #7 il cui contenuto è il formato binario di SignatureValue dalla firma della licenza. Agisce fondamentalmente come controfirma della licenza.  
  
## <a name="return-value"></a>Valore restituito  
 `S_OK` se la funzione ha esito positivo. In caso contrario, verrà restituito un codice di errore.  
  
## <a name="see-also"></a>Vedere anche
- [Authenticode](../../../../docs/framework/unmanaged-api/authenticode/index.md)
