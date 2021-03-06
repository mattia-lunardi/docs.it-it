---
title: Attacchi di tipo replay
ms.date: 03/30/2017
ms.assetid: 7a17e040-93cd-4432-81b9-9f62fec78c8f
ms.openlocfilehash: bceaa1bb723144ee4e3b534aa1537acdc7f65fc3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54712077"
---
# <a name="replay-attacks"></a>Attacchi di tipo replay
Oggetto *attacco di tipo replay* si verifica quando un utente malintenzionato copia un flusso di messaggi tra due parti e lo riproduce verso una o più parti. Se l'attacco non viene respinto, i computer colpiti elaborano il flusso come se i messaggi fossero legittimi. Ciò determina una serie di conseguenze negative, ad esempio la creazione di ordini ridondanti di un articolo.  
  
## <a name="bindings-may-be-subject-to-reflection-attacks"></a>Vulnerabilità delle associazioni agli attacchi di tipo reflection  
 *Attacchi di tipo reflection* sono riproduzioni di messaggi a un mittente proveniente dal destinatario della risposta. Lo standard *rilevamento riproduzione* in Windows Communication Foundation (WCF) meccanismo non gestiscono automaticamente questo.  
  
 Attacchi di tipo reflection vengono mitigati per impostazione predefinita perché il modello di servizio WCF aggiunge un ID messaggio firmato ai messaggi di richiesta e richiede un oggetto firmato `relates-to` intestazione nei messaggi di risposta. Risulta di conseguenza impossibile riprodurre il messaggio di richiesta come risposta. Negli scenari che prevedono messaggi affidabili gli attacchi di tipo reflection vengono respinti per i motivi seguenti:  
  
-   Lo schema dei messaggi di creazione di sequenza non corrisponde a quello di creazione di sequenza di risposta.  
  
-   Per le sequenze simplex, i messaggi di sequenza inviati dal client non possono essere riprodotti verso il client stesso in quanto quest'ultimo non è in grado di riconoscere tali messaggi.  
  
-   Per le sequenze duplex, i due ID di sequenza devono essere univoci. Inoltre, ogni intestazione e corpo della sequenza è firmato. Risulta pertanto impossibile riprodurre un messaggio di sequenza in uscita sottoforma di messaggio di sequenza in ingresso.  
  
 Le uniche associazioni vulnerabili agli attacchi di tipo reflection sono quelle in cui non viene applicata la specifica WS-Addressing, ovvero le associazioni personalizzate in cui la funzionalità WS-Addressing è stata disattivata e in cui si utilizza la protezione basata su chiavi simmetriche. Per impostazione predefinita, l'associazione <xref:System.ServiceModel.BasicHttpBinding> non applica la specifica WS-Addressing. Tuttavia, tale associazione presenta una modalità di sicurezza basata su chiavi simmetriche in grado di respingere gli attacchi di questo tipo.  
  
 Affinché le associazioni personalizzate siano in grado di respingere gli attacchi di tipo reflection è necessario richiedere l'utilizzo di intestazioni WS-Addressing oppure evitare di stabilire contesti di sicurezza.  
  
## <a name="web-farm-attacker-replays-request-to-multiple-nodes"></a>Web Farm: Richiesta riproduzioni hacker in più nodi  
 Si consideri il caso di un client che utilizza un servizio implementato in una Web farm. In questo caso un utente malintenzionato può riprodurre una richiesta inviata a un determinato nodo della farm verso un'altro nodo della stessa farm. Inoltre, se un servizio viene riavviato, la cache di riproduzione viene svuotata. Ciò consente a un utente malintenzionato di riprodurre una richiesta. Nota: una cache di riproduzione contiene i valori di firma dei messaggi usati o già visualizzati e impedisce che tali firme vengano utilizzate più di una volta, respingendo in questo modo gli attacchi di tipo replay. Tuttavia, le funzionalità di una cache di riproduzione non vengono estese all'intera Web farm.  
  
 Le prevenzioni includono:  
  
-   Usare una modalità di sicurezza dei messaggi che preveda token del contesto di sicurezza con stato. La funzionalità di conversazione protetta può essere attiva o disattivata. Per altre informazioni, vedere [Procedura: Creare un contesto di sicurezza Token per una sessione protetta](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-context-token-for-a-secure-session.md).  
  
-   Configurare il servizio in modo che utilizzi un meccanismo di sicurezza a livello di trasporto.  
  
## <a name="see-also"></a>Vedere anche
- [Considerazioni sulla sicurezza](../../../../docs/framework/wcf/feature-details/security-considerations-in-wcf.md)
- [Divulgazione di informazioni](../../../../docs/framework/wcf/feature-details/information-disclosure.md)
- [Elevazione dei privilegi](../../../../docs/framework/wcf/feature-details/elevation-of-privilege.md)
- [Negazione del servizio](../../../../docs/framework/wcf/feature-details/denial-of-service.md)
- [Manomissioni](../../../../docs/framework/wcf/feature-details/tampering.md)
- [Scenari non supportati](../../../../docs/framework/wcf/feature-details/unsupported-scenarios.md)
