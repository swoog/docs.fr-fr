---
title: Mode de fichier incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID54
ms.assetid: 74891e96-884b-4c8d-872d-cd11ae272372
ms.openlocfilehash: bccbbbeb79f38790a4664b0152ca3378fb55448d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="bad-file-mode"></a>Mode de fichier incorrect
Les instructions utilisées pour la manipulation du contenu du fichier doivent être adaptées au mode dans lequel le fichier a été ouvert. Plusieurs causes sont possibles :  
  
-   A `FilePutObject` ou `FileGetObject` instruction spécifie un fichier séquentiel.  
  
-   A `Print` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Output` ou `Append`.  
  
-   Un `Input` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Input`  
  
-   Toute tentative d’écriture dans un fichier en lecture seule.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Assurez-vous que `FilePutObject` et `FileGetObject` font uniquement référence à des fichiers ouverts pour `Random` ou `Binary` accès.  
  
-   Assurez-vous que `Print` spécifie un fichier ouvert pour un `Output` ou `Append` mode d’accès. Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.  
  
-   Assurez-vous que `Input` spécifie un fichier ouvert pour `Input`. Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.  
  
-   Si vous écrivez dans un fichier en lecture seule, de modifier l’état de lecture/écriture du fichier ou n’essayez pas d’écrire dedans.  
  
-   Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.FileSystem>  
 [Dépannage : lecture et écriture dans des fichiers texte](../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
