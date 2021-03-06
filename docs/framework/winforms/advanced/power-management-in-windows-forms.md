---
title: Risparmio energia in Windows Form
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- battery states
- power states
ms.assetid: ad04a801-5682-4d88-92c5-26eb9cdb209a
ms.openlocfilehash: 172472cf9a2e1bc7bb81448dc8793a4eaeb12da4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54546556"
---
# <a name="power-management-in-windows-forms"></a>Risparmio energia in Windows Form
Le applicazioni Windows Forms possono sfruttare la funzionalità di risparmio energia nel sistema operativo Windows. Le applicazioni possono monitorare lo stato di alimentazione di un computer e intervenire quando viene apportata una modifica dello stato. Ad esempio, se l'applicazione è in esecuzione in un computer portatile, voler disabilitare alcune funzionalità dell'applicazione quando rientra carica della batteria del computer in un determinato livello.  
  
 Il [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] fornisce un <xref:Microsoft.Win32.SystemEvents.PowerModeChanged> evento che si verifica ogni volta che viene apportata una modifica dello stato di alimentazione, ad esempio quando un utente sospende o riprende il sistema operativo, o quando lo stato dell'alimentazione CA o lo stato della batteria cambia. Il <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> proprietà del <xref:System.Windows.Forms.SystemInformation> classe può essere usato per eseguire una query per lo stato corrente, come illustrato nell'esempio di codice seguente.  
  
 [!code-csharp[PowerMode#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#1)]
 [!code-vb[PowerMode#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#1)]  
  
 Altre origini oltre al <xref:System.Windows.Forms.BatteryChargeStatus> enumerazioni, le <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> la proprietà contiene le enumerazioni per determinare la capacità della batteria (<xref:System.Windows.Forms.PowerStatus.BatteryFullLifetime%2A>) e percentuale di carica della batteria (<xref:System.Windows.Forms.PowerStatus.BatteryLifePercent%2A>, <xref:System.Windows.Forms.PowerStatus.BatteryLifeRemaining%2A>).  
  
 È possibile usare la <xref:System.Windows.Forms.Application.SetSuspendState%2A> metodo del <xref:System.Windows.Forms.Application> per impostare un computer in modalità di sospensione. Se il `force` argomento è impostato su `false`, il sistema operativo verrà trasmesso un evento a tutte le applicazioni che richiedono l'autorizzazione a sospendere. Se il `disableWakeEvent` argomento è impostato su `true`, il sistema operativo Disabilita tutti gli eventi di riattivazione.  
  
 Esempio di codice seguente viene illustrato come inserire un computer in sospensione.  
  
 [!code-csharp[PowerMode#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#2)]
 [!code-vb[PowerMode#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#2)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:Microsoft.Win32.SystemEvents.PowerModeChanged>
- <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A>
- <xref:System.Windows.Forms.Application.SetSuspendState%2A>
- <xref:Microsoft.Win32.SystemEvents.SessionSwitch>
