---
title: Un delimitatore non può essere Nothing o una stringa vuota
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_DelimiterNothing
ms.assetid: 8885fcd1-c201-409d-9a32-6ff2b13c0c13
ms.openlocfilehash: 1a99bd1594bd754dd8fcf73ee4e621ed60113867
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737702"
---
# <a name="a-delimiter-cannot-be-nothing-or-an-empty-string"></a>Un delimitatore non può essere Nothing o una stringa vuota
`TextFieldParser` non riesce a leggere i contenuti dal file perché la proprietà `Delimiters` è impostata su `Nothing` o corrisponde a un oggetto `String` vuoto ("").  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Specificare un valore valido per `Delimiters`.  
  
## <a name="see-also"></a>Vedere anche
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters%2A>
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters>
- [Procedura: Leggere file di testo delimitato da virgole](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)
- [Oggetto TextFieldParser](../../visual-basic/language-reference/objects/textfieldparser-object.md)
- [Analisi dei file di testo con l'oggetto TextFieldParser](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
