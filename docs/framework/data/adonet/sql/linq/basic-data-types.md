---
title: Tipi di dati di base
ms.date: 03/30/2017
ms.assetid: eca2c472-9548-4800-bd31-5d8d9f11752b
ms.openlocfilehash: d9c79ae70d860c5e86d4338038b3158ebfba184f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704969"
---
# <a name="basic-data-types"></a>Tipi di dati di base
Poiché le query LINQ to SQL vengono convertite in Transact-SQL prima di essere eseguite in Microsoft SQL Server, in LINQ to SQL è supportata buona parte delle funzionalità predefinite di SQL Server  per i tipi di dati di base.  
  
## <a name="casting"></a>Cast  
 I cast impliciti o espliciti vengono abilitati da un tipo CLR di origine in un tipo CLR di destinazione se è disponibile una conversione valida simile all'interno di SQL Server. Per altre informazioni sul cast CLR, vedere [CType Function](~/docs/visual-basic/language-reference/functions/ctype-function.md) (Visual Basic) e [come](~/docs/csharp/language-reference/keywords/as.md). Dopo la conversione i cast modificano il comportamento delle operazioni eseguite su un'espressione CLR, in modo che corrisponda a quello di altre espressioni CLR di cui viene eseguito naturalmente il mapping al tipo di destinazione. I cast sono inoltre convertibili nel contesto del mapping di ereditarietà. È possibile eseguire il cast degli oggetti in sottotipi dell'entità più specifici, in modo che sia possibile accedere ai dati specifici del sottotipo.  
  
## <a name="equality-operators"></a>Operatori di uguaglianza  
 LINQ to SQL all'interno di query LINQ to SQL supporta i seguenti operatori di uguaglianza sui tipi di dati di base:  
  
-   Uguali e l'operatore di disuguaglianza: Sono supportati gli operatori di uguaglianza e disuguaglianza per numerica <xref:System.Boolean>, <xref:System.DateTime>, e <xref:System.TimeSpan> tipi. Per altre informazioni sugli operatori di Visual Basic `=` e `<>`, vedere [gli operatori di confronto](~/docs/visual-basic/language-reference/operators/comparison-operators.md). Per altre informazioni sui C# operatori di confronto `==` e `!=`, vedere [= = Operator](~/docs/csharp/language-reference/operators/equality-comparison-operator.md) e [! = (operatore)](~/docs/csharp/language-reference/operators/not-equal-operator.md)rispettivamente  
  
-   È l'operatore: Il `IS` operatore ha supporta la conversione quando viene utilizzato il mapping di ereditarietà. È possibile usarlo invece di testare direttamente la colonna del discriminatore per determinare se un oggetto è di un tipo di entità specifico e viene convertito in un controllo nella colonna del discriminatore. Per altre informazioni su Visual Basic e C# è operators, vedere [operatore Is](~/docs/visual-basic/language-reference/operators/is-operator.md) e [viene](~/docs/csharp/language-reference/keywords/is.md).  
  
## <a name="see-also"></a>Vedere anche
- [Mapping del tipo SQL-CLR](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mapping.md)
- [Tipi di dati e funzioni](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
