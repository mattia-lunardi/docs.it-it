---
title: '- (Negative) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 208e54ef-4741-4ec5-89d6-6ff700863cb0
ms.openlocfilehash: f33b672ecd635234b8a8859651d117aabdaf14d5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745853"
---
# <a name="--negative-entity-sql"></a>- (negativo) (Entity SQL)
Restituisce il corrispondente negativo del valore di un'espressione numerica.  
  
## <a name="syntax"></a>Sintassi  
  
```  
- expression  
```  
  
## <a name="arguments"></a>Argomenti  
 `expression`  
 Qualsiasi espressione valida con qualsiasi tipo di dati numerici.  
  
## <a name="result-types"></a>Tipi di risultati  
 Tipo di dati di `expression`.  
  
## <a name="remarks"></a>Note  
 Se `expression` è un tipo senza segno, il tipo di risultato sarà il tipo con segno più strettamente correlato al tipo di `expression`. Se, ad esempio, `expression` è di tipo Byte, verrà restituito un valore di tipo Int16.  
  
## <a name="example"></a>Esempio  
 Nella query Entity SQL seguente viene usato l'operatore aritmetico - per restituire il corrispondente negativo del valore di un'espressione numerica. La query è basata sul modello Sales di AdventureWorks. Per compilare ed eseguire questa query, effettuare le operazioni seguenti:  
  
1.  Attenersi alla procedura di [come: Eseguire una Query che restituisce risultati StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :  
  
 [!code-csharp[DP EntityServices Concepts 2#NEGATIVE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#negative)]  
  
## <a name="see-also"></a>Vedere anche
- [Riferimento a Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
