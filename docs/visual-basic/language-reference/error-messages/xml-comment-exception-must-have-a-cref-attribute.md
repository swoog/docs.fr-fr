---
title: L'exception de commentaire XML doit avoir un attribut 'cref'
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: a974df5d2305b88946981d0d258a8088b23d3fc3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58813286"
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
