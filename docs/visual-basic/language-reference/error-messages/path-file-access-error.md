---
title: Errore di accesso percorso-File
ms.date: 07/20/2015
f1_keywords:
- vbrID75
ms.assetid: 6ce3a161-7316-46bd-a785-0d50e5414020
ms.openlocfilehash: 53f021faa9e4ae69a71d825ca823e1180421afc6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54522479"
---
# <a name="pathfile-access-error"></a>Errore di accesso al percorso/file
Durante un'operazione di accesso ai file o di accesso al disco del sistema operativo non è stato possibile stabilire una connessione tra il percorso e il nome del file.  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Assicurarsi che la specifica del file è formattata correttamente. Un nome di file può contenere un nome completo (assoluto) o il relativo percorso. Il percorso completo inizia con il nome dell'unità (se il percorso in un'unità diversa) ed elenca il percorso esplicito dalla radice del file. Qualsiasi percorso che non è completo è relativo alla unità corrente e della directory.  
  
2.  Assicurarsi che non si ha provato a salvare un file sostituirà un file di sola lettura esistente. In questo caso, modificare l'attributo di sola lettura del file di destinazione o salvare il file con un nome file diverso.  
  
3.  Assicurarsi che non si ha provato a aprire un file di sola lettura sequenziale `Output` o `Append` modalità. In questo caso, aprire il file in `Input` modalità o modifica l'attributo di sola lettura del file.  
  
4.  Assicurarsi che non si ha provato a modificare un progetto di Visual Basic all'interno di un database o un documento.  
  
## <a name="see-also"></a>Vedere anche
- [Tipi di errore](../../../visual-basic/programming-guide/language-features/error-types.md)
