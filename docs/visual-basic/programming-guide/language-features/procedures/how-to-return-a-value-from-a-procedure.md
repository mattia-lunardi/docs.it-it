---
title: 'Procedura: Restituire un valore da una routine (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], returning from
- procedures [Visual Basic], returning a value
ms.assetid: 4bcc4724-2b4e-4df8-9b4b-16054607f87d
ms.openlocfilehash: 38b0673f5725077eec9253021eec4216e66504a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54615249"
---
# <a name="how-to-return-a-value-from-a-procedure-visual-basic"></a>Procedura: Restituire un valore da una routine (Visual Basic)
Oggetto `Function` routine restituisce un valore al codice chiamante tramite l'esecuzione di un `Return` istruzione o l'individuazione un' `Exit Function` o `End Function` istruzione.  
  
### <a name="to-return-a-value-using-the-return-statement"></a>Per restituire un valore utilizzando l'istruzione Return  
  
1.  Inserire un `Return` istruzione in corrispondenza del punto in cui il completamento di attività della stored procedure.  
  
2.  Seguire il `Return` (parola chiave) con un'espressione che restituisce il valore di cui si desidera venga restituito al codice chiamante.  
  
3.  Una routine può includere più di un'istruzione `Return`.  
  
     Nell'esempio `Function` procedure calcola il lato lungo, ovvero l'ipotenusa di un triangolo rettangolo e lo restituisce al codice chiamante.  
  
     [!code-vb[VbVbcnProcedures#1](./codesnippet/VisualBasic/how-to-return-a-value-from-a-procedure_1.vb)]  
  
     Nell'esempio seguente viene illustrata una tipica chiamata alla `hypotenuse`, che archivia il valore restituito.  
  
     [!code-vb[VbVbcnProcedures#6](./codesnippet/VisualBasic/how-to-return-a-value-from-a-procedure_2.vb)]  
  
### <a name="to-return-a-value-using-exit-function-or-end-function"></a>Per restituire un valore di utilizzo di Exit Function o funzione End  
  
1.  In almeno un punto nel `Function` routine, assegnare un valore al nome della stored procedure.  
  
2.  Quando si esegue un' `Exit Function` o `End Function` istruzione Visual Basic restituisce l'ultimo valore assegnato al nome della stored procedure.  
  
3.  Una routine può includere più di un'istruzione `Exit Function` ed è possibile combinare istruzioni `Return` e `Exit Function` nella stessa routine.  
  
4.  Si può avere un solo `End Function` istruzione in un `Function` procedure.  
  
     Per altre informazioni e un esempio, vedere "Valore di restituire" nella [istruzione Function](../../../../visual-basic/language-reference/statements/function-statement.md).  
  
## <a name="see-also"></a>Vedere anche
- [Routine](./index.md)
- [Routine Sub](./sub-procedures.md)
- [Routine Property](./property-procedures.md)
- [Routine di operatore](./operator-procedures.md)
- [Parametri e argomenti delle routine](./procedure-parameters-and-arguments.md)
- [Istruzione Function](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Istruzione Return](../../../../visual-basic/language-reference/statements/return-statement.md)
- [Procedura: Creare una routine che restituisce un valore](./how-to-create-a-procedure-that-returns-a-value.md)
- [Procedura: Chiamare una routine che restituisce un valore](./how-to-call-a-procedure-that-returns-a-value.md)
