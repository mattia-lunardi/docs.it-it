---
title: Enumerazioni di debug
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- debugging enumerations [.NET Framework]
- unmanaged enumerations [.NET Framework], debugging
- enumerations [.NET Framework debugging]
ms.assetid: 3af9f584-f1b4-4154-aeaa-8fce7c9f8b50
caps.latest.revision: "27"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c24882f2bd9819043bbc786bd2e5f35129a92744
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="debugging-enumerations"></a><span data-ttu-id="b9433-102">Enumerazioni di debug</span><span class="sxs-lookup"><span data-stu-id="b9433-102">Debugging Enumerations</span></span>
<span data-ttu-id="b9433-103">Questa sezione descrive le enumerazioni non gestite usate dall'API di debug.</span><span class="sxs-lookup"><span data-stu-id="b9433-103">This section describes the unmanaged enumerations that the debugging API uses.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b9433-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b9433-104">In This Section</span></span>  
 [<span data-ttu-id="b9433-105">CLR_DEBUGGING_PROCESS_FLAGS (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-105">CLR_DEBUGGING_PROCESS_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clr-debugging-process-flags-enumeration.md)  
 <span data-ttu-id="b9433-106">Fornisce i valori utilizzati per il [ICLRDebugging:: OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="b9433-106">Provides values that are used by the [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
 [<span data-ttu-id="b9433-107">CLRDataEnumMemoryFlags (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-107">CLRDataEnumMemoryFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdataenummemoryflags-enumeration.md)  
 <span data-ttu-id="b9433-108">Indica le aree di memoria di una chiamata al [ICLRDataEnumMemoryRegions:: EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) deve includere metodo.</span><span class="sxs-lookup"><span data-stu-id="b9433-108">Indicates which memory regions a call to the [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) method should include.</span></span>  
  
 [<span data-ttu-id="b9433-109">COR_PUB_ENUMPROCESS (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-109">COR_PUB_ENUMPROCESS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cor-pub-enumprocess-enumeration.md)  
 <span data-ttu-id="b9433-110">Identifica il tipo di processo da enumerare.</span><span class="sxs-lookup"><span data-stu-id="b9433-110">Identifies the type of process to be enumerated.</span></span>  
  
 [<span data-ttu-id="b9433-111">CorDebugBlockingReason (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-111">CorDebugBlockingReason Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingreason-enumeration.md)  
 <span data-ttu-id="b9433-112">Specifica i motivi che possono causare il blocco di un thread su un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="b9433-112">Specifies the reasons why a thread may become blocked on a given object.</span></span>  
  
 <span data-ttu-id="b9433-113">CorDebugChainReason</span><span class="sxs-lookup"><span data-stu-id="b9433-113">CorDebugChainReason</span></span>  
 <span data-ttu-id="b9433-114">Indica i motivi che determinano l'avvio di una catena di chiamate.</span><span class="sxs-lookup"><span data-stu-id="b9433-114">Indicates the reason or reasons for the initiation of a call chain.</span></span>  
  
 [<span data-ttu-id="b9433-115">Enumerazione CorDebugCodeInvokeKind</span><span class="sxs-lookup"><span data-stu-id="b9433-115">CorDebugCodeInvokeKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugcodeinvokekind-enumeration.md)  
 <span data-ttu-id="b9433-116">Descrive in che modo una funzione esportata richiama il codice gestito.</span><span class="sxs-lookup"><span data-stu-id="b9433-116">Describes how an exported function invokes managed code.</span></span>  
  
 [<span data-ttu-id="b9433-117">Enumerazione CorDebugCodeInvokePurpose</span><span class="sxs-lookup"><span data-stu-id="b9433-117">CorDebugCodeInvokePurpose Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugcodeinvokepurpose-enumeration.md)  
 <span data-ttu-id="b9433-118">Descrive il motivo per cui una funzione esportata chiama il codice gestito.</span><span class="sxs-lookup"><span data-stu-id="b9433-118">Describes why an exported function calls managed code.</span></span>  
  
 <span data-ttu-id="b9433-119">CorDebugCreateProcessFlags</span><span class="sxs-lookup"><span data-stu-id="b9433-119">CorDebugCreateProcessFlags</span></span>  
 <span data-ttu-id="b9433-120">Fornisce opzioni di debug aggiuntive che possono essere utilizzate in una chiamata al [ICorDebug:: CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="b9433-120">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
 [<span data-ttu-id="b9433-121">Enumerazione CorDebugDebugEventKind</span><span class="sxs-lookup"><span data-stu-id="b9433-121">CorDebugDebugEventKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md)  
 <span data-ttu-id="b9433-122">Indica il tipo di evento le cui informazioni sono decodificate dal [DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="b9433-122">Indicates the type of event whose information is decoded by the [DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) method.</span></span>  
  
 [<span data-ttu-id="b9433-123">Enumerazione CorDebugDecodeEventFlagsWindows</span><span class="sxs-lookup"><span data-stu-id="b9433-123">CorDebugDecodeEventFlagsWindows Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugdecodeeventflagswindows-enumeration.md)  
 <span data-ttu-id="b9433-124">Fornisce altre informazioni sugli eventi di debug nella piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="b9433-124">Provides additional information about debug events on the Windows platform.</span></span>  
  
 <span data-ttu-id="b9433-125">CorDebugExceptionCallbackType</span><span class="sxs-lookup"><span data-stu-id="b9433-125">CorDebugExceptionCallbackType</span></span>  
 <span data-ttu-id="b9433-126">Indica il tipo di callback che viene eseguita da un [ICorDebugManagedCallback2:: Exception](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md) evento.</span><span class="sxs-lookup"><span data-stu-id="b9433-126">Indicates the type of callback that is made from an [ICorDebugManagedCallback2::Exception](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md) event.</span></span>  
  
 [<span data-ttu-id="b9433-127">CorDebugExceptionFlags (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-127">CorDebugExceptionFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionflags-enumeration.md)  
 <span data-ttu-id="b9433-128">Offre informazioni aggiuntive su un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="b9433-128">Provides additional information about an exception.</span></span>  
  
 <span data-ttu-id="b9433-129">CorDebugExceptionUnwindCallbackType</span><span class="sxs-lookup"><span data-stu-id="b9433-129">CorDebugExceptionUnwindCallbackType</span></span>  
 <span data-ttu-id="b9433-130">Indica l'evento segnalato dal callback durante la fase di rimozione.</span><span class="sxs-lookup"><span data-stu-id="b9433-130">Indicates the event that is being signaled by the callback during the unwind phase.</span></span>  
  
 [<span data-ttu-id="b9433-131">Enumerazione CorDebugGCType</span><span class="sxs-lookup"><span data-stu-id="b9433-131">CorDebugGCType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebuggctype-enumeration.md)  
 <span data-ttu-id="b9433-132">Indica se un Garbage Collector è in esecuzione in una workstation o in un server.</span><span class="sxs-lookup"><span data-stu-id="b9433-132">Indicates whether the garbage collector is running on a workstation or a server.</span></span>  
  
 [<span data-ttu-id="b9433-133">Enumerazione CorDebugGenerationTypes</span><span class="sxs-lookup"><span data-stu-id="b9433-133">CorDebugGenerationTypes Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebuggenerationtypes-enumeration.md)  
 <span data-ttu-id="b9433-134">Specifica la generazione di un'area di memoria nell'heap gestito.</span><span class="sxs-lookup"><span data-stu-id="b9433-134">Specifies the generation of a region of memory on the managed heap.</span></span>  
  
 <span data-ttu-id="b9433-135">CorDebugHandleType</span><span class="sxs-lookup"><span data-stu-id="b9433-135">CorDebugHandleType</span></span>  
 <span data-ttu-id="b9433-136">Indica il tipo di handle.</span><span class="sxs-lookup"><span data-stu-id="b9433-136">Indicates the handle type.</span></span>  
  
 [<span data-ttu-id="b9433-137">Enumerazione CorDebugIlToNativeMappingTypes</span><span class="sxs-lookup"><span data-stu-id="b9433-137">CorDebugIlToNativeMappingTypes Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugiltonativemappingtypes-enumeration.md)  
 <span data-ttu-id="b9433-138">Indica se un intervallo specifico di istruzioni native corrisponde a un'area di codice speciale.</span><span class="sxs-lookup"><span data-stu-id="b9433-138">Indicates whether a particular range of native instructions corresponds to a special code region.</span></span>  
  
 <span data-ttu-id="b9433-139">CorDebugIntercept</span><span class="sxs-lookup"><span data-stu-id="b9433-139">CorDebugIntercept</span></span>  
 <span data-ttu-id="b9433-140">Indica i tipi di codice in cui è possibile eseguire l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="b9433-140">Indicates the types of code that can be stepped into.</span></span>  
  
 [<span data-ttu-id="b9433-141">Enumerazione CorDebugInterfaceVersion</span><span class="sxs-lookup"><span data-stu-id="b9433-141">CorDebugInterfaceVersion Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebuginterfaceversion-enumeration.md)  
 <span data-ttu-id="b9433-142">Specifica una versione di .NET Framework o una versione di .NET Framework in cui è stata introdotta un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b9433-142">Specifies either a version of the .NET Framework, or the version of the .NET Framework in which an interface was introduced.</span></span>  
  
 <span data-ttu-id="b9433-143">CorDebugInternalFrameType</span><span class="sxs-lookup"><span data-stu-id="b9433-143">CorDebugInternalFrameType</span></span>  
 <span data-ttu-id="b9433-144">Identifica il tipo di stack frame.</span><span class="sxs-lookup"><span data-stu-id="b9433-144">Identifies the type of stack frame.</span></span>  
  
 [<span data-ttu-id="b9433-145">Enumerazione CorDebugJITCompilerFlags</span><span class="sxs-lookup"><span data-stu-id="b9433-145">CorDebugJITCompilerFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md)  
 <span data-ttu-id="b9433-146">Contiene valori che influenzano il comportamento del compilatore JIT gestito.</span><span class="sxs-lookup"><span data-stu-id="b9433-146">Contains values that influence the behavior of the managed just-in-time (JIT) compiler.</span></span>  
  
 [<span data-ttu-id="b9433-147">CorDebugJITCompilerFlagsDeprecated (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-147">CorDebugJITCompilerFlagsDeprecated Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflagsdeprecated-enumeration.md)  
 <span data-ttu-id="b9433-148">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="b9433-148">Obsolete.</span></span> <span data-ttu-id="b9433-149">Utilizzare il `CORDEBUG_JIT_DEFAULT` appartenente il [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) enumerazione invece.</span><span class="sxs-lookup"><span data-stu-id="b9433-149">Use the `CORDEBUG_JIT_DEFAULT` member of the [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) enumeration instead.</span></span>  
  
 <span data-ttu-id="b9433-150">CorDebugMappingResult</span><span class="sxs-lookup"><span data-stu-id="b9433-150">CorDebugMappingResult</span></span>  
 <span data-ttu-id="b9433-151">Fornisce informazioni su come è stato ottenuto il valore del puntatore dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="b9433-151">Provides the details of how the value of the instruction pointer (IP) was obtained.</span></span>  
  
 [<span data-ttu-id="b9433-152">CorDebugMDAFlags (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-152">CorDebugMDAFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugmdaflags-enumeration.md)  
 <span data-ttu-id="b9433-153">Specifica lo stato del thread su cui è attivato l'assistente al debug gestito.</span><span class="sxs-lookup"><span data-stu-id="b9433-153">Specifies the status of the thread on which the managed debugging assistant (MDA) is fired.</span></span>  
  
 [<span data-ttu-id="b9433-154">Enumerazione CorDebugNGenPolicy</span><span class="sxs-lookup"><span data-stu-id="b9433-154">CorDebugNGenPolicy Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md)  
 <span data-ttu-id="b9433-155">Fornisce un valore che determina se un debugger carica immagini native (NGen) dalla cache delle immagini native.</span><span class="sxs-lookup"><span data-stu-id="b9433-155">Provides a value that determines whether a debugger loads native (NGen) images from the native image cache.</span></span>  
  
 [<span data-ttu-id="b9433-156">Enumerazione CorDebugPlatform</span><span class="sxs-lookup"><span data-stu-id="b9433-156">CorDebugPlatform Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugplatform-enumeration.md)  
 <span data-ttu-id="b9433-157">Fornisce i valori di piattaforma di destinazione vengono utilizzati dal [ICorDebugDataTarget:: GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="b9433-157">Provides target platform values that are used by the [ICorDebugDataTarget::GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) method.</span></span>  
  
 [<span data-ttu-id="b9433-158">Enumerazione CorDebugRecordFormat</span><span class="sxs-lookup"><span data-stu-id="b9433-158">CorDebugRecordFormat Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
 <span data-ttu-id="b9433-159">Descrive il formato dei dati in una matrice di byte che contiene informazioni su un evento di debug per le eccezioni native.</span><span class="sxs-lookup"><span data-stu-id="b9433-159">Describes the format of the data in a byte array that contains information about a native exception debug event.</span></span>  
  
 <span data-ttu-id="b9433-160">CorDebugRegister</span><span class="sxs-lookup"><span data-stu-id="b9433-160">CorDebugRegister</span></span>  
 <span data-ttu-id="b9433-161">Specifica i registri associati a un'architettura di processore specifica.</span><span class="sxs-lookup"><span data-stu-id="b9433-161">Specifies the registers associated with a given processor architecture.</span></span>  
  
 [<span data-ttu-id="b9433-162">Enumerazione CorDebugSetContextFlag</span><span class="sxs-lookup"><span data-stu-id="b9433-162">CorDebugSetContextFlag Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugsetcontextflag-enumeration.md)  
 <span data-ttu-id="b9433-163">Indica se il contesto proviene dal frame attivo (o foglia) sullo stack o se è stato calcolato dalla rimozione da un altro frame.</span><span class="sxs-lookup"><span data-stu-id="b9433-163">Indicates whether the context is from the active (or leaf) frame on the stack or has been computed by unwinding from another frame.</span></span>  
  
 [<span data-ttu-id="b9433-164">Enumerazione CorDebugStateChange</span><span class="sxs-lookup"><span data-stu-id="b9433-164">CorDebugStateChange Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugstatechange-enumeration.md)  
 <span data-ttu-id="b9433-165">Descrive la quantità di dati memorizzati nella cache da rimuovere in base alle modifiche apportate al processo.</span><span class="sxs-lookup"><span data-stu-id="b9433-165">Describes the amount of cached data that must be discarded based on changes to the process.</span></span>  
  
 <span data-ttu-id="b9433-166">CorDebugStepReason</span><span class="sxs-lookup"><span data-stu-id="b9433-166">CorDebugStepReason</span></span>  
 <span data-ttu-id="b9433-167">Indica l'esito di una singola istruzione.</span><span class="sxs-lookup"><span data-stu-id="b9433-167">Indicates the outcome of an individual step.</span></span>  
  
 <span data-ttu-id="b9433-168">CorDebugThreadState</span><span class="sxs-lookup"><span data-stu-id="b9433-168">CorDebugThreadState</span></span>  
 <span data-ttu-id="b9433-169">Specifica lo stato di un thread per il debug.</span><span class="sxs-lookup"><span data-stu-id="b9433-169">Specifies the state of a thread for debugging.</span></span>  
  
 <span data-ttu-id="b9433-170">\>CorDebugUnmappedStop</span><span class="sxs-lookup"><span data-stu-id="b9433-170">\>CorDebugUnmappedStop</span></span>  
 <span data-ttu-id="b9433-171">Specifica il tipo di codice non mappato che può attivare un arresto nell'esecuzione del codice da parte del gestore di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="b9433-171">Specifies the type of unmapped code that can trigger a halt in code execution by the stepper.</span></span>  
  
 <span data-ttu-id="b9433-172">CorDebugUserState</span><span class="sxs-lookup"><span data-stu-id="b9433-172">CorDebugUserState</span></span>  
 <span data-ttu-id="b9433-173">Indica lo stato utente di un thread.</span><span class="sxs-lookup"><span data-stu-id="b9433-173">Indicates the user state of a thread.</span></span>  
  
 [<span data-ttu-id="b9433-174">Enumerazione CorGCReferenceType</span><span class="sxs-lookup"><span data-stu-id="b9433-174">CorGCReferenceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/corgcreferencetype-enumeration.md)  
 <span data-ttu-id="b9433-175">Identifica l'origine di un oggetto per la Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="b9433-175">Identifies the source of an object to be garbage-collected.</span></span>  
  
 [<span data-ttu-id="b9433-176">Enumerazione ILCodeKind</span><span class="sxs-lookup"><span data-stu-id="b9433-176">ILCodeKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/ilcodekind-enumeration.md)  
 <span data-ttu-id="b9433-177">Fornisce valori che specificano se il debugger può accedere a variabili locali o a codice aggiunto nella strumentazione ReJIT del profiler.</span><span class="sxs-lookup"><span data-stu-id="b9433-177">Provides values that specify whether the debugger is able to access local variables or code added in profiler ReJIT instrumentation.</span></span>  
  
 [<span data-ttu-id="b9433-178">LoggingLevelEnum (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-178">LoggingLevelEnum Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/logginglevelenum-enumeration.md)  
 <span data-ttu-id="b9433-179">Indica il livello di gravità di un messaggio descrittivo scritto nel registro eventi quando un thread gestito registra un evento.</span><span class="sxs-lookup"><span data-stu-id="b9433-179">Indicates the severity level of a descriptive message that is written to the event log when a managed thread logs an event.</span></span>  
  
 [<span data-ttu-id="b9433-180">LogSwitchCallReason (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="b9433-180">LogSwitchCallReason Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/logswitchcallreason-enumeration.md)  
 <span data-ttu-id="b9433-181">Indica l'operazione che è stata eseguita su un'opzione di debug/traccia.</span><span class="sxs-lookup"><span data-stu-id="b9433-181">Indicates the operation that was performed on a debugging/tracing switch.</span></span>  
  
 [<span data-ttu-id="b9433-182">Enumerazione VariableLocationType</span><span class="sxs-lookup"><span data-stu-id="b9433-182">VariableLocationType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/variablelocationtype-enumeration.md)  
 <span data-ttu-id="b9433-183">Indica il tipo nativo di percorso di una variabile.</span><span class="sxs-lookup"><span data-stu-id="b9433-183">Indicates the native location type of a variable.</span></span>  
  
 [<span data-ttu-id="b9433-184">Enumerazione WriteableMetadataUpdateMode</span><span class="sxs-lookup"><span data-stu-id="b9433-184">WriteableMetadataUpdateMode Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/writeablemetadataupdatemode-enumeration.md)  
 <span data-ttu-id="b9433-185">Fornisce i valori che specificano se gli aggiornamenti in memoria ai metadati sono visibili a un debugger.</span><span class="sxs-lookup"><span data-stu-id="b9433-185">Provides values that specify whether in-memory updates to metadata are visible to a debugger.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="b9433-186">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="b9433-186">Related Sections</span></span>  
 [<span data-ttu-id="b9433-187">Coclassi di debug</span><span class="sxs-lookup"><span data-stu-id="b9433-187">Debugging Coclasses</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-coclasses.md)  
  
 [<span data-ttu-id="b9433-188">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="b9433-188">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
  
 [<span data-ttu-id="b9433-189">Funzioni statiche globali di debug</span><span class="sxs-lookup"><span data-stu-id="b9433-189">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)  
  
 [<span data-ttu-id="b9433-190">Strutture di debug</span><span class="sxs-lookup"><span data-stu-id="b9433-190">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)