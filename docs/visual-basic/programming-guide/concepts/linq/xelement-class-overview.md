---
title: Panoramica della classe XElement (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 52331fcd-6023-4d19-b423-7b24f2d86ded
ms.openlocfilehash: fe2a91d2b286061453e41870d68c04424417c6ef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628813"
---
# <a name="xelement-class-overview-visual-basic"></a>Panoramica della classe XElement (Visual Basic)
<xref:System.Xml.Linq.XElement> è una delle classi fondamentali di [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]. Rappresenta un elemento XML. Può essere usata per creare elementi, modificare il contenuto dell'elemento, aggiungere, modificare o eliminare elementi figlio, aggiungere attributi a un elemento oppure serializzare il contenuto di un elemento in formato testo. È inoltre possibile definire l'interoperabilità con altre classi di <xref:System.Xml?displayProperty=nameWithType>, ad esempio <xref:System.Xml.XmlReader>, <xref:System.Xml.XmlWriter> e <xref:System.Xml.Xsl.XslCompiledTransform>.  
  
## <a name="xelement-functionality"></a>Funzionalità di XElement  
 In questo argomento viene descritta la funzionalità fornita dalla classe <xref:System.Xml.Linq.XElement>.  
  
### <a name="constructing-xml-trees"></a>Costruzione di alberi XML  
 È possibile costruire alberi XML in diversi modi:  
  
-   È possibile costruire un albero XML nel codice. Per altre informazioni, vedere [creazione di alberi XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/creating-xml-trees.md).  
  
-   È possibile analizzare codice XML di origini diverse, incluso un oggetto <xref:System.IO.TextReader>, file di testo o un indirizzo Web (URL). Per altre informazioni, vedere [analisi XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/parsing-xml.md).  
  
-   È possibile usare un oggetto <xref:System.Xml.XmlReader> per popolare l'albero. Per altre informazioni, vedere <xref:System.Xml.Linq.XNode.ReadFrom%2A>.  
  
-   Se si dispone di un modulo in grado di scrivere contenuto in un oggetto <xref:System.Xml.XmlWriter>, è possibile usare il metodo <xref:System.Xml.Linq.XContainer.CreateWriter%2A> per creare un writer, passare il writer al modulo e quindi usare il contenuto scritto in <xref:System.Xml.XmlWriter> per popolare l'albero XML.  
  
 Tuttavia, il modo più comune per creare un albero XML è il seguente:  
  
```vb  
Dim contacts As XElement = _  
    <Contacts>  
        <Contact>  
            <Name>Patrick Hines</Name>  
            <Phone>206-555-0144</Phone>  
            <Address>  
                <Street1>123 Main St</Street1>  
                <City>Mercer Island</City>  
                <State>WA</State>  
                <Postal>68042</Postal>  
            </Address>  
        </Contact>  
    </Contacts>  
```  
  
 Un'altra tecnica molto comune per la creazione di un albero XML implica l'uso dei risultati di una query [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] per popolare un albero XML, come illustrato nell'esempio seguente:  
  
```vb  
Dim srcTree As XElement = _  
    <Root>  
        <Element>1</Element>  
        <Element>2</Element>  
        <Element>3</Element>  
        <Element>4</Element>  
        <Element>5</Element>  
    </Root>  
Dim xmlTree As XElement = _  
    <Root>  
        <Child>1</Child>  
        <Child>2</Child>  
        <%= From el In srcTree.Elements() _  
            Where el.Value > 2 _  
            Select el %>  
    </Root>  
Console.WriteLine(xmlTree)  
```  
  
 Questo esempio produce il seguente output:  
  
```xml  
<Root>  
  <Child>1</Child>  
  <Child>2</Child>  
  <Element>3</Element>  
  <Element>4</Element>  
  <Element>5</Element>  
</Root>  
```  
  
### <a name="serializing-xml-trees"></a>Serializzazione di strutture ad albero XML  
 È possibile serializzare l'albero XML in un oggetto <xref:System.IO.File>, <xref:System.IO.TextWriter> o <xref:System.Xml.XmlWriter>.  
  
 Per altre informazioni, vedere [serializzazione di alberi XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/serializing-xml-trees.md).  
  
### <a name="retrieving-xml-data-via-axis-methods"></a>Recupero di dati XML tramite metodi dell'asse  
 È possibile usare metodi dell'asse per recuperare attributi, elementi figlio, elementi discendenti ed elementi predecessori. Le query [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] vengono eseguite sui metodi dell'asse e forniscono numerose funzionalità flessibili e potenti per spostarsi in un albero XML ed elaborarla.  
  
 Per altre informazioni, vedere [assi LINQ to XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md).  
  
### <a name="querying-xml-trees"></a>Esecuzione di query su strutture ad albero XML  
 È possibile scrivere query [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] per estrarre dati da un albero XML.  
  
 Per altre informazioni, vedere [esecuzione di query su strutture ad albero XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/querying-xml-trees.md).  
  
### <a name="modifying-xml-trees"></a>Modifica di strutture ad albero XML  
 È possibile modificare un elemento in modi diversi, ad esempio modificandone il contenuto o gli attributi. È inoltre possibile rimuovere un elemento dal relativo elemento padre.  
  
 Per altre informazioni, vedere [modifica di alberi XML (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/modifying-xml-trees-linq-to-xml.md).  
  
## <a name="see-also"></a>Vedere anche
- [LINQ to XML Panoramica della programmazione (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-programming-overview.md)
