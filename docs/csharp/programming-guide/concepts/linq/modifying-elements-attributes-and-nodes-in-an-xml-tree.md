---
title: Modifica di elementi, attributi e nodi in un albero XML
ms.date: 07/20/2015
ms.assetid: 0ed22e4e-4c6b-4eb1-b0eb-06685efd8c33
ms.openlocfilehash: 68195133a944f14f83bf6a33903152393205bfce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54606242"
---
# <a name="modifying-elements-attributes-and-nodes-in-an-xml-tree"></a>Modifica di elementi, attributi e nodi in un albero XML
Nella tabella seguente sono riepilogati i metodi e le proprietà che è possibile usare per modificare un elemento, i relativi elementi figlio o gli attributi.  
  
 I metodi seguenti modificano <xref:System.Xml.Linq.XElement>.  
  
|Metodo|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>|Sostituisce un elemento con XML analizzato.|  
|<xref:System.Xml.Linq.XElement.RemoveAll%2A?displayProperty=nameWithType>|Rimuove tutto il contenuto di un elemento (nodi figlio e attributi).|  
|<xref:System.Xml.Linq.XElement.RemoveAttributes%2A?displayProperty=nameWithType>|Rimuove gli attributi di un elemento.|  
|<xref:System.Xml.Linq.XElement.ReplaceAll%2A?displayProperty=nameWithType>|Sostituisce tutto il contenuto di un elemento (nodi figlio e attributi).|  
|<xref:System.Xml.Linq.XElement.ReplaceAttributes%2A?displayProperty=nameWithType>|Sostituisce gli attributi di un elemento.|  
|<xref:System.Xml.Linq.XElement.SetAttributeValue%2A?displayProperty=nameWithType>|Imposta il valore di un attributo. Crea l'attributo se non esiste. Se il valore è impostato su `null`, rimuove l'attributo.|  
|<xref:System.Xml.Linq.XElement.SetElementValue%2A?displayProperty=nameWithType>|Imposta il valore di un elemento figlio. Crea l'elemento se non esiste. Se il valore è impostato su `null`, rimuove l'elemento.|  
|<xref:System.Xml.Linq.XElement.Value%2A?displayProperty=nameWithType>|Sostituisce il contenuto (nodi figlio) di un elemento con il testo specificato.|  
|<xref:System.Xml.Linq.XElement.SetValue%2A?displayProperty=nameWithType>|Imposta il valore di un elemento.|  
  
 I metodi seguenti modificano <xref:System.Xml.Linq.XAttribute>.  
  
|Metodo|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XAttribute.Value%2A?displayProperty=nameWithType>|Imposta il valore di un attributo.|  
|<xref:System.Xml.Linq.XAttribute.SetValue%2A?displayProperty=nameWithType>|Imposta il valore di un attributo.|  
  
 I metodi seguenti modificano <xref:System.Xml.Linq.XNode> (incluso <xref:System.Xml.Linq.XElement> o <xref:System.Xml.Linq.XDocument>).  
  
|Metodo|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XNode.ReplaceWith%2A?displayProperty=nameWithType>|Sostituisce un nodo con nuovo contenuto.|  
  
 I metodi seguenti modificano <xref:System.Xml.Linq.XContainer> (<xref:System.Xml.Linq.XElement> o <xref:System.Xml.Linq.XDocument>).  
  
|Metodo|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XContainer.ReplaceNodes%2A?displayProperty=nameWithType>|Sostituisce i nodi figlio con nuovo contenuto.|  
  
## <a name="see-also"></a>Vedere anche

- [Modifica degli alberi XML (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/modifying-xml-trees-linq-to-xml.md)
