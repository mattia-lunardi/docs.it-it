---
title: Creazione ed esecuzione di un'istanza del flusso di lavoro
ms.date: 03/30/2017
ms.assetid: 19d27f47-0491-4569-8f53-51bc1d940e80
ms.openlocfilehash: a86835155417692bc332bf51eb5825ce0b017b04
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527263"
---
# <a name="creating-and-running-a-workflow-instance"></a>Creazione ed esecuzione di un'istanza del flusso di lavoro
In questo esempio viene illustrato come eseguire un'istanza del flusso di lavoro, sia in modo sincrono che asincrono.  
  
## <a name="demonstrates"></a>Dimostrazione  
 <xref:System.Activities.WorkflowInvoker>, <xref:System.Activities.WorkflowApplication>.  
  
## <a name="discussion"></a>Discussione  
 Nella prima parte dell'esempio viene usato <xref:System.Activities.WorkflowInvoker.Invoke%2A>. Si tratta della modalità di base per eseguire un flusso di lavoro. I flussi di lavoro eseguiti con <xref:System.Activities.WorkflowInvoker.Invoke%2A> possono esserlo solo in modo sincrono.  
  
 Nella seconda parte dell'esempio viene usata la classe <xref:System.Activities.WorkflowApplication>. <xref:System.Activities.WorkflowApplication> consente un maggiore controllo su ogni istanza, inclusa la possibilità di interagire con il flusso di lavoro in esecuzione ed eseguirlo in modo asincrono.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare al [Windows Communication Foundation (WCF) e gli esempi di Windows Workflow Foundation (WF) per .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti i Windows Communication Foundation (WCF) e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] esempi. Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\CreatingWorkflowInstances`  
  
## <a name="see-also"></a>Vedere anche
- [Uso di WorkflowInvoker e WorkflowApplication](../../../../docs/framework/windows-workflow-foundation/using-workflowinvoker-and-workflowapplication.md)
