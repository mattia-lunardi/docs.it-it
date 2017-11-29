---
title: Funzione StrongNameKeyGen
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StrongNameKeyGen
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: StrongNameKeyGen
helpviewer_keywords: StrongNameKeyGen function [.NET Framework strong naming]
ms.assetid: 883e413a-ad2f-4f7f-b1b9-aeb8fe5b65f8
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 4410719674b72bf25be63756edc89802740cb3cf
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="strongnamekeygen-function"></a><span data-ttu-id="aec7d-102">Funzione StrongNameKeyGen</span><span class="sxs-lookup"><span data-stu-id="aec7d-102">StrongNameKeyGen Function</span></span>
<span data-ttu-id="aec7d-103">Crea una nuova coppia di chiavi pubblica/privata per l'utilizzo con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="aec7d-103">Creates a new public/private key pair for strong name use.</span></span>  
  
 <span data-ttu-id="aec7d-104">Questa funzione è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="aec7d-104">This function has been deprecated.</span></span> <span data-ttu-id="aec7d-105">Utilizzare il [ICLRStrongName:: StrongNameKeyGen](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md) metodo invece.</span><span class="sxs-lookup"><span data-stu-id="aec7d-105">Use the [ICLRStrongName::StrongNameKeyGen](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aec7d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aec7d-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameKeyGen (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aec7d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aec7d-107">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="aec7d-108">[in] Il nome di contenitore di chiavi richiesto.</span><span class="sxs-lookup"><span data-stu-id="aec7d-108">[in] The requested key container name.</span></span> <span data-ttu-id="aec7d-109">`wszKeyContainer`deve essere una stringa non vuota o null per generare un nome temporaneo.</span><span class="sxs-lookup"><span data-stu-id="aec7d-109">`wszKeyContainer` must be a non-empty string, or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="aec7d-110">[in] Specifica se mantenere la chiave registrata.</span><span class="sxs-lookup"><span data-stu-id="aec7d-110">[in] Specifies whether to leave the key registered.</span></span> <span data-ttu-id="aec7d-111">Sono supportati i seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="aec7d-111">The following values are supported:</span></span>  
  
-   <span data-ttu-id="aec7d-112">0x00000000 - utilizzato quando `wszKeyContainer` è null per generare un nome di contenitore di chiavi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="aec7d-112">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
-   <span data-ttu-id="aec7d-113">0x00000001 (`SN_LEAVE_KEY`)-specifica che la chiave deve essere registrata a sinistra.</span><span class="sxs-lookup"><span data-stu-id="aec7d-113">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="aec7d-114">[out] La coppia di chiavi pubblica/privata restituita.</span><span class="sxs-lookup"><span data-stu-id="aec7d-114">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="aec7d-115">[out] Le dimensioni, in byte, di `ppbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="aec7d-115">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="aec7d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aec7d-116">Return Value</span></span>  
 <span data-ttu-id="aec7d-117">`true`al termine dell'esecuzione; in caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="aec7d-117">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aec7d-118">Note</span><span class="sxs-lookup"><span data-stu-id="aec7d-118">Remarks</span></span>  
 <span data-ttu-id="aec7d-119">Il `StrongNameKeyGen` funzione crea una chiave a 1024 bit.</span><span class="sxs-lookup"><span data-stu-id="aec7d-119">The `StrongNameKeyGen` function creates a 1024-bit key.</span></span> <span data-ttu-id="aec7d-120">Dopo il recupero della chiave, è necessario chiamare il [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) funzione per rilasciare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="aec7d-120">After the key is retrieved, you should call the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="aec7d-121">Se il `StrongNameKeyGen` funzione non viene completata correttamente, chiamare il [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) per recuperare l'ultimo errore generato.</span><span class="sxs-lookup"><span data-stu-id="aec7d-121">If the `StrongNameKeyGen` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aec7d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aec7d-122">Requirements</span></span>  
 <span data-ttu-id="aec7d-123">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aec7d-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aec7d-124">**Intestazione:** StrongName. H</span><span class="sxs-lookup"><span data-stu-id="aec7d-124">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="aec7d-125">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="aec7d-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="aec7d-126">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aec7d-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aec7d-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aec7d-127">See Also</span></span>  
 [<span data-ttu-id="aec7d-128">StrongNameKeyGen (metodo)</span><span class="sxs-lookup"><span data-stu-id="aec7d-128">StrongNameKeyGen Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md)  
 [<span data-ttu-id="aec7d-129">StrongNameKeyGenEx (metodo)</span><span class="sxs-lookup"><span data-stu-id="aec7d-129">StrongNameKeyGenEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygenex-method.md)  
 [<span data-ttu-id="aec7d-130">ICLRStrongName (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="aec7d-130">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)