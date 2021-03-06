---
title: -imports (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- /imports compiler option [Visual Basic]
- imports compiler option [Visual Basic]
- -imports compiler option [Visual Basic]
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
ms.openlocfilehash: 9e5adcce85c4ca4863d28784a7d7f61c441a06c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54588444"
---
# <a name="-imports-visual-basic"></a>-imports (Visual Basic)
Importa gli spazi dei nomi da un assembly specificato.  
  
## <a name="syntax"></a>Sintassi  
  
```  
-imports:namespaceList  
```  
  
## <a name="arguments"></a>Argomenti  
  
|Termine|Definizione|  
|---|---|  
|`namespaceList`|Obbligatorio. Elenco delimitato da virgole degli spazi dei nomi da importare.|  
  
## <a name="remarks"></a>Note  
 Il `-imports` opzione consente di importare spazi dei nomi definiti all'interno del gruppo di file di origine o da qualsiasi assembly di riferimento correnti.  
  
 I membri di uno spazio dei nomi specificati con `-imports` sono disponibili a tutti i file di codice sorgente nella compilazione. Usare la [istruzione Imports (tipo e .NET Namespace)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) usare uno spazio dei nomi in un file del codice sorgente singolo.  
  
|Per impostare/Importa nell'ambiente di sviluppo integrato di Visual Studio|  
|---|  
|1.  Selezionare un progetto in **Esplora soluzioni**. Scegliere **Proprietà** dal menu **Progetto**. <br />2.  Fare clic sulla scheda **Riferimenti**.<br />3.  Immettere il nome dello spazio dei nomi nella casella accanto il **Aggiungi importazione utente** pulsante.<br />4.  Scegliere il **Aggiungi importazione utente** pulsante.|  
  
## <a name="example"></a>Esempio  
 Il codice seguente viene compilato quando `/imports:system.globalization` è specificato. In caso contrario, la compilazione ha esito positivo richiede che un `Imports System.Globalization` istruzione può essere incluso all'inizio del file del codice sorgente o che la proprietà essere qualificato come `System.Globalization.CultureInfo.CurrentCulture.Name`. 
  
 [!code-vb[imports example](codesnippet/VisualBasic/imports_2.vb)]  
  
## <a name="see-also"></a>Vedere anche
- [Compilatore della riga di comando di Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Riferimenti e istruzione Imports](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [Esempi di righe di comando di compilazione](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
