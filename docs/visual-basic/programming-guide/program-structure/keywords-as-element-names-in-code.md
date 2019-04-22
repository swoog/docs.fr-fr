---
title: Utilisation des mots clés comme noms d'éléments dans le code (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, naming conventions
- keywords [Visual Basic], in code
- name conflicts [Visual Basic]
- element names [Visual Basic], in code
ms.assetid: 2e4e8e02-23f7-49b9-a1c8-2b0402b6b525
ms.openlocfilehash: c247ada67f6554362f287cf252dd49856c4995da
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58841145"
---
# <a name="keywords-as-element-names-in-code-visual-basic"></a><span data-ttu-id="1a764-102">Utilisation des mots clés comme noms d'éléments dans le code (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1a764-102">Keywords as Element Names in Code (Visual Basic)</span></span>
<span data-ttu-id="1a764-103">Un élément de programme, tel qu’une variable, une classe ou un membre — peut avoir le même nom qu’un mot clé restreint.</span><span class="sxs-lookup"><span data-stu-id="1a764-103">Any program element — such as a variable, class, or member — can have the same name as a restricted keyword.</span></span> <span data-ttu-id="1a764-104">Par exemple, vous pouvez créer une variable nommée `Loop`.</span><span class="sxs-lookup"><span data-stu-id="1a764-104">For example, you can create a variable named `Loop`.</span></span> <span data-ttu-id="1a764-105">Toutefois, pour faire référence à votre version de celui-ci, qui a le même nom que restreint `Loop` mot clé, vous devez le faire précéder d’une chaîne de qualification complète ou le placer entre crochets (`[ ]`), comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="1a764-105">However, to refer to your version of it — which has the same name as the restricted `Loop` keyword — you must either precede it with a full qualification string or enclose it in square brackets (`[ ]`), as the following example shows.</span></span>  
  
 [!code-vb[VbVbcnConventions#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#8)]  
  
 <span data-ttu-id="1a764-106">Si vous ne le faites pas une de ces, Visual Basic suppose l’utilisation de la fonction intrinsèque `Loop` mot clé et génère une erreur, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="1a764-106">If you do not do either of these, then Visual Basic assumes use of the intrinsic `Loop` keyword and produces an error, as in the following example:</span></span>  
  
 `' The following statement causes a compiler error.`  
  
 `Loop.Visible = True`  
  
 <span data-ttu-id="1a764-107">Vous pouvez utiliser des crochets lorsque vous faites référence aux formulaires et contrôles et lors de la déclaration d’une variable ou la définition d’une procédure portant le même nom qu’un mot clé restreint.</span><span class="sxs-lookup"><span data-stu-id="1a764-107">You can use square brackets when referring to forms and controls, and when declaring a variable or defining a procedure with the same name as a restricted keyword.</span></span> <span data-ttu-id="1a764-108">Il peut être facile d’oublier de qualifier des noms ou inclure des crochets, par conséquent introduire des erreurs dans votre code et rendre plus difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="1a764-108">It can be easy to forget to qualify names or include square brackets, and thus introduce errors into your code and make it harder to read.</span></span> <span data-ttu-id="1a764-109">Pour cette raison, nous vous recommandons de pas utiliser de mots clés restreints comme noms d’éléments de programme.</span><span class="sxs-lookup"><span data-stu-id="1a764-109">For this reason, we recommend that you not use restricted keywords as the names of program elements.</span></span> <span data-ttu-id="1a764-110">Toutefois, si une version ultérieure de Visual Basic définit un nouveau mot clé qui entre en conflit avec un nom de contrôle ou un formulaire existant, puis vous pouvez utiliser cette technique lorsque la mise à jour votre code pour travailler avec la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="1a764-110">However, if a future version of Visual Basic defines a new keyword that conflicts with an existing form or control name, then you can use this technique when updating your code to work with the new version.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1a764-111">Votre programme peut également inclure des noms d’éléments fournis par d’autres assemblys référencés.</span><span class="sxs-lookup"><span data-stu-id="1a764-111">Your program also might include element names provided by other referenced assemblies.</span></span> <span data-ttu-id="1a764-112">Si ces noms sont en conflit avec les mots clés restreints, puis placer des crochets autour d’elles entraîne Visual Basic pour les interpréter comme vos éléments définis.</span><span class="sxs-lookup"><span data-stu-id="1a764-112">If these names conflict with restricted keywords, then placing square brackets around them causes Visual Basic to interpret them as your defined elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a764-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a764-113">See also</span></span>

- [<span data-ttu-id="1a764-114">Conventions d’affectation de noms de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1a764-114">Visual Basic Naming Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
- [<span data-ttu-id="1a764-115">Structure de programme et conventions de codage</span><span class="sxs-lookup"><span data-stu-id="1a764-115">Program Structure and Code Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [<span data-ttu-id="1a764-116">Mots clés</span><span class="sxs-lookup"><span data-stu-id="1a764-116">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
