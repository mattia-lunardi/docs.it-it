---
title: 'Procedura: Associare un controllo ContextMenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- context menus [Windows Forms], relating
- ContextMenuStrips [Windows Forms], associating with controls
- context menus [Windows Forms], associating with controls
- ContextMenuStrips [Windows Forms], relating
ms.assetid: 6fc40a42-5d69-427f-aa30-0a146193226b
ms.openlocfilehash: 979245291a03b07b7bad548193737c0577b5c107
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221121"
---
# <a name="how-to-associate-a-contextmenustrip-with-a-control"></a>Procedura: Associare un controllo ContextMenuStrip
Dopo avere creato controlli e menu di scelta rapida, attenersi alle procedure riportate di seguito per visualizzare un determinato menu di scelta rapida quando l'utente fa clic sul controllo con il pulsante destro del mouse. Queste procedure consentono di associare un oggetto <xref:System.Windows.Forms.ContextMenuStrip> a un Windows Form e a un controllo <xref:System.Windows.Forms.ToolStrip>.  
  
### <a name="to-associate-a-contextmenustrip-with-a-windows-form"></a>Per associare un oggetto ContextMenuStrip a un Windows Form  
  
1.  Impostare la proprietà <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> sul nome del controllo <xref:System.Windows.Forms.ContextMenuStrip> associato.  
  
### <a name="to-associate-a-contextmenustrip-with-a-toolstrip-control"></a>Per associare un oggetto ContextMenuStrip a un controllo ToolStrip  
  
1.  Impostare la proprietà <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> del controllo sul nome del controllo <xref:System.Windows.Forms.ContextMenuStrip> associato.  
  
## <a name="example"></a>Esempio  
 Nell'esempio di codice seguente vengono creati un Windows Form e un controllo <xref:System.Windows.Forms.ToolStrip> e a ciascuno di essi viene associato un controllo <xref:System.Windows.Forms.ContextMenuStrip> diverso.  
  
 [!code-csharp[System.Windows.Forms.ContextMenuStrip#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ContextMenuStrip/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ContextMenuStrip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ContextMenuStrip/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Riferimenti agli assembly System, System.Data, System.Drawing e System.Windows.Forms.  
  
 Per informazioni sulla compilazione di questo esempio dalla riga di comando per Visual Basic o Visual c#, vedere [compilazione dalla riga di comando](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oppure [con la creazione della riga di comando csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). È anche possibile compilare questo esempio in Visual Studio incollando il codice in un nuovo progetto.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.Control.ContextMenuStrip%2A>
- <xref:System.Windows.Forms.ToolStrip>
- [Procedura: Aggiungere le voci di Menu a un controllo ContextMenuStrip](../../../../docs/framework/winforms/controls/how-to-add-menu-items-to-a-contextmenustrip.md)
- [Controllo ContextMenuStrip](../../../../docs/framework/winforms/controls/contextmenustrip-control.md)
