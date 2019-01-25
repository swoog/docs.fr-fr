---
title: Erreur de chargement de la DLL (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID48
ms.assetid: 4226cd1f-028c-477d-88a5-cb57f7e0cdc8
ms.openlocfilehash: 76a0a443fd9f8a6dec5ead24bc75c97d89d6c36b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518460"
---
# <a name="error-in-loading-dll-visual-basic"></a>Erreur de chargement de la DLL (Visual Basic)
Une bibliothèque de liens dynamiques (DLL) est une bibliothèque spécifiée dans le `Lib` clause d’une `Declare` instruction. Les causes possibles de cette erreur :  
  
-   Le fichier n’est pas exécutable DLL.  
  
-   Le fichier n’est pas une DLL de Windows de Microsoft.  
  
-   La DLL fait référence à une autre DLL qui n’est pas présente.  
  
-   La DLL ou la DLL référencée n’est pas un répertoire spécifié dans le chemin d’accès.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si le fichier est un fichier texte source et par conséquent pas un exécutable DLL, il doit être compilé et lié à un formulaire exécutable DLL.  
  
-   Si le fichier n’est pas une DLL de Windows de Microsoft, obtenir l’équivalent Microsoft Windows.  
  
-   Si la DLL fait référence à une autre DLL qui n’est pas présente, obtenir la DLL référencée et le rendre disponible.  
  
-   Si la DLL ou la DLL référencée n’est pas un répertoire spécifié par le chemin d’accès, déplacez la DLL vers un répertoire référencé.  
  
## <a name="see-also"></a>Voir aussi
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
