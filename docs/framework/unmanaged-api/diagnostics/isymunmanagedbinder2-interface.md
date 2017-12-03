---
title: Interfaccia ISymUnmanagedBinder2
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedBinder2
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedBinder2 Interface
helpviewer_keywords: ISymUnmanagedBinder2 interface [.NET Framework debugging]
ms.assetid: 7a59f405-73e8-4434-8bcc-a9dc45ea08e6
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c276f0abedf4ccab92770af649a8dd0afb6d39d2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="isymunmanagedbinder2-interface"></a><span data-ttu-id="ee621-102">Interfaccia ISymUnmanagedBinder2</span><span class="sxs-lookup"><span data-stu-id="ee621-102">ISymUnmanagedBinder2 Interface</span></span>
<span data-ttu-id="ee621-103">Rappresenta un raccoglitore di simboli per codice non gestito ed estende il [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ee621-103">Represents a symbol binder for unmanaged code, and extends the [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interface.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ee621-104">È un rischio per la sicurezza per aprire un file di programma (PDB) di database da un'origine non attendibile.</span><span class="sxs-lookup"><span data-stu-id="ee621-104">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ee621-105">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee621-105">Methods</span></span>  
  
|<span data-ttu-id="ee621-106">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee621-106">Method</span></span>|<span data-ttu-id="ee621-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee621-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ee621-108">GetReaderForFile2 (metodo)</span><span class="sxs-lookup"><span data-stu-id="ee621-108">GetReaderForFile2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)|<span data-ttu-id="ee621-109">Dato un'interfaccia di metadati e un nome di file, restituisce la corretta <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> interfaccia che verrà letti i simboli di debug associati al modulo.</span><span class="sxs-lookup"><span data-stu-id="ee621-109">Given a metadata interface and a file name, returns the correct <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> interface that will read the debugging symbols associated with the module.</span></span> <span data-ttu-id="ee621-110">Esegue una ricerca più completa rispetto di [ISymUnmanagedBinder::](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="ee621-110">Provides a more extensive search than the [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ee621-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee621-111">Requirements</span></span>  
 <span data-ttu-id="ee621-112">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ee621-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee621-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ee621-113">See Also</span></span>  
 [<span data-ttu-id="ee621-114">Interfacce dell'archivio dei simboli di diagnostica</span><span class="sxs-lookup"><span data-stu-id="ee621-114">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="ee621-115">Interfaccia ISymUnmanagedBinder</span><span class="sxs-lookup"><span data-stu-id="ee621-115">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 [<span data-ttu-id="ee621-116">ISymUnmanagedBinder3 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="ee621-116">ISymUnmanagedBinder3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)