---
title: -utf8output (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
ms.openlocfilehash: e6bb04364c2f92129993e19c746fd7cb9c18dc8a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648534"
---
# <a name="-utf8output-visual-basic"></a>-utf8output (Visual Basic)
Visualizza l'output del compilatore usando la codifica UTF-8.  
  
## <a name="syntax"></a>Sintassi  
  
```  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a>Argomenti  
 `+` &#124; `-`  
 Facoltativo. Il valore predefinito per questa opzione è `-utf8output-`, ovvero l'output del compilatore non usa la codifica UTF-8. Specificare `-utf8output` equivale a specificare `-utf8output+`.  
  
## <a name="remarks"></a>Note  
 In alcune configurazioni internazionali, output del compilatore non può essere visualizzato correttamente nella console. In questi casi è necessario usare `-utf8output` e reindirizzare l'output del compilatore in un file.  
  
> [!NOTE]
>  Il `-utf8output` opzione non è disponibile all'interno dell'ambiente di sviluppo di Visual Studio, è disponibile solo durante la compilazione dalla riga di comando.  
  
## <a name="example"></a>Esempio  
 Il codice seguente Compila `In.vb` e indica al compilatore di visualizzare l'output utilizzando la codifica UTF-8.  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a>Vedere anche
- [Compilatore della riga di comando di Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Esempi di righe di comando di compilazione](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
