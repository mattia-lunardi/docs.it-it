---
title: Metodo SqlStreamChars.Dispose(Boolean) (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Dispose
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 4e6cfd6d4c04b1a2835b6e34b82c95b564dea588
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/07/2019
ms.locfileid: "55826863"
---
# <a name="sqlstreamcharsdisposeboolean-method"></a>Metodo SqlStreamChars.Dispose(Boolean)

Quando sottoposto a override in una classe derivata, rilascia le risorse usate dal flusso. L'assembly contenente questo metodo ha una relazione di tipo friend SQLAccess. Si tratta per l'uso da SQL Server. Per altri database, usare il meccanismo di hosting fornito da tale database.

```csharp
protected virtual void Dispose (bool disposing);
```

## <a name="parameters"></a>Parametri

`disposing`\
`true` per rilasciare sia le risorse gestite sia quelle non gestite; `false` per rilasciare solo le risorse non gestite.

## <a name="remarks"></a>Note

> [!WARNING]
> Il `SqlStreamChars.Dispose` metodo è privato e non deve essere utilizzato direttamente nel codice.
>
> Microsoft non supporta l'uso di questo campo in un'applicazione di produzione in alcuna circostanza.

## <a name="requirements"></a>Requisiti

**Spazio dei nomi:** <xref:System.Data.SqlTypes>

**Assembly:** System. Data (in System)

**Versioni di .NET framework:** Disponibile dalla 2.0.