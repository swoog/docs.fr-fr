---
title: <message> Cette erreur peut également être en raison d’une combinaison d’une référence de fichier avec une référence de projet à l’assembly '<assemblyname>'
ms.date: 07/20/2015
f1_keywords:
- bc30971
- vbc30971
helpviewer_keywords:
- BC30971
ms.assetid: 75d2e8b5-2fdc-4623-8b32-cba805dab7db
ms.openlocfilehash: 951f90a9209ff31896f4426ceb75f05b012897a6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59335145"
---
# <a name="message-this-error-could-also-be-due-to-mixing-a-file-reference-with-a-project-reference-to-assembly-assemblyname"></a>\<message > Cette erreur peut également être en raison d’une combinaison d’une référence de fichier avec une référence de projet à l’assembly '\<nom_assembly >'
\<message > Cette erreur peut également être en raison d’une combinaison d’une référence de fichier avec une référence de projet à l’assembly '\<nom_assembly >. Dans ce cas, essayez de remplacer la référence de fichier à '\<nom_fichier_assembly >' dans le projet '\<nom_projet1 >' avec une référence de projet à '\<nom_projet2 >'.  
  
 Code de votre projet accède à un membre d’un autre projet, mais la configuration de votre solution n’autorise pas le compilateur Visual Basic résoudre la référence.  
  
 Pour accéder à un type défini dans un autre assembly, le compilateur Visual Basic doit avoir une référence à cet assembly. Il doit s’agir d’une référence unique et non équivoque qui ne provoque pas de références circulaires parmi des projets.  
  
 **ID d’erreur :** BC30971  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Identifiez le projet qui produit le meilleur assembly pour votre projet à référencer. Pour prendre cette décision, vous pouvez utiliser des critères, tels que la facilité d’accès au fichier et la fréquence des mises à jour.  
  
2. Dans les propriétés de votre projet, ajoutez une référence au projet contenant l’assembly qui définit le type que vous utilisez.  
  
## <a name="see-also"></a>Voir aussi

- [Gestion des références dans un projet](/visualstudio/ide/managing-references-in-a-project)
- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)

- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
- [Dépannage de références rompues](/visualstudio/ide/troubleshooting-broken-references)
