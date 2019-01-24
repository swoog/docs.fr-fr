---
title: Propriété par défaut &#39; &lt;nom_propriété1&gt; &#39; est en conflit avec la propriété par défaut &#39; &lt;propertyname2&gt; &#39; dans &#39; &lt;classname&gt; &#39;et devrait donc être déclarée &#39;ombres&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: 3099467fa3c5a162c13c9235fb8d55375953ba3a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521424"
---
# <a name="default-property-39ltpropertyname1gt39-conflicts-with-default-property-39ltpropertyname2gt39-in-39ltclassnamegt39-and-so-should-be-declared-39shadows39"></a>Propriété par défaut &#39; &lt;nom_propriété1&gt; &#39; est en conflit avec la propriété par défaut &#39; &lt;propertyname2&gt; &#39; dans &#39; &lt;classname&gt; &#39;et devrait donc être déclarée &#39;ombres&#39;
Une propriété est déclarée avec le même nom qu’une propriété définie dans la classe de base. Dans ce cas, la propriété de cette classe doit occulter la propriété de classe de base.  
  
 Ce message est un avertissement. `Shadows` est supposé par défaut. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC40007  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Ajouter le `Shadows` mot clé à la déclaration, ou modifiez le nom de la propriété déclarée.  
  
## <a name="see-also"></a>Voir aussi
- [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md)
- [Occultation dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
