---
title: Mode de fichier incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID54
ms.assetid: 74891e96-884b-4c8d-872d-cd11ae272372
ms.openlocfilehash: d3d0ebd003f178567ec9e9b19d6baccb8bc15f60
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819981"
---
# <a name="bad-file-mode"></a>Mode de fichier incorrect
Les instructions utilisées pour la manipulation du contenu du fichier doivent être adaptées à la mode dans lequel le fichier a été ouvert. Plusieurs causes sont possibles :  
  
-   Un `FilePutObject` ou `FileGetObject` instruction spécifie un fichier séquentiel.  
  
-   Un `Print` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Output` ou `Append`.  
  
-   Un `Input` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Input`  
  
-   Une tentative d’écriture dans un fichier en lecture seule.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Assurez-vous que `FilePutObject` et `FileGetObject` font uniquement référence à des fichiers ouverts pour `Random` ou `Binary` accès.  
  
-   Assurez-vous que `Print` spécifie un fichier ouvert pour un `Output` ou `Append` mode d’accès. Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.  
  
-   Assurez-vous que `Input` spécifie un fichier ouvert pour `Input`. Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.  
  
-   Si vous écrivez dans un fichier en lecture seule, modifier l’état de lecture/écriture du fichier ou n’essayez pas d’y écrire.  
  
-   Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.FileSystem>
- [Résolution des problèmes : lecture et écriture dans des fichiers texte](../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
