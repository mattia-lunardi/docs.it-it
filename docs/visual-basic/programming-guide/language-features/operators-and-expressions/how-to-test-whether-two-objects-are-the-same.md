---
title: 'Procedura: Verificare se due oggetti sono la stessa (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], reference
- Is operator [Visual Basic], comparing objects
- reference variables [Visual Basic]
- variables [Visual Basic], referring to same object
- objects [Visual Basic], variables referring to same
- Visual Basic code, operators
ms.assetid: f760e828-8704-4256-bc2d-c22a4c93b524
ms.openlocfilehash: 4130dfbe70682e28b6bb15db633ede2790e20aa3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595552"
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a>Procedura: Verificare se due oggetti sono la stessa (Visual Basic)
Se si dispone di due variabili fanno riferimento agli oggetti, è possibile usare la `Is` o `IsNot` operatore o entrambi, per determinare se si riferiscono alla stessa istanza.  
  
### <a name="to-test-whether-two-objects-are-the-same"></a>Per verificare se due oggetti sono uguali.  
  
-   Usare la [operatore Is](../../../../visual-basic/language-reference/operators/is-operator.md) o nella [operatore IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md) con le due variabili come operandi.  
  
     [!code-vb[VbVbalrOperators#69](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-test-whether-two-objects-are-the-same_1.vb)]  
  
 È possibile eseguire una determinata azione a seconda del fatto che due oggetti si riferiscono alla stessa istanza. Nell'esempio precedente viene confrontato il controllo `c` con il controllo attivo sul form `f`. Se non è disponibile alcun controllo attivo o se è presente uno ma non è la stessa istanza di controllo come `c`, quindi il `If` istruzione ha esito negativo e la procedura restituisce senza ulteriore elaborazione.  
  
 Se si utilizza `Is` o `IsNot` è una questione di praticità aggiuntivo personale all'utente. Uno potrebbe essere più facile da leggere rispetto a altro in una determinata espressione.  
  
## <a name="see-also"></a>Vedere anche
- [Operatori di confronto in Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
