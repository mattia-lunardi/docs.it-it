---
title: 'Procedura: Recuperare dati in un formato dati particolare'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], retrieving data
- DataFormats class [WPF], retrieving data
- DataObject class [WPF], retrieving data
ms.assetid: a625acf3-1144-44cd-add7-456aefc3859f
ms.openlocfilehash: d11374cbc70210e648e93a385c4a9fbca112c09f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718295"
---
# <a name="how-to-retrieve-data-in-a-particular-data-format"></a>Procedura: Recuperare dati in un formato dati particolare
Negli esempi seguenti mostrano come recuperare i dati da un oggetto dati in un formato specificato.  
  
## <a name="example"></a>Esempio  
  
### <a name="description"></a>Descrizione  
 Il codice di esempio seguente usa il <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> overload per prima cosa controllare se i dati specificati di formato è disponibile (in modo nativo o tramite conversione automatica); se il formato specificato è disponibile, l'esempio recupera i dati utilizzando il <xref:System.Windows.DataObject.GetData%28System.String%29> (metodo).  
  
### <a name="code"></a>Codice  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat)]  
  
## <a name="example"></a>Esempio  
  
### <a name="description"></a>Descrizione  
 Il codice di esempio seguente usa il <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> overload prima di tutto verificare se un formato dati specificato è disponibile in modo nativo (formati convertibili automaticamente i dati vengono filtrati); se il formato specificato è disponibile, l'esempio recupera i dati usando il <xref:System.Windows.DataObject.GetData%28System.String%29>metodo.  
  
### <a name="code"></a>Codice  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat_native)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat_native)]  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.IDataObject>
- [Cenni preliminari sul trascinamento della selezione](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)
