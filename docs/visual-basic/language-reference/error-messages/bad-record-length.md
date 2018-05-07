---
title: Longueur d'enregistrement incorrecte
ms.date: 07/20/2015
f1_keywords:
- vbrID59
ms.assetid: 0926a3a4-177b-4452-9b33-d8a01e24cc21
ms.openlocfilehash: b4b311e2eb504c485772091ed126b3beb71729cb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="bad-record-length"></a>Longueur d'enregistrement incorrecte
Cette erreur peut avoir plusieurs causes, dont les suivantes :  
  
-   La longueur d’une variable d’enregistrement spécifiée dans un `FileGet`, `FileGetObject`, `FilePut` ou `FilePutObject` instruction diffère de la longueur spécifiée dans correspondant `FileOpen` instruction.  
  
-   La variable dans un `FilePut` ou `FilePutObject` instruction est ou inclut une chaîne de longueur variable.  
  
-   La variable dans un `FilePut` ou `FilePutObject` est ou inclut un `Variant` type.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que la somme des tailles des variables à longueur fixe dans le type défini par l’utilisateur de définition de type de la variable d’enregistrement est identique à la valeur indiquée dans le `FileOpen` l’instruction `Len` clause.  
  
2.  Si la variable dans un `FilePut` ou `FilePutObject` instruction est ou inclut une chaîne de longueur variable, vérifiez que la chaîne de longueur variable est au moins 2 caractères plus courtes que la longueur d’enregistrement spécifiée dans le `Len` clause de la `FileOpen` instruction.  
  
3.  Si la variable dans un `FilePut` ou `FilePutObject` est ou inclut un `Variant` Assurez-vous que la chaîne de longueur variable est au moins de 4 octets plus court que la longueur d’enregistrement spécifiée dans le `Len` clause de la `FileOpen` instruction.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.FileSystem.FileGet%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.FileGetObject%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.FilePut%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.FilePutObject%2A>
