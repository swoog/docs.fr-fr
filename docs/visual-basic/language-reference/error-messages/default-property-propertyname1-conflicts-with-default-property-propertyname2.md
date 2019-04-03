---
title: La propriété par défaut '<propertyname1>' est en conflit avec la propriété par défaut '<propertyname2>' de la classe '<classname>' et devrait donc être déclarée 'Shadows'
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: ab45278b2e1199282e3066c34828b9bda716e162
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58813169"
---
# <a name="default-property-propertyname1-conflicts-with-default-property-propertyname2-in-classname-and-so-should-be-declared-shadows"></a>Propriété par défaut '\<nom_propriété1 >' est en conflit avec la propriété par défaut '\<propertyname2 >' dans '\<nom_classe >' et devrait donc être déclarée 'Shadows'
Une propriété est déclarée avec le même nom qu’une propriété définie dans la classe de base. Dans ce cas, la propriété de cette classe doit occulter la propriété de classe de base.  
  
 Ce message est un avertissement. `Shadows` est supposé par défaut. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC40007  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Ajouter le `Shadows` mot clé à la déclaration, ou modifiez le nom de la propriété déclarée.  
  
## <a name="see-also"></a>Voir aussi

- [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md)
- [Occultation dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
