---
title: System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
ms.date: 03/30/2017
ms.assetid: 7e142e9d-e81b-4309-974a-02e9cc064ea0
ms.openlocfilehash: f41fd08138591a90b6173b5e4806e5ac73ff07da
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662764"
---
# <a name="systemservicemodeltxcompletionstatusabortedonsessionclose"></a>System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
La transazione specificata è stata interrotta perché non era stata completata alla chiusura della sessione e TransactionAutoCompleteOnSessionClose OperationBehaviorAttribute era impostato su False.  
  
## <a name="description"></a>Descrizione  
 Viene tracciato se la sessione attiva corrente è stata chiusa prima del completamento della transazione e se TransactionAutoCompleteOnSessionClose è impostato su `false`.  
  
## <a name="troubleshooting"></a>Risoluzione dei problemi  
 Questa traccia indica un bug potenziale dell'applicazione che deve essere esaminato.  
  
## <a name="see-also"></a>Vedere anche
- [Traccia](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Uso delle tracce per risolvere i problemi di un'applicazione](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Amministrazione e diagnostica](../../../../../docs/framework/wcf/diagnostics/index.md)
