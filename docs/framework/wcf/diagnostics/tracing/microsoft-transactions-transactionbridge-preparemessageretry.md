---
title: Microsoft.Transactions.TransactionBridge.PrepareMessageRetry
ms.date: 03/30/2017
ms.assetid: ada4baa5-b60d-46b8-ad46-4d69f8d8a9fa
ms.openlocfilehash: f168cb24d87f3159a1ea41003c2ffa7041ce8c09
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710443"
---
# <a name="microsofttransactionstransactionbridgepreparemessageretry"></a>Microsoft.Transactions.TransactionBridge.PrepareMessageRetry
Tentativo di invio di un messaggio Prepare a un partecipante che non risponde.  
  
## <a name="description"></a>Descrizione  
 Viene tracciato se il gestore transazioni locale deve inviare nuovamente un messaggio Prepare a un partecipante subordinato poiché non viene ricevuta alcuna risposta entro un determinato periodo di tempo.  
  
## <a name="troubleshooting"></a>Risoluzione dei problemi  
 Esaminare i potenziali problemi della rete o del prodotto che impediscono il recapito della risposta entro il periodo di tempo specificato.  La visualizzazione di numerosi messaggi di questo tipo può indicare problemi dell'infrastruttura o tempi di risposta eccessivamente lunghi. Entrambi i problemi possono ridurre drasticamente la velocità effettiva delle transazioni all'interno del sistema.  
  
## <a name="see-also"></a>Vedere anche
- [Traccia](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Uso delle tracce per risolvere i problemi di un'applicazione](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Amministrazione e diagnostica](../../../../../docs/framework/wcf/diagnostics/index.md)
