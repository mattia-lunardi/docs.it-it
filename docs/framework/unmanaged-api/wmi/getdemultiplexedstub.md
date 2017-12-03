---
title: Funzione GetDemultiplexedStub (riferimenti alle API non gestite)
description: La funzione GetDemultiplexedStub crea un oggetto sink di server d'inoltro per facilitare un client riceve le chiamate asincrone dalla gestione di Windows.
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: GetDemultiplexedStub
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: GetDemultiplexedStub
helpviewer_keywords: GetDemultiplexedStub function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a81101acbf65546ea068e6b5a0e8d9045aaadc71
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2017
---
# <a name="getdemultiplexedstub-function"></a><span data-ttu-id="8277b-103">GetDemultiplexedStub (funzione)</span><span class="sxs-lookup"><span data-stu-id="8277b-103">GetDemultiplexedStub function</span></span>
<span data-ttu-id="8277b-104">Crea un oggetto sink di server d'inoltro per facilitare un client riceve le chiamate asincrone dalla gestione di Windows.</span><span class="sxs-lookup"><span data-stu-id="8277b-104">Creates an object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="8277b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8277b-105">Syntax</span></span>  
  
```  
HRESULT GetDemultiplexedStub (
   [in] IUnknown*    pObject, 
   [in] boolean      isLocal, 
   [out] IUnknown**  ppObject
); 
```  

## <a name="parameters"></a><span data-ttu-id="8277b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8277b-106">Parameters</span></span>

`pObject`  
<span data-ttu-id="8277b-107">[in] Un puntatore all'implementazione in-process del client di [IWbemObjectSink](https://msdn.microsoft.com/en-us/library/aa391787(v=vs.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8277b-107">[in] A pointer to the client's in-process implementation of [IWbemObjectSink](https://msdn.microsoft.com/en-us/library/aa391787(v=vs.85).aspx).</span></span>

`isLocal`  
<span data-ttu-id="8277b-108">[in] Un flag che indica se l'evento è locale (`true`); in caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="8277b-108">[in] A flag that indicates whether the event is local (`true`); otherwise, `false`.</span></span>

`ppObject`  
<span data-ttu-id="8277b-109">[out] Un sink di server d'inoltro di oggetto per facilitare un client riceve le chiamate asincrone dalla gestione di Windows.</span><span class="sxs-lookup"><span data-stu-id="8277b-109">[out] A object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>

## <a name="return-value"></a><span data-ttu-id="8277b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8277b-110">Return value</span></span>

<span data-ttu-id="8277b-111">Se la funzione ha esito positivo, il valore restituito è `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="8277b-111">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="8277b-112">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8277b-112">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="8277b-113">Per ottenere informazioni dettagliate sull'errore, chiamare il [GetErrorInfo](geterrorinfo.md) (funzione).</span><span class="sxs-lookup"><span data-stu-id="8277b-113">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
    
## <a name="requirements"></a><span data-ttu-id="8277b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8277b-114">Requirements</span></span>  
 <span data-ttu-id="8277b-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8277b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8277b-116">**Intestazione:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="8277b-116">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="8277b-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8277b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8277b-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8277b-118">See also</span></span>  
[<span data-ttu-id="8277b-119">WMI e i contatori delle prestazioni (riferimenti alle API non gestite)</span><span class="sxs-lookup"><span data-stu-id="8277b-119">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)