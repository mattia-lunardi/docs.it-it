---
title: 'Procedura: Combinare delegati multicast - Guida per programmatori C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- delegates [C#], combining
- multicast delegates [C#]
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
ms.openlocfilehash: ebfcba4d2ebebe2697aa01b7109bbf50b8f144e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631555"
---
# <a name="how-to-combine-delegates-multicast-delegatesc-programming-guide"></a>Procedura: Combinare delegati multicast (Guida per programmatori C#)
Questo esempio illustra come creare delegati multicast. Una proprietà utile degli oggetti [delegate](../../../csharp/language-reference/keywords/delegate.md) è la possibilità di assegnare più oggetti a un'istanza di delegato usando l'operatore `+`. Il delegato multicast contiene un elenco dei delegati assegnati. Quando il delegato multicast viene chiamato, richiama i delegati nell'elenco, in ordine. Solo i delegati dello stesso tipo possono essere combinati.  
  
 L'operatore `-` può essere usato per rimuovere un delegato componente da un delegato multicast.  
  
## <a name="example"></a>Esempio  
 [!code-csharp[csProgGuideDelegates#11](../../../csharp/programming-guide/delegates/codesnippet/CSharp/how-to-combine-delegates-multicast-delegates_1.cs)]  
  
## <a name="see-also"></a>Vedere anche

- <xref:System.MulticastDelegate>
- [Guida per programmatori C#](../../../csharp/programming-guide/index.md)
- [Eventi](../../../csharp/programming-guide/events/index.md)
