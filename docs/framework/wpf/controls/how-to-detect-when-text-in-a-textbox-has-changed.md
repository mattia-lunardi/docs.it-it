---
title: 'Procedura: Rilevare eventuali modifiche del testo in un oggetto TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TextBox control [WPF], detecting text change
- text change [WPF], detecting
- detecting text change [WPF]
ms.assetid: 1c39ee14-e37f-49fb-a0d1-a9824ca13584
ms.openlocfilehash: 23bf0a88b3dc16491fbd520683385c65a58a7f6a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696555"
---
# <a name="how-to-detect-when-text-in-a-textbox-has-changed"></a>Procedura: Rilevare eventuali modifiche del testo in un oggetto TextBox
In questo esempio illustra un modo per usare la <xref:System.Windows.Controls.Primitives.TextBoxBase.TextChanged> eventi di eseguire un metodo ogni volta che il testo in un <xref:System.Windows.Controls.TextBox> controllo è stato modificato.  
  
 Nella classe code-behind per il [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] che contiene il <xref:System.Windows.Controls.TextBox> controllo che si desidera monitorare le modifiche, inserire un metodo da chiamare ogni volta che il <xref:System.Windows.Controls.Primitives.TextBoxBase.TextChanged> viene generato l'evento.  Questo metodo deve avere una firma che corrisponde a quello previsto dal <xref:System.Windows.Controls.TextChangedEventHandler> delegare.  
  
 Il gestore eventi viene chiamato ogni volta che il contenuto del <xref:System.Windows.Controls.TextBox> controllo vengono modificate, da un utente o a livello di codice.  
  
 **Nota:** Questo evento viene generato quando il <xref:System.Windows.Controls.TextBox> controllo viene creato e popolato inizialmente con il testo.  
  
## <a name="example"></a>Esempio  
 Nel [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] che definisce i <xref:System.Windows.Controls.TextBox> controllare, specificare il <xref:System.Windows.Controls.Primitives.TextBoxBase.TextChanged> attributo con un valore che corrisponde al nome di metodo del gestore eventi.  
  
 [!code-xaml[TextBox_MiscCode#_TextChangedXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textchangedxaml)]  
  
## <a name="example"></a>Esempio  
 Nella classe code-behind per il [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] che contiene il <xref:System.Windows.Controls.TextBox> controllo che si desidera monitorare le modifiche, inserire un metodo da chiamare ogni volta che il <xref:System.Windows.Controls.Primitives.TextBoxBase.TextChanged> viene generato l'evento.  Questo metodo deve avere una firma che corrisponde a quello previsto dal <xref:System.Windows.Controls.TextChangedEventHandler> delegare.  
  
 [!code-csharp[TextBox_MiscCode#_TextChangedEventHandler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textchangedeventhandler)]
 [!code-vb[TextBox_MiscCode#_TextChangedEventHandler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_textchangedeventhandler)]  
  
 Il gestore eventi viene chiamato ogni volta che il contenuto del <xref:System.Windows.Controls.TextBox> controllo vengono modificate, da un utente o a livello di codice.  
  
 **Nota:** Questo evento viene generato quando il <xref:System.Windows.Controls.TextBox> controllo viene creato e popolato inizialmente con il testo.  
  
 Commenti  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Controls.TextChangedEventArgs>
- [Cenni preliminari sulla classe TextBox](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [Cenni preliminari sul controllo RichTextBox](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
