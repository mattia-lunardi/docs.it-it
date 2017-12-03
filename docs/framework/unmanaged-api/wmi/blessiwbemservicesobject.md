---
title: Funzione BlessIWbemServicesObject (riferimenti alle API non gestite)
description: La funzione BlessIWbemServicesObject indica se le credenziali utente consentono l'accesso a un oggetto IWbemServices
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: BlessIWbemServicesObject
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: BlessIWbemServicesObject
helpviewer_keywords: BlessIWbemServicesObject function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ebba6df29b814315180e9c8e936e5e1ad175ecf8
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2017
---
# <a name="blessiwbemservicesobject-function"></a><span data-ttu-id="cb52c-103">BlessIWbemServicesObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb52c-103">BlessIWbemServicesObject function</span></span>
<span data-ttu-id="cb52c-104">Indica se le credenziali utente di consentono l'accesso a un oggetto specificato [IWbemServices](https://msdn.microsoft.com/library/aa392093(v=vs.85).aspx) oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb52c-104">Indicates whether the user credentials permit access to a specified [IWbemServices](https://msdn.microsoft.com/library/aa392093(v=vs.85).aspx) object.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="cb52c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb52c-105">Syntax</span></span>  
  
```  
HRESULT BlessIWbemServicesObject (
   [in] IUnknown* pIUnknown,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```  

## <a name="parameters"></a><span data-ttu-id="cb52c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb52c-106">Parameters</span></span>

`pIWbemServices`  
<span data-ttu-id="cb52c-107">[in] Puntatore a un oggetto servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="cb52c-107">[in] A pointer to a WMI service object.</span></span>

`strUser`  
<span data-ttu-id="cb52c-108">[in] Il nome utente.</span><span class="sxs-lookup"><span data-stu-id="cb52c-108">[in] The user name.</span></span>

`strPassword`  
<span data-ttu-id="cb52c-109">[in] La password associata a `strUser`.</span><span class="sxs-lookup"><span data-stu-id="cb52c-109">[in] The password associated with `strUser`.</span></span>

<span data-ttu-id="cb52c-110">`strAuthority`[in] Il nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cb52c-110">`strAuthority` [in] The domain name of the user.</span></span> <span data-ttu-id="cb52c-111">Vedere il [ConnectServerWmi](connectserverwmi.md) funzione per ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="cb52c-111">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

<span data-ttu-id="cb52c-112">`impLevel`[in] Il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="cb52c-112">`impLevel` [in] The impersonation level.</span></span>

<span data-ttu-id="cb52c-113">`authnLevel`[in] Il livello di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb52c-113">`authnLevel` [in] The authorization level.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb52c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb52c-114">Return value</span></span>

<span data-ttu-id="cb52c-115">I seguenti valori restituiti da questa funzione sono definiti nel *Winerror* file di intestazione, oppure è possibile definirli come costanti nel codice:</span><span class="sxs-lookup"><span data-stu-id="cb52c-115">The following values returned by this function are defined in the *WinError.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="cb52c-116">Costante</span><span class="sxs-lookup"><span data-stu-id="cb52c-116">Constant</span></span>  |<span data-ttu-id="cb52c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cb52c-117">Value</span></span>  |<span data-ttu-id="cb52c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb52c-118">Description</span></span>  |
|---------|---------|---------|
| `E_INVALIDARG` | <span data-ttu-id="cb52c-119">0x80070057</span><span class="sxs-lookup"><span data-stu-id="cb52c-119">0x80070057</span></span> | <span data-ttu-id="cb52c-120">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="cb52c-120">One or more arguments are invalid.</span></span> |
| `E_POINTER` | <span data-ttu-id="cb52c-121">0x80004003</span><span class="sxs-lookup"><span data-stu-id="cb52c-121">0x80004003</span></span> | <span data-ttu-id="cb52c-122">`pIWbemServices` è `null`.</span><span class="sxs-lookup"><span data-stu-id="cb52c-122">`pIWbemServices` is `null`.</span></span> | 
| `E_FAIL` | <span data-ttu-id="cb52c-123">0x80000008</span><span class="sxs-lookup"><span data-stu-id="cb52c-123">0x80000008</span></span> | <span data-ttu-id="cb52c-124">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="cb52c-124">An unspecified error has occurred.</span></span> |
| `E_OUTOFMEMORY` | <span data-ttu-id="cb52c-125">0x80000002</span><span class="sxs-lookup"><span data-stu-id="cb52c-125">0x80000002</span></span> | <span data-ttu-id="cb52c-126">Memoria disponibile è insufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb52c-126">Insufficient memory is available to perform the operation.</span></span> | 
| `S_OK` | <span data-ttu-id="cb52c-127">0</span><span class="sxs-lookup"><span data-stu-id="cb52c-127">0</span></span> | <span data-ttu-id="cb52c-128">La chiamata di funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cb52c-128">The function call was successful.</span></span> | 

## <a name="requirements"></a><span data-ttu-id="cb52c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb52c-129">Requirements</span></span>  
 <span data-ttu-id="cb52c-130">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cb52c-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb52c-131">**Intestazione:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="cb52c-131">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="cb52c-132">**Versioni di .NET framework:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="cb52c-132">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb52c-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cb52c-133">See also</span></span>  
[<span data-ttu-id="cb52c-134">WMI e i contatori delle prestazioni (riferimenti alle API non gestite)</span><span class="sxs-lookup"><span data-stu-id="cb52c-134">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)