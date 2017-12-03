---
title: Interfaccia IMetaDataConverter
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataConverter
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataConverter
helpviewer_keywords: IMetaDataConverter interface [.NET Framework metadata]
ms.assetid: 9caea662-0167-4267-b14a-2fa42c3be4ea
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: f551a774a860f595cc90a7cca9eee2c726ef50ee
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataconverter-interface"></a><span data-ttu-id="cdb6b-102">Interfaccia IMetaDataConverter</span><span class="sxs-lookup"><span data-stu-id="cdb6b-102">IMetaDataConverter Interface</span></span>
<span data-ttu-id="cdb6b-103">Fornisce metodi per eseguire il mapping delle librerie dei tipi alle relative firme di metadati e per eseguire la conversione da una all'altra.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-103">Provides methods to map type libraries to their metadata signatures, and to convert from one to the other.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cdb6b-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="cdb6b-104">Methods</span></span>  
  
|<span data-ttu-id="cdb6b-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="cdb6b-105">Method</span></span>|<span data-ttu-id="cdb6b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdb6b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cdb6b-107">GetMetaDataFromTypeInfo (metodo)</span><span class="sxs-lookup"><span data-stu-id="cdb6b-107">GetMetaDataFromTypeInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-getmetadatafromtypeinfo-method.md)|<span data-ttu-id="cdb6b-108">Ottiene un puntatore a un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) istanza che rappresenta la firma dei metadati per la libreria dei tipi a cui fa riferimento specificato `ITypeInfo` istanza.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-108">Gets a pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance that represents the metadata signature for the type library referenced by the specified `ITypeInfo` instance.</span></span>|  
|[<span data-ttu-id="cdb6b-109">GetMetaDataFromTypeLib (metodo)</span><span class="sxs-lookup"><span data-stu-id="cdb6b-109">GetMetaDataFromTypeLib Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-getmetadatafromtypelib-method.md)|<span data-ttu-id="cdb6b-110">Ottiene un puntatore a un `IMetaDataImport` istanza che rappresenta la firma dei metadati per la libreria dei tipi rappresentata dall'oggetto `ITypeLib` istanza.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-110">Gets a pointer to an `IMetaDataImport` instance that represents the metadata signature for the type library represented by the specified `ITypeLib` instance.</span></span>|  
|[<span data-ttu-id="cdb6b-111">GetTypeLibFromMetaData (metodo)</span><span class="sxs-lookup"><span data-stu-id="cdb6b-111">GetTypeLibFromMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-gettypelibfrommetadata-method.md)|<span data-ttu-id="cdb6b-112">Ottiene un puntatore a un `ITypeLib` istanza che rappresenta la libreria dei tipi con i nomi di modulo e la libreria specificati.</span><span class="sxs-lookup"><span data-stu-id="cdb6b-112">Gets a pointer to an `ITypeLib` instance that represents the type library that has the specified module and library names.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cdb6b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdb6b-113">Requirements</span></span>  
 <span data-ttu-id="cdb6b-114">**Piattaforma:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cdb6b-114">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cdb6b-115">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="cdb6b-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cdb6b-116">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cdb6b-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cdb6b-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cdb6b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdb6b-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cdb6b-118">See Also</span></span>  
 [<span data-ttu-id="cdb6b-119">Interfacce di metadati</span><span class="sxs-lookup"><span data-stu-id="cdb6b-119">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)  
 [<span data-ttu-id="cdb6b-120">IMetaDataImport (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="cdb6b-120">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)