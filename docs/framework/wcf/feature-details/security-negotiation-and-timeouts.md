---
title: Negoziazione di sicurezza e timeout
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: 38dce9bd6587850a5e3327600bb8bc13c48b93e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592614"
---
# <a name="security-negotiation-and-timeouts"></a>Negoziazione di sicurezza e timeout
Quando l'autenticazione client e servizi, Windows Communication Foundation (WCF) supporta una modalità in cui la credenziale del servizio viene negoziata nell'ambito dell'autenticazione. In scenari di questo tipo, può verificarsi uno scambio di autenticazione multifase tra il client e il servizio al fine di propagare la credenziale del servizio al client. La proprietà <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> controlla il tempo di completamento richiesto per tale scambio multifase. Questo timeout viene tuttavia applicato solo se lo scambio impiega effettivamente più tempo di una singola richiesta-risposta. Nel caso in cui la negoziazione venga completata in un singolo round trip, il timeout non viene applicato.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [Procedura: Set un'inclinazione di Clock massima](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
