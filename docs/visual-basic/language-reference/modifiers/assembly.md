---
title: Assembly (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Assembly
- vb.AssemblyAttribute
- Assembly
helpviewer_keywords:
- Assembly modifier
- Assembly keyword [Visual Basic]
- attribute blocks, Assembly keyword
ms.assetid: 925e7471-3bdf-4b51-bb93-cbcfc6efc52f
ms.openlocfilehash: 819fa9cf1bd25e9426fb1e75925a269fcf7a71cd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819253"
---
# <a name="assembly-visual-basic"></a>Assembly (Visual Basic)
Spécifie qu’un attribut situé au début d’un fichier source s’applique à la totalité de l’assembly.  
  
## <a name="remarks"></a>Notes  
 Beaucoup d’attributs se rapportent à un élément de programmation individuel, tel qu’une classe ou une propriété. Vous appliquez cet attribut en attachant le bloc d’attributs, entre crochets (`< >`), directement à l’instruction de déclaration.  
  
 Si un attribut appartient non seulement à l’élément suivant, mais aussi à la totalité de l’assembly, vous placez le bloc d’attributs au début du fichier source et identifiez l’attribut avec le `Assembly` mot clé. Si elle s’applique à l’assembly actuel, vous utilisez le [Module](../../../visual-basic/language-reference/modifiers/module-keyword.md) mot clé.  
  
 Vous pouvez également appliquer un attribut à un assembly dans le fichier AssemblyInfo.vb, auquel cas il est inutile d’utiliser un bloc d’attributs dans votre fichier de code source principal.  
  
## <a name="see-also"></a>Voir aussi

- [\<mot clé> du module](../../../visual-basic/language-reference/modifiers/module-keyword.md)
- [Vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md)
