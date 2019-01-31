---
title: Le nom <membername> n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- bc40031
- vbc40031
helpviewer_keywords:
- BC40031
ms.assetid: e2b885dc-cbf9-49ff-bbbe-531657ea99f7
ms.openlocfilehash: 74b625cc3a60e591417530c6a6229c01666038e2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271250"
---
# <a name="name-membername-is-not-cls-compliant"></a>Nom \<nom_membre > n’est pas conforme CLS
Un assembly est marqué comme `<CLSCompliant(True)>` mais expose un membre dont le nom commence par un trait de soulignement (`_`).  
  
 Un élément de programmation peut contenir un ou plusieurs des traits de soulignement, mais to être conforme à la [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS), il ne doit pas commencer par un trait de soulignement. Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
 Quand vous appliquez <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité. Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.  
  
 Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC40031  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si vous contrôlez le code source, modifiez le nom du membre afin qu’il ne commence pas par un trait de soulignement.  
  
-   Si vous avez besoin que le nom de membre reste inchangé, supprimez le <xref:System.CLSCompliantAttribute> à partir de sa définition ou marquez-le comme `<CLSCompliant(False)>`. Vous pouvez toujours marquer l’assembly en tant que `<CLSCompliant(True)>`.  
  
## <a name="see-also"></a>Voir aussi
- [Noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)

