---
title: "Procedura: Ottenere l'indirizzo di una variabile - Guida per programmatori C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- variables [C#], address of
- pointers [C#], & operator
- pointer expressions [C#], address-of operator
ms.assetid: 44fe2cd9-a64f-4ef5-be2a-09ce807c0182
ms.openlocfilehash: cba33803c31ccc144479ad3e7b073ea7057495d5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54490558"
---
# <a name="how-to-obtain-the-address-of-a-variable-c-programming-guide"></a>Procedura: Ottenere l'indirizzo di una variabile (Guida per programmatori C#)

Per ottenere l'indirizzo di un'espressione unaria, che restituisce una variabile fissa, usare l'operatore address-of `&`:  
  
```csharp  
int number;  
int* p = &number; //address-of operator &  
```  
  
 L'operatore address-of può essere applicato solo a una variabile. Se la variabile è spostabile, è possibile usare l'[istruzione fissa](../../../csharp/language-reference/keywords/fixed-statement.md) per fissare temporaneamente la variabile prima di ottenerne l'indirizzo.  
  
 È compito del programmatore garantire che la variabile sia inizializzata. Il compilatore non genera un messaggio di errore se la variabile non è inizializzata.  
  
 Non è possibile ottenere l'indirizzo di una costante o di un valore.  
  
## <a name="example"></a>Esempio  
 In questo esempio viene dichiarato un puntatore a `int`, `p`, e gli viene assegnato l'indirizzo di una variabile di tipo integer, `number`. La variabile `number` viene inizializzata in seguito all'assegnazione a `*p`. Se si imposta l'istruzione di assegnazione come commento, l'inizializzazione della variabile `number` viene rimossa, ma non viene generato alcun errore in fase di compilazione.  

> [!NOTE]
> Compilare questo esempio con l'opzione del compilatore [ `-unsafe` ](../../language-reference/compiler-options/unsafe-compiler-option.md).
  
 [!code-csharp[address-of-a-variable](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#8)]  
  
## <a name="see-also"></a>Vedere anche

- [Guida per programmatori C#](../../../csharp/programming-guide/index.md)
- [Espressioni puntatore](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [Tipi di puntatori](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [Tipi](../../../csharp/language-reference/keywords/types.md)
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)
- [Istruzione fixed](../../../csharp/language-reference/keywords/fixed-statement.md)
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
