---
title: Connessione di contesto
ms.date: 03/30/2017
ms.assetid: e443ca86-9243-4234-a822-ed10a53a9de0
ms.openlocfilehash: 7a2ac8e09b0c108780eb1972d7185ddbfe11b78f
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093996"
---
# <a name="the-context-connection"></a>Connessione di contesto
Il problema dell'accesso ai dati interni è uno scenario abbastanza comune. In altri termini, si desidera accedere allo stesso server sul quale è in esecuzione la propria stored procedure o funzione CLR (Common Language Runtime). Una possibilità consiste nel creare una connessione usando il tipo <xref:System.Data.SqlClient.SqlConnection>, specificare una stringa di connessione che faccia riferimento al server locale, quindi aprire la connessione. A tale scopo è necessario fornire per l'accesso le credenziali appropriate. La connessione si trova infatti in una sessione di database diversa da quella della stored procedure o della funzione, può disporre di opzioni `SET` diverse, si trova in una transazione separata, non rileva le tabelle temporanee e così via. Se la stored procedure gestita o il codice di funzione gestito è in esecuzione nel processo SQL Server, significa che un utente ha effettuato l'accesso a quel server e ha eseguito un'istruzione SQL per richiamare tale stored procedure o funzione. Con tutta probabilità si desidera che la stored procedure o funzione venga eseguita nel contesto di tale connessione, insieme alla relativa transazione, alle relative opzioni `SET` e così via. Questa viene definita connessione di contesto.  
  
 La connessione di contesto consente di eseguire istruzioni Transact-SQL nello stesso contesto in cui il codice era stato richiamato in primo luogo. Per informazioni più dettagliate, vedere la versione della documentazione online di SQL Server corrispondente alla versione di SQL Server in uso.  
  
 **Documentazione online di SQL Server**  
  
1.  [Connessione di contesto](https://go.microsoft.com/fwlink/?LinkId=115395)  
  
## <a name="see-also"></a>Vedere anche
- [Provider gestiti ADO.NET e Centro per sviluppatori di set di dati](https://go.microsoft.com/fwlink/?LinkId=217917)
