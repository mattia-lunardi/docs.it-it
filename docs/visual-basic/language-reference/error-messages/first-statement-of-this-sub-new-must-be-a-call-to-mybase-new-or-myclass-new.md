---
title: La prima istruzione di questo 'Sub New' deve essere una chiamata a 'MyBase.New' o a 'MyClass.New' (nessun costruttore accessibile senza parametri)
ms.date: 07/20/2015
f1_keywords:
- bc30148
- vbc30148
helpviewer_keywords:
- BC30148
ms.assetid: 4426e8fc-cb39-4eb8-ba95-503cd32fcc89
ms.openlocfilehash: d29d7609f8f3f38eadda9a9c763f3ba8e6b99e61
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278538"
---
# <a name="first-statement-of-this-sub-new-must-be-a-call-to-mybasenew-or-myclassnew-no-accessible-constructor-without-parameters"></a>La prima istruzione di questo 'Sub New' deve essere una chiamata a 'MyBase.New' o a 'MyClass.New' (nessun costruttore accessibile senza parametri)
La prima istruzione di questo 'Sub New' deve essere una chiamata a 'MyBase. New' o 'MyClass. New' perché classe di base\<basename >' di '\<derivedname >' è privo di un 'Sub New' accessibile che può essere chiamato senza argomenti.  
  
 In una classe derivata, ogni costruttore deve chiamare un costruttore di classe di base (`MyBase.New`). Se la classe di base ha un costruttore senza parametri accessibile alle classi derivate, `MyBase.New` può essere chiamato automaticamente. In caso contrario, un costruttore di classe di base deve essere chiamato con parametri e questa operazione non può essere eseguita automaticamente. In questo caso, la prima istruzione di ogni costruttore della classe derivata deve chiamare un costruttore con parametri nella classe base o chiamare un altro costruttore nella classe derivata che consente di chiamare un costruttore di classe di base.  
  
 **ID errore:** BC30148  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Chiamare `MyBase.New` specificando i parametri obbligatori o chiamare un costruttore di peer che effettua una chiamata di questo tipo.  
  
     Ad esempio, se la classe di base ha un costruttore che viene dichiarato come `Public Sub New(ByVal index as Integer)`, la prima istruzione in derivato costruttore della classe potrebbe essere `MyBase.New(100)`.  
  
## <a name="see-also"></a>Vedere anche
- [Nozioni fondamentali sull'ereditarietà](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
