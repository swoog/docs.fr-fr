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
# <a name="assembly-visual-basic"></a><span data-ttu-id="ac972-102">Assembly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ac972-102">Assembly (Visual Basic)</span></span>
<span data-ttu-id="ac972-103">Spécifie qu’un attribut situé au début d’un fichier source s’applique à la totalité de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ac972-103">Specifies that an attribute at the beginning of a source file applies to the entire assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ac972-104">Notes</span><span class="sxs-lookup"><span data-stu-id="ac972-104">Remarks</span></span>  
 <span data-ttu-id="ac972-105">Beaucoup d’attributs se rapportent à un élément de programmation individuel, tel qu’une classe ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="ac972-105">Many attributes pertain to an individual programming element, such as a class or property.</span></span> <span data-ttu-id="ac972-106">Vous appliquez cet attribut en attachant le bloc d’attributs, entre crochets (`< >`), directement à l’instruction de déclaration.</span><span class="sxs-lookup"><span data-stu-id="ac972-106">You apply such an attribute by attaching the attribute block, within angle brackets (`< >`), directly to the declaration statement.</span></span>  
  
 <span data-ttu-id="ac972-107">Si un attribut appartient non seulement à l’élément suivant, mais aussi à la totalité de l’assembly, vous placez le bloc d’attributs au début du fichier source et identifiez l’attribut avec le `Assembly` mot clé.</span><span class="sxs-lookup"><span data-stu-id="ac972-107">If an attribute pertains not only to the following element but to the entire assembly, you place the attribute block at the beginning of the source file and identify the attribute with the `Assembly` keyword.</span></span> <span data-ttu-id="ac972-108">Si elle s’applique à l’assembly actuel, vous utilisez le [Module](../../../visual-basic/language-reference/modifiers/module-keyword.md) mot clé.</span><span class="sxs-lookup"><span data-stu-id="ac972-108">If it applies to the current assembly module, you use the [Module](../../../visual-basic/language-reference/modifiers/module-keyword.md) keyword.</span></span>  
  
 <span data-ttu-id="ac972-109">Vous pouvez également appliquer un attribut à un assembly dans le fichier AssemblyInfo.vb, auquel cas il est inutile d’utiliser un bloc d’attributs dans votre fichier de code source principal.</span><span class="sxs-lookup"><span data-stu-id="ac972-109">You can also apply an attribute to an assembly in the AssemblyInfo.vb file, in which case you do not have to use an attribute block in your main source-code file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac972-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac972-110">See also</span></span>

- [<span data-ttu-id="ac972-111">\<mot clé> du module</span><span class="sxs-lookup"><span data-stu-id="ac972-111">Module \<keyword></span></span>](../../../visual-basic/language-reference/modifiers/module-keyword.md)
- [<span data-ttu-id="ac972-112">Vue d’ensemble des attributs</span><span class="sxs-lookup"><span data-stu-id="ac972-112">Attributes overview</span></span>](../../../visual-basic/programming-guide/concepts/attributes/index.md)
