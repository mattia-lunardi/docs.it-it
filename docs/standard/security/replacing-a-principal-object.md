---
title: Sostituzione di oggetti Principal
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- principal objects, replacing
- security [.NET Framework], replacing principal objects
- security [.NET Framework], principals
ms.assetid: c323687e-b196-487b-beba-f38f9b3f961b
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d5193756861f407315ec82e4419f1d04495c7dd2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54606033"
---
# <a name="replacing-a-principal-object"></a>Sostituzione di oggetti Principal
Le applicazioni che forniscono servizi di autenticazione devono poter sostituire l'oggetto **Principal** (<xref:System.Security.Principal.IPrincipal>) per un determinato thread. Inoltre, il sistema di sicurezza deve garantire la possibilità di sostituire gli oggetti **Principal** perché un oggetto **Principal** non corretto collegato in modo intenzionalmente dannoso compromette la sicurezza dell'applicazione attestando un identità o un ruolo non true. Quindi alle applicazioni che devono poter sostituire gli oggetti **Principal** deve essere concesso l'oggetto <xref:System.Security.Permissions.SecurityPermission?displayProperty=nameWithType> per il controllo dell'entità. Tenere presente che questa autorizzazione non è necessaria per eseguire controlli di sicurezza basata sui ruoli o per creare oggetti **Principal** .  
  
 L'oggetto **Principal** corrente può essere sostituito eseguendo le attività seguenti:  
  
1.  Creare l'oggetto **Principal** di sostituzione e l'oggetto **Identity** associato.  
  
2.  Associare il nuovo oggetto **Principal** al contesto chiamata.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente illustra come creare un oggetto identità generico e usarlo per impostare l'identità di un thread.  
  
 [!code-csharp[SetCurrentPrincipal#1](../../../samples/snippets/csharp/VS_Snippets_CLR/SetCurrentPrincipal/CS/program.cs#1)]
 [!code-vb[SetCurrentPrincipal#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/SetCurrentPrincipal/VB/program.vb#1)]  
  
## <a name="see-also"></a>Vedere anche

- <xref:System.Security.Permissions.SecurityPermission?displayProperty=nameWithType>
- [Oggetti Principal e Identity](../../../docs/standard/security/principal-and-identity-objects.md)
