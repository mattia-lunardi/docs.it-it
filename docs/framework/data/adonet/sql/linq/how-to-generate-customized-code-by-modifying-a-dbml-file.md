---
title: 'Procedura: Generare codice personalizzato modificando un File DBML'
ms.date: 03/30/2017
ms.assetid: 50ad597a-8598-42d3-82dd-fc7d702ebc37
ms.openlocfilehash: b17743f20cf9fcb01cdd39dc7afc3f6b4419ebff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499093"
---
# <a name="how-to-generate-customized-code-by-modifying-a-dbml-file"></a>Procedura: Generare codice personalizzato modificando un File DBML
È possibile generare Visual Basic o C# codice sorgente da un file di metadati di database markup language (con estensione dbml). Questo approccio consente di personalizzare il file DBML predefinito prima di generare il codice di mapping dell'applicazione. Si tratta di una funzionalità avanzata.  
  
 Di seguito sono elencati i passaggi di questo processo.  
  
1.  Generare un file con estensione dbml.  
  
2.  Usare un editor per modificare il file con estensione dbml, Si noti che il file con estensione dbml deve convalidare il file di schema definition (XSD) per [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] i file. dbml. Per altre informazioni, vedere [generazione di codice in LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/code-generation-in-linq-to-sql.md).  
  
3.  Generazione di Visual Basic o C# codice sorgente.  
  
 Negli esempi seguenti viene usato lo strumento della riga di comando SQLMetal. Per altre informazioni, vedere [SqlMetal.exe (strumento per la generazione del codice)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).  
  
## <a name="example"></a>Esempio  
 Nel codice seguente viene generato un file con estensione dbml dal database di esempio Northwind. Come origine per i metadati del database è possibile usare il nome del database o il nome del file con estensione mdf.  
  
```  
sqlmetal /server:myserver /database:northwind /dbml:mymeta.dbml  
sqlmetal /dbml:mymeta.dbml mydbfile.mdf  
```  
  
## <a name="example"></a>Esempio  
 Il codice seguente genera l'errore Visual Basic o C# file del codice sorgente da un file con estensione dbml.  
  
```  
sqlmetal /namespace:nwind /code:nwind.vb /language:vb DBMLFile.dbml  
sqlmetal /namespace:nwind /code:nwind.cs /language:csharp DBMLFile.dbml  
```  
  
## <a name="see-also"></a>Vedere anche
- [Generazione di codice in LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/code-generation-in-linq-to-sql.md)
- [SqlMetal.exe (strumento per la generazione del codice)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md)
- [Creazione del modello a oggetti](../../../../../../docs/framework/data/adonet/sql/linq/creating-the-object-model.md)
