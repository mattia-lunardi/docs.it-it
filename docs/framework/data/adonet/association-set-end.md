---
title: entità finale del set di associazioni
ms.date: 03/30/2017
ms.assetid: fe4bf1d3-047a-4a37-98c5-a66e70811346
ms.openlocfilehash: 9a71fd434bea87a75e259a3d5caa902fbecf8a57
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701638"
---
# <a name="association-set-end"></a>entità finale del set di associazioni
Un *fine del set di associazioni* identifica le [tipo di entità](../../../../docs/framework/data/adonet/entity-type.md) e il [set di entità](../../../../docs/framework/data/adonet/entity-set.md) alla fine di un [set di associazioni](../../../../docs/framework/data/adonet/association-set.md). Le entità finali del set di associazioni sono definite come parte di un set di associazioni. Un set di associazioni deve disporre esattamente di due entità finali.  
  
 Una definizione di entità finale del set di associazioni contiene le informazioni seguenti:  
  
-   Uno dei tipi di entità coinvolti nel set di associazioni (obbligatorio).  
  
-   Il set di entità per il tipo di entità coinvolto nel set di associazioni (obbligatorio).  
  
## <a name="example"></a>Esempio  
 Nel diagramma seguente viene illustrato un modello concettuale con due associazioni: `WrittenBy` e `PublishedBy`.  
  
 ![Modello di esempio](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 Nel diagramma seguente vengono illustrati un set di associazioni (`PublishedBy`) e due set di entità (`Books` e `Publishers`) basati sul modello concettuale illustrato in precedenza. Le fini del set di associazioni sono i set di entità `Books` e `Publishers`. Business Intelligence nel `Books` set di entità rappresenta un'istanza del `Book` tipo di entità in fase di esecuzione. Analogamente, Pj rappresenta un `Publisher` dell'istanza nel `Publishers` set di entità. BiPj rappresenta un'istanza del `PublishedBy` association nel `PublishedBy` set di associazioni.  
  
 ![Imposta riportato](../../../../docs/framework/data/adonet/media/setsexample.gif "SetsExample")  
  
 Il [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) Usa un linguaggio DSL denominato conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) per definire i modelli concettuali. Il linguaggio CSDL seguente definisce un contenitore di entità con un set di associazioni per ogni associazione nel diagramma precedente. Si noti che le entità finali del set di associazioni sono definite come parte di ogni definizione di set di associazioni.  
  
 [!code-xml[EDM_Example_Model#EntityContainerExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entitycontainerexample)]  
  
## <a name="see-also"></a>Vedere anche
- [Concetti chiave di Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
