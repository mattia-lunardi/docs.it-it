---
title: Clausola Join (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryJoinIn
- vb.QueryJoin
- vb.QueryJoinOn
helpviewer_keywords:
- queries [Visual Basic], Join
- Join statement [Visual Basic]
- Join clause [Visual Basic]
ms.assetid: 6dd37936-b27c-4e00-98ad-154b23f4de64
ms.openlocfilehash: 2017e8edbb4d1bd25a3669b92553f2905b567594
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514686"
---
# <a name="join-clause-visual-basic"></a>Clausola Join (Visual Basic)
Combina due raccolte in un'unica raccolta. L'operazione di join è basata su chiavi corrispondenti e viene utilizzato il `Equals` operatore.  
  
## <a name="syntax"></a>Sintassi  
  
```  
Join element In collection _  
  [ joinClause _ ]   
  [ groupJoinClause ... _ ]   
On key1 Equals key2 [ And key3 Equals key4 [... ]  
```  
  
## <a name="parts"></a>Parti  
 `element`  
 Obbligatorio. La variabile di controllo per la raccolta da unire in join.  
  
 `collection`  
 Obbligatorio. La raccolta da combinare con l'insieme è identificato nel lato sinistro del `Join` operatore. Oggetto `Join` clausola può essere annidata in un'altra `Join` clausola, o in un `Group Join` clausola.  
  
 `joinClause`  
 Facoltativo. Uno o più altre `Join` clausole per perfezionare la query.  
  
 `groupJoinClause`  
 Facoltativo. Uno o più altre `Group Join` clausole per perfezionare la query.  
  
 `key1` `Equals` `key2`  
 Obbligatorio. Identifica le chiavi per le raccolte da unire in join. È necessario usare il `Equals` operatore per confrontare le chiavi delle raccolte da unire in join. È possibile combinare le condizioni di join tramite il `And` operatore per identificare più chiavi. `key1` deve essere compresa tra la raccolta sul lato sinistro del `Join` operatore. `key2` deve essere compresa tra la raccolta sul lato destro del `Join` operatore.  
  
 Le chiavi usate nella condizione di join possono essere espressioni che includono più di un elemento dalla raccolta. Tuttavia, ogni espressione chiave può contenere solo gli elementi del rispettivo insieme.  
  
## <a name="remarks"></a>Note  
 Il `Join` clausola combina due raccolte in base ai corrispondenti valori di chiave da raccolte da includere. La raccolta risultante può contenere qualsiasi combinazione di valori dalla raccolta identificata nel lato sinistro della `Join` operatore e la raccolta identificata nel `Join` clausola. La query restituirà solo i risultati per il quale la condizione specificata dal `Equals` operatore viene soddisfatta. Ciò equivale a un `INNER JOIN` in SQL.  
  
 È possibile usare più `Join` clausole in una query per unire due o più raccolte in un'unica raccolta.  
  
 È possibile eseguire un join implicito per combinare raccolte senza il `Join` clausola. A tale scopo, includere più `In` clausole nel `From` clausola e specificare un `Where` clausola che identifica le chiavi che si desidera utilizzare per il join.  
  
 È possibile usare il `Group Join` clausola per combinare raccolte in un'unica raccolta gerarchica. Si tratta, ad esempio un `LEFT OUTER JOIN` in SQL.  
  
## <a name="example"></a>Esempio  
 Esempio di codice seguente esegue un join implicito per combinare un elenco di clienti con i relativi ordini.  
  
 [!code-vb[VbSimpleQuerySamples#13](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/join-clause_1.vb)]  
  
## <a name="example"></a>Esempio  
 Esempio di codice seguente unisce due raccolte mediante il `Join` clausola.  
  
 [!code-vb[VbSimpleQuerySamples#12](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/join-clause_2.vb)]  
  
 In questo esempio viene prodotto un output simile al seguente:  
  
 `winlogon (968), Windows Logon`  
  
 `explorer (2424), File Explorer`  
  
 `cmd (5136), Command Window`  
  
## <a name="example"></a>Esempio  
 Esempio di codice seguente unisce due raccolte mediante il `Join` clausola con due colonne chiave.  
  
 [!code-vb[VbSimpleQuerySamples#17](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/join-clause_3.vb)]  
  
 Nell'esempio viene prodotto un output simile al seguente:  
  
 `winlogon (968), Windows Logon, Priority = 13`  
  
 `cmd (700), Command Window, Priority = 8`  
  
 `explorer (2424), File Explorer, Priority = 8`  
  
## <a name="see-also"></a>Vedere anche
- [Introduzione a LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Query](../../../visual-basic/language-reference/queries/index.md)
- [Clausola Select](../../../visual-basic/language-reference/queries/select-clause.md)
- [Clausola From](../../../visual-basic/language-reference/queries/from-clause.md)
- [Clausola Group Join](../../../visual-basic/language-reference/queries/group-join-clause.md)
- [Clausola Where](../../../visual-basic/language-reference/queries/where-clause.md)
