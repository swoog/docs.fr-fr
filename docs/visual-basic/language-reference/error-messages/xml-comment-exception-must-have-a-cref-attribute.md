---
title: L'exception de commentaire XML doit avoir un attribut 'cref'
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: a11bfe261ffb8ded95f2e513aaddf00aa00f702e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266635"
---
# <a name="xml-comment-exception-must-have-a-cref-attribute"></a>L'exception de commentaire XML doit avoir un attribut 'cref'
Le \<exception > balise offre un moyen de documenter les exceptions qui peuvent être levées par une méthode. Requis `cref` attribut désigne le nom d’un membre qui est vérifié par le Générateur de documentation. Si le membre existe, elle est convertie en nom d’élément canonique dans le fichier de documentation.  
  
 **ID d’erreur :** BC42319  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Ajouter le `cref` attribut à l’exception comme suit :  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [\<exception>](../../../visual-basic/language-reference/xmldoc/exception.md)
- [Guide pratique pour Créer une Documentation XML](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
