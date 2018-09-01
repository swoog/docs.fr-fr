---
title: '&lt;exemple&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- example XML tag
- <example> XML tag
ms.assetid: 90eeda1c-3fc4-427c-879c-5046d265a97c
ms.openlocfilehash: 2de91d828fd9706b66f4c810486e54e2d3062de0
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43384229"
---
# <a name="ltexamplegt-visual-basic"></a>&lt;exemple&gt; (Visual Basic)
Spécifie un exemple pour le membre.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<example>description</example>  
```  
  
#### <a name="parameters"></a>Paramètres  
 `description`  
 Description de l’exemple de code.  
  
## <a name="remarks"></a>Notes  
 Le `<example>` balise vous permet de spécifier un exemple montrant comment utiliser une méthode ou autres membres de la bibliothèque. Cela implique généralement l’utilisation de la balise [\<code>](../../../visual-basic/language-reference/xmldoc/code.md).  
  
 Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `<example>` balise pour inclure un exemple d’utilisation de la `ID` champ.  
  
 [!code-vb[VbVbcnXmlDocComments#2](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/example_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
