---
title: Le nom <membername> n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- bc40031
- vbc40031
helpviewer_keywords:
- BC40031
ms.assetid: e2b885dc-cbf9-49ff-bbbe-531657ea99f7
ms.openlocfilehash: 06b20b4f61741f2174654d749df55c3c4348c547
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787463"
---
# <a name="name-membername-is-not-cls-compliant"></a><span data-ttu-id="116ac-102">Nom \<nom_membre > n’est pas conforme CLS</span><span class="sxs-lookup"><span data-stu-id="116ac-102">Name \<membername> is not CLS-compliant</span></span>
<span data-ttu-id="116ac-103">Un assembly est marqué comme `<CLSCompliant(True)>` mais expose un membre dont le nom commence par un trait de soulignement (`_`).</span><span class="sxs-lookup"><span data-stu-id="116ac-103">An assembly is marked as `<CLSCompliant(True)>` but exposes a member with a name that begins with an underscore (`_`).</span></span>  
  
 <span data-ttu-id="116ac-104">Un élément de programmation peut contenir un ou plusieurs des traits de soulignement, mais to être conforme à la [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS), il ne doit pas commencer par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="116ac-104">A programming element can contain one or more underscores, but to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must not begin with an underscore.</span></span> <span data-ttu-id="116ac-105">Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="116ac-105">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
 <span data-ttu-id="116ac-106">Quand vous appliquez <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité.</span><span class="sxs-lookup"><span data-stu-id="116ac-106">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="116ac-107">Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="116ac-107">There is no default for this parameter, and you must supply a value.</span></span>  
  
 <span data-ttu-id="116ac-108">Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.</span><span class="sxs-lookup"><span data-stu-id="116ac-108">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>  
  
 <span data-ttu-id="116ac-109">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="116ac-109">By default, this message is a warning.</span></span> <span data-ttu-id="116ac-110">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="116ac-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="116ac-111">**ID d’erreur :** BC40031</span><span class="sxs-lookup"><span data-stu-id="116ac-111">**Error ID:** BC40031</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="116ac-112">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="116ac-112">To correct this error</span></span>  
  
- <span data-ttu-id="116ac-113">Si vous contrôlez le code source, modifiez le nom du membre afin qu’il ne commence pas par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="116ac-113">If you have control over the source code, change the member name so that it does not begin with an underscore.</span></span>  
  
- <span data-ttu-id="116ac-114">Si vous avez besoin que le nom de membre reste inchangé, supprimez le <xref:System.CLSCompliantAttribute> à partir de sa définition ou marquez-le comme `<CLSCompliant(False)>`.</span><span class="sxs-lookup"><span data-stu-id="116ac-114">If you require that the member name remain unchanged, remove the <xref:System.CLSCompliantAttribute> from its definition or mark it as `<CLSCompliant(False)>`.</span></span> <span data-ttu-id="116ac-115">Vous pouvez toujours marquer l’assembly en tant que `<CLSCompliant(True)>`.</span><span class="sxs-lookup"><span data-stu-id="116ac-115">You can still mark the assembly as `<CLSCompliant(True)>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="116ac-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="116ac-116">See also</span></span>

- [<span data-ttu-id="116ac-117">Noms d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="116ac-117">Declared Element Names</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="116ac-118">Conventions d’affectation de noms de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="116ac-118">Visual Basic Naming Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
