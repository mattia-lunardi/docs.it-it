---
title: <include> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- include XML tag
- <include> XML tag
ms.assetid: ba8e9173-82cd-460b-8938-a075a2dfb36d
ms.openlocfilehash: ea14cc8182b8917a0805fbc509a0000c6df67462
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267040"
---
# <a name="include-visual-basic"></a>\<include> (Visual Basic)
Fa riferimento a un altro file che descrive i tipi e membri nel codice sorgente.  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<include file="filename" path="tagpath[@name='id']" />  
```  
  
#### <a name="parameters"></a>Parametri  
 `filename`  
 Obbligatorio. Nome del file che contiene la documentazione. È possibile qualificare il nome del file con un percorso. Racchiudere `filename` tra virgolette doppie ("").  
  
 `tagpath`  
 Obbligatorio. Percorso dei tag di `filename` che porta al `name` del tag. Racchiudere il percorso tra virgolette doppie ("").  
  
 `name`  
 Obbligatorio. L'identificatore di nome nel tag che precede i commenti. `Name` sarà necessario un `id`.  
  
 `id`  
 Obbligatorio. ID del tag che precede i commenti. Racchiudere l'ID tra virgolette singole (' ').  
  
## <a name="remarks"></a>Note  
 Usare il `<include>` tag per fare riferimento ai commenti in un altro file che descrivono i tipi e membri nel codice sorgente. eliminando la necessità di inserire i commenti relativi alla documentazione direttamente nel file del codice sorgente.  
  
 Il `<include>` tag Usa la raccomandazione di W3C XML Path Language (XPath) Version 1.0. Per altre informazioni sui modi per personalizzare il `<include>` usare, vedere <https://www.w3.org/TR/xpath>.  
  
## <a name="example"></a>Esempio  
 Questo esempio Usa la `<include>` tag per importare i commenti della documentazione membro da un file denominato `commentFile.xml`.  
  
 [!code-vb[VbVbcnXmlDocComments#4](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/include_1.vb)]  
  
 Il formato del `commentFile.xml` è come indicato di seguito.  
  
```xml  
<Docs>  
<Members name="Open">  
<summary>Opens a file.</summary>  
<param name="filename">File name to open.</param>  
</Members>  
<Members name="Close">  
<summary>Closes a file.</summary>  
<param name="filename">File name to close.</param>  
</Members>  
</Docs>  
```  
  
## <a name="see-also"></a>Vedere anche
- [Tag di commento XML](../../../visual-basic/language-reference/xmldoc/index.md)
