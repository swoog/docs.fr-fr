---
title: Une référence à l'assembly '<assemblyidentity>' contenant le type '<typename>' est requise, mais une référence adéquate n'a pas été trouvée en raison de l'ambiguïté entre les projets '<projectname1>' et '<projectname2>'
ms.date: 07/20/2015
f1_keywords:
- bc30969
- vbc30969
helpviewer_keywords:
- BC30969
ms.assetid: 1b29dbc5-8268-45fe-bfc2-b2070a5c845c
ms.openlocfilehash: 3cfdf8150c8ccd9e1b4f047cd1ce8ee4ad6bbc1a
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58813403"
---
# <a name="reference-required-to-assembly-assemblyidentity-containing-type-typename-but-a-suitable-reference-could-not-be-found-due-to-ambiguity-between-projects-projectname1-and-projectname2"></a>Référence à l’assembly requise '\<assemblyidentity >' contenant le type '\<nom_type >', mais une référence appropriée est introuvable en raison de l’ambiguïté entre les projets\<nom_projet1 >' et '\< nom_projet2 >'
Une expression utilise un type, comme une classe, une structure, une interface, une énumération ou un délégué, qui est défini en dehors de votre projet. Cependant, des références de projet désignent plusieurs assemblys définissant ce type.  
  
 Les projets cités produisent des assemblys de même nom. Par conséquent, le compilateur ne peut pas déterminer quel assembly utiliser pour le type auquel vous accédez.  
  
 Pour accéder à un type défini dans un autre assembly, le compilateur Visual Basic doit avoir une référence à cet assembly. Il doit s’agir d’une référence unique et non équivoque qui ne provoque pas de références circulaires parmi des projets.  
  
 **ID d’erreur :** BC30969  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Identifiez le projet qui produit le meilleur assembly pour votre projet à référencer. Pour prendre cette décision, vous pouvez utiliser des critères, tels que la facilité d’accès au fichier et la fréquence des mises à jour.  
  
2.  Dans vos propriétés de projet, ajoutez une référence au fichier contenant l’assembly qui définit le type que vous utilisez.  
  
## <a name="see-also"></a>Voir aussi

- [Gestion des références dans un projet](/visualstudio/ide/managing-references-in-a-project)
- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)

- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
- [Dépannage de références rompues](/visualstudio/ide/troubleshooting-broken-references)
