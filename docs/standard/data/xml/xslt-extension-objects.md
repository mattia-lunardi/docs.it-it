---
title: Oggetti di estensione XSLT
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: a4ebdbad-087c-4cfe-acc0-17c48142f81a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ab96d5bdefee0cd85d98174f8f7410e940cb12b4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498372"
---
# <a name="xslt-extension-objects"></a>Oggetti di estensione XSLT
Gli oggetti di estensione vengono usati per estendere la funzionalità dei fogli di stile. Gli oggetti di estensione sono gestiti dalla classe <xref:System.Xml.Xsl.XsltArgumentList>.  
  
 Di seguito sono riportati i vantaggi derivanti dall'utilizzo di un oggetto di estensione anziché di uno script incorporato:  
  
-   Migliore incapsulamento e riutilizzo delle classi.  
  
-   Fogli di stile di dimensioni minori e più gestibili.  
  
 Gli oggetti di estensione XSLT vengono aggiunti all'oggetto <xref:System.Xml.Xsl.XsltArgumentList> usando il metodo <xref:System.Xml.Xsl.XsltArgumentList.AddExtensionObject%2A>. Un nome completo e un URI dello spazio dei nomi sono associati all'oggetto di estensione in quel momento.  
  
> [!NOTE]
>  È richiesto il set di autorizzazioni FullTrust per chiamare il metodo <xref:System.Xml.Xsl.XsltArgumentList.AddExtensionObject%2A>. Per altre informazioni, vedere [Sicurezza dall’accesso di codice](../../../../docs/framework/misc/code-access-security.md) e [NIB: set di autorizzazioni denominati](https://msdn.microsoft.com/library/08250d67-c99d-4ab0-8d2b-b0e12019f6e3).  
  
 Dagli oggetti di estensione vengono restituiti dati appartenenti a uno dei quattro tipi di dati XPath principali, ovvero `number`, `string`, `Boolean` e `node set`.  
  
 I metodi definiti con la parola chiave `params`, che consente di passare un numero non specificato di parametri, non sono supportati dalla classe <xref:System.Xml.Xsl.XslCompiledTransform>. I fogli di stile XSLT in cui sono usati metodi definiti con la parola chiave `params` non funzioneranno correttamente. Per informazioni dettagliate, vedere la sezione [params](~/docs/csharp/language-reference/keywords/params.md).  
  
### <a name="to-use-an-xslt-extension-object"></a>Per usare un oggetto di estensione XSLT  
  
1.  Creare un tipo <xref:System.Xml.Xsl.XsltArgumentList> e aggiungere l'oggetto di estensione usando il metodo <xref:System.Xml.Xsl.XsltArgumentList.AddExtensionObject%2A>.  
  
2.  Chiamare l'oggetto di estensione dal foglio di stile.  
  
3.  Passare l'oggetto <xref:System.Xml.Xsl.XsltArgumentList> al metodo <xref:System.Xml.Xsl.XslCompiledTransform.Transform%2A>.  
  
## <a name="see-also"></a>Vedere anche

- [Trasformazioni XSLT](../../../../docs/standard/data/xml/xslt-transformations.md)
- [Considerazioni sulla sicurezza XSLT](../../../../docs/standard/data/xml/xslt-security-considerations.md)
