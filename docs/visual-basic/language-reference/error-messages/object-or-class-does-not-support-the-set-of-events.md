---
title: L'oggetto o la classe non supporta il set di eventi
ms.date: 07/20/2015
f1_keywords:
- vbrID459
ms.assetid: 785df3f3-2aae-4a25-af36-1f9879d4e5fd
ms.openlocfilehash: 82f3acff1730b4b31b0118a46376825c8807e1da
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552151"
---
# <a name="object-or-class-does-not-support-the-set-of-events"></a>L'oggetto o la classe non supporta il set di eventi
Si è provato a usare un `WithEvents` variabile con un componente che non può fungere da un'origine evento per il set specificato di eventi. Ad esempio, si voleva il sink degli eventi di un oggetto, quindi creare un altro oggetto che `Implements` il primo oggetto. Anche se si potrebbe pensare che è possibile effettuare il sink gli eventi dall'oggetto implementato, questo non è sempre il caso. `Implements` implementa solo un'interfaccia per i metodi e proprietà. `WithEvents` non è supportata per privati `UserControls`, perché le informazioni sul tipo necessarie generare il `ObjectEvent` non è disponibile in fase di esecuzione.  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  È possibile effettuare il sink degli eventi per un componente che non sia l'origine eventi.  
  
## <a name="see-also"></a>Vedere anche
- [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)
- [Istruzione Implements](../../../visual-basic/language-reference/statements/implements-statement.md)
