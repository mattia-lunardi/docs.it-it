---
title: Previsto 'Optional'
ms.date: 07/20/2015
f1_keywords:
- bc30202
- vbc30202
helpviewer_keywords:
- BC30202
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
ms.openlocfilehash: 0ad0d0890b73103a0678b13409a24190329d37d4
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266331"
---
# <a name="optional-expected"></a>Previsto 'Optional'
Un argomento facoltativo in una dichiarazione di routine è seguito da un argomento obbligatorio. Ogni argomento dopo un argomento facoltativo deve anche essere facoltativo.  
  
 **ID errore:** BC30202  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Se l'argomento è destinato a essere necessari, spostarlo in modo che preceda il primo argomento facoltativo nell'elenco di argomenti.  
  
2.  Se l'argomento è destinato a essere facoltativi, usare il `Optional` (parola chiave).  
  
## <a name="see-also"></a>Vedere anche
- [Parametri facoltativi](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)
