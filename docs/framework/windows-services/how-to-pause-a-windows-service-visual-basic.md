---
title: 'Procedura: Sospendere un servizio Windows (Visual Basic)'
ms.date: 03/30/2017
dev_langs:
- vb
f1_keywords:
- ServiceController.Pause
helpviewer_keywords:
- Windows Service applications, pausing
- pausing Windows Service applications
ms.assetid: eddb9409-942b-46b6-a2ce-fbd4c65f2790
author: ghogen
ms.openlocfilehash: 8d378aba5ad09a38d24359fda8b50de072c58035
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54612723"
---
# <a name="how-to-pause-a-windows-service-visual-basic"></a>Procedura: Sospendere un servizio Windows (Visual Basic)
Questo esempio usa il componente <xref:System.ServiceProcess.ServiceController> per sospendere l'esecuzione del servizio IIS Admin nel computer locale.  
  
## <a name="example"></a>Esempio  
 [!code-vb[VbRadconService#11](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#11)]  
[!code-vb[VbRadconService#12](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#12)]  
  
 Questo esempio di codice è disponibile anche come frammento di codice IntelliSense. Nello strumento di selezione dei frammenti di codice il frammento si trova in **Sistema operativo Windows > Servizi Windows**. Per altre informazioni, vedere [Code Snippets](/visualstudio/ide/code-snippets) (Frammenti di codice).  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Un riferimento del progetto a System.serviceprocess.dll.  
  
-   Accedere ai membri dello spazio dei nomi <xref:System.ServiceProcess>. Aggiungere un'istruzione `Imports` se i nomi dei membri all'interno del codice non sono specificati in modo completo. Per altre informazioni, vedere [Istruzione Imports (tipo e spazio dei nomi .NET)](~/docs/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).  
  
## <a name="robust-programming"></a>Programmazione efficiente  
 La proprietà <xref:System.ServiceProcess.ServiceController.MachineName%2A> della classe <xref:System.ServiceProcess.ServiceController> è il computer locale per impostazione predefinita. Per fare riferimento a servizi di Windows in un altro computer, modificare la proprietà <xref:System.ServiceProcess.ServiceController.MachineName%2A> impostando il nome di tale computer.  
  
 Le seguenti condizioni possono generare un'eccezione:  
  
-   Il servizio non può essere sospeso. (<xref:System.InvalidOperationException>)  
  
-   Si è verificato un errore durante l'accesso a un'API di sistema. (<xref:System.ComponentModel.Win32Exception>)  
  
## <a name="net-framework-security"></a>Sicurezza di .NET Framework  
 Il controllo dei servizi nel computer può essere limitato usando <xref:System.ServiceProcess.ServiceControllerPermissionAccess> per impostare le autorizzazioni in <xref:System.ServiceProcess.ServiceControllerPermission>.  
  
 L'accesso alle informazioni sul servizio può essere limitato tramite <xref:System.Security.Permissions.PermissionState> per impostare le autorizzazioni in <xref:System.Security.Permissions.SecurityPermission>.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.ServiceProcess.ServiceController>
- <xref:System.ServiceProcess.ServiceControllerStatus>
- <xref:System.ServiceProcess.ServiceController.WaitForStatus%2A>
- [Procedura: Continuare un servizio Windows (Visual Basic)](../../../docs/framework/windows-services/how-to-continue-a-windows-service-visual-basic.md)
