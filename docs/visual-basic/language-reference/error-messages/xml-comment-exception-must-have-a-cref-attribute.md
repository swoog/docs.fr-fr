---
title: Exception de commentaire XML doit avoir un &#39;cref&#39; attribut
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: abe9fe0f6216f81fa223fe83a122b580577e1c32
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43404763"
---
# <a name="xml-comment-exception-must-have-a-39cref39-attribute"></a>Exception de commentaire XML doit avoir un &#39;cref&#39; attribut
Le \<exception > balise offre un moyen de documenter les exceptions qui peuvent être levées par une méthode. Requis `cref` attribut désigne le nom d’un membre qui est vérifié par le Générateur de documentation. Si le membre existe, elle est convertie en nom d’élément canonique dans le fichier de documentation.  
  
 **ID d’erreur :** BC42319  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Ajouter le `cref` attribut à l’exception comme suit :  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [\<exception>](../../../visual-basic/language-reference/xmldoc/exception.md)  
 [Guide pratique : créer une documentation XML](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)  
 [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
