---
title: Cenni preliminari sul controllo NumericUpDown (Windows Form)
ms.date: 03/30/2017
f1_keywords:
- NumericUpDown
helpviewer_keywords:
- numeric spin button control [Windows Forms], Windows Forms
- NumericUpDown control [Windows Forms], about NumericUpDown control
- spin button control [Windows Forms], Windows Forms
ms.assetid: cff3cf30-4d46-4381-87df-37bfe83c71c5
ms.openlocfilehash: 95fab00555231f7605e9104e8264f88b0909785a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671434"
---
# <a name="numericupdown-control-overview-windows-forms"></a>Cenni preliminari sul controllo NumericUpDown (Windows Form)
Il <xref:System.Windows.Forms.NumericUpDown> controllo è simile a una combinazione di una casella di testo e una coppia di frecce su cui l'utente può fare clic per modificare un valore. Il controllo Visualizza e imposta un valore numerico singolo da un elenco di scelte fisse di valori numerici. L'utente può aumentare e ridurre il numero facendo clic sulla freccia e freccia giù, premendo i tasti di direzione su e giù oppure digitando un numero nella casella di testo inclusa del controllo. Facendo clic su freccia su Sposta il numero verso il valore massimo; scegliendo il tasto freccia giù sposta il numero o minimo.  
  
 A causa delle relative funzionalità versatile, questo controllo è una scelta ovvia, ad esempio, se si desidera creare un controllo del volume per un'applicazione di lettore musicale. Il <xref:System.Windows.Forms.NumericUpDown> controllo viene usato in molte applicazioni del Pannello di controllo di Windows.  
  
## <a name="key-properties-and-methods"></a>I metodi e proprietà chiave  
 I numeri visualizzati nella casella di testo del controllo possono essere in un'ampia gamma di formati, tra cui esadecimali. Per altre informazioni, vedere [Procedura: Impostare il formato per i Windows Form controllo NumericUpDown](../../../../docs/framework/winforms/controls/how-to-set-the-format-for-the-windows-forms-numericupdown-control.md). Le proprietà principali del controllo sono <xref:System.Windows.Forms.NumericUpDown.Value%2A>, <xref:System.Windows.Forms.NumericUpDown.Maximum%2A> (valore predefinito 100), <xref:System.Windows.Forms.NumericUpDown.Minimum%2A> (valore predefinito: 0), e <xref:System.Windows.Forms.NumericUpDown.Increment%2A> (impostazione predefinita il valore 1). Il <xref:System.Windows.Forms.NumericUpDown.Value%2A> proprietà imposta il numero corrente selezionato nel controllo. Il <xref:System.Windows.Forms.NumericUpDown.Increment%2A> proprietà imposta la quantità che il numero viene modificato da quando l'utente fa clic su una freccia su o freccia giù. Quando lo stato attivo viene spostato fuori dal controllo, qualsiasi valore immesso verrà convalidato rispetto ai valori numerici minimi e massimo. È possibile aumentare la velocità con cui il controllo si sposta tra i numeri, quando l'utente preme continuamente l'alto o verso il basso freccia, con la <xref:System.Windows.Forms.NumericUpDown.Accelerations%2A> proprietà. I metodi principali del controllo sono <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> e <xref:System.Windows.Forms.NumericUpDown.DownButton%2A>.  
  
## <a name="see-also"></a>Vedere anche
- <xref:System.Windows.Forms.NumericUpDown>
- [Controllo NumericUpDown](../../../../docs/framework/winforms/controls/numericupdown-control-windows-forms.md)
- [Procedura: Impostare il formato per il controllo NumericUpDown di Windows Form](../../../../docs/framework/winforms/controls/how-to-set-the-format-for-the-windows-forms-numericupdown-control.md)
- [Controllo TextBox](../../../../docs/framework/winforms/controls/textbox-control-windows-forms.md)
