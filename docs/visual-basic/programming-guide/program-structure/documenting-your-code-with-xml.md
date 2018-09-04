---
title: Documentation de votre code avec le langage XML (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], documenting code
- XML comments, Visual Basic
- Visual Basic code, documenting with XML
ms.assetid: a0d35dc7-c5f9-4d74-92ff-a1c6f28d5235
ms.openlocfilehash: b99c37f30d595e114bb4625a2881a9f0b463f5e6
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43524405"
---
# <a name="documenting-your-code-with-xml-visual-basic"></a>Documentation de votre code avec le langage XML (Visual Basic)
En Visual Basic, vous pouvez documenter votre code à l’aide de XML  
  
## <a name="xml-documentation-comments"></a>Commentaires de documentation XML  
 Visual Basic fournit un moyen simple pour créer automatiquement la documentation XML pour les projets. Vous pouvez générer automatiquement une structure XML pour vos types et membres et puis fournir des résumés, une documentation descriptive pour chaque paramètre et autres notes. Le programme d’installation approprié, la documentation XML est émise automatiquement dans un fichier XML avec le même nom que votre projet et l’extension .xml. Pour plus d’informations, consultez [/doc](../../../visual-basic/reference/command-line-compiler/doc.md).  
  
 Le fichier XML peut être consommé ou manipulé en tant que XML. Ce fichier se trouve dans le même répertoire que le fichier de sortie .exe ou .dll de votre projet.  
  
 Documentation XML commence par `'''`. Le traitement de ces commentaires présente certaines restrictions :  
  
-   La documentation doit être dans un format XML correct. Si le code XML n’est pas bien formé, un avertissement est généré et le fichier de documentation contient un commentaire indiquant qu’une erreur s’est produite.  
  
-   Les développeurs sont libres de créer leur propre jeu de balises. Il existe un ensemble de recommandée de balises (voir « Sections connexes » dans cette rubrique). Certaines des balises recommandées ont des significations spéciales :  
  
    -   La balise \<param> est utilisée pour décrire les paramètres. Quand elle est utilisée, le compilateur vérifie que le paramètre existe et que tous les paramètres sont décrits dans la documentation. Si la vérification échoue, le compilateur émet un avertissement.  
  
    -   L’attribut `cref` peut être joint à n’importe quelle balise pour fournir une référence à un élément de code. Le compilateur vérifie l’existence de cet élément de code. Si la vérification échoue, le compilateur émet un avertissement. Le compilateur respecte également les `Imports` instructions lorsque vous recherchez un type décrit dans le `cref` attribut.  
  
    -   Le \<Résumé > balise est utilisée par IntelliSense dans Visual Studio pour afficher des informations supplémentaires sur un type ou membre.  
  
## <a name="related-sections"></a>Rubriques connexes  
 Pour plus d’informations sur la création d’un fichier XML avec des commentaires de documentation, consultez les rubriques suivantes :  
  
-   [/doc](../../../visual-basic/reference/command-line-compiler/doc.md)  
  
-   [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)  
  
-   [Traitement du fichier XML](../../../visual-basic/programming-guide/program-structure/processing-the-xml-file.md)  
  
-   [Guide pratique : créer une documentation XML](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)  
  
-   [Outils XML dans Visual Studio](/visualstudio/xml-tools/xml-tools-in-visual-studio)  
  
## <a name="see-also"></a>Voir aussi  
 [Développement d’applications avec Visual Basic](../../../visual-basic/developing-apps/index.md)  
 [Guide de programmation Visual Basic](../../../visual-basic/programming-guide/index.md)
