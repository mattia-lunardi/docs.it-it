---
title: "'<typename>' non può ereditare da <type> '<basetypename>' perché espande l'accesso del <type> base all'esterno dell'assembly"
ms.date: 07/20/2015
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords:
- BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
ms.openlocfilehash: 226c85f887ecc706a5cb554c2163742f10896141
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269822"
---
# <a name="typename-cannot-inherit-from-type-basetypename-because-it-expands-the-access-of-the-base-type-outside-the-assembly"></a>'\<nomeTipo >' non può ereditare \<tipo > '\<nomeTipoBase >' perché espande l'accesso della base \<tipo > all'esterno dell'assembly
Una classe o interfaccia eredita da una classe di base o interfaccia ma ha un livello di accesso meno restrittivo.  
  
 Ad esempio, un `Public` interfaccia eredita da un `Friend` interfaccia o una `Protected` classe eredita da un `Private` classe. Ciò espone la classe di base o l'interfaccia per accedere a oltre il livello desiderato.  
  
 **ID errore:** BC30910  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Modificare il livello di accesso della classe derivata o dell'interfaccia sia restrittiva almeno quanto quella della classe di base o dell'interfaccia.  
  
     -oppure-  
  
-   Se è necessario il livello di accesso meno restrittivo, rimuovere il `Inherits` istruzione. È possibile ereditare da una classe di base con maggiori restrizioni o un'interfaccia.  
  
## <a name="see-also"></a>Vedere anche
- [Istruzione Class](../../../visual-basic/language-reference/statements/class-statement.md)
- [Istruzione Interface](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Istruzione Inherits](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [Livelli di accesso in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
