---
title: L'espace de noms ou le type spécifié dans les Imports '<qualifiedelementname>' au niveau du projet ne contient aucun membre public ou est introuvable
ms.date: 07/20/2015
f1_keywords:
- vbc40057
- bc40057
helpviewer_keywords:
- BC40057
ms.assetid: 4ae3506e-2ebe-4ff3-995d-14ac60db5e9f
ms.openlocfilehash: 105fa8da838938d13022c210c1f65cdafd251003
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59308482"
---
# <a name="namespace-or-type-specified-in-the-project-level-imports-qualifiedelementname-doesnt-contain-any-public-member-or-cannot-be-found"></a><span data-ttu-id="aea8c-102">Namespace ou type spécifié dans les Imports' au niveau du projet\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable</span><span class="sxs-lookup"><span data-stu-id="aea8c-102">Namespace or type specified in the project-level Imports '\<qualifiedelementname>' doesn't contain any public member or cannot be found</span></span>
<span data-ttu-id="aea8c-103">Namespace ou type spécifié dans les Imports' au niveau du projet\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="aea8c-103">Namespace or type specified in the project-level Imports '\<qualifiedelementname>' doesn't contain any public member or cannot be found.</span></span> <span data-ttu-id="aea8c-104">Assurez-vous que l’espace de noms ou le type est défini et contient au moins un membre public.</span><span class="sxs-lookup"><span data-stu-id="aea8c-104">Make sure the namespace or the type is defined and contains at least one public member.</span></span> <span data-ttu-id="aea8c-105">Assurez-vous que le nom d’alias ne contient pas d’autres alias.</span><span class="sxs-lookup"><span data-stu-id="aea8c-105">Make sure the alias name doesn't contain other aliases.</span></span>  
  
 <span data-ttu-id="aea8c-106">Une propriété de l’importation d’un projet spécifie un élément conteneur qui ne peut pas être trouvé ou ne définit pas `Public` membres.</span><span class="sxs-lookup"><span data-stu-id="aea8c-106">An import property of a project specifies a containing element that either cannot be found or does not define any `Public` members.</span></span>  
  
 <span data-ttu-id="aea8c-107">Un *contenant l’élément* peut être un espace de noms, une classe, une structure, un module, une interface ou une énumération.</span><span class="sxs-lookup"><span data-stu-id="aea8c-107">A *containing element* can be a namespace, class, structure, module, interface, or enumeration.</span></span> <span data-ttu-id="aea8c-108">L’élément conteneur contient des membres, tels que des variables, procédures ou d’autres éléments qui le contient.</span><span class="sxs-lookup"><span data-stu-id="aea8c-108">The containing element contains members, such as variables, procedures, or other containing elements.</span></span>  
  
 <span data-ttu-id="aea8c-109">L’objectif de l’importation consiste à autoriser votre code pour accéder aux membres de type ou espace de noms sans devoir les qualifier.</span><span class="sxs-lookup"><span data-stu-id="aea8c-109">The purpose of importing is to allow your code to access namespace or type members without having to qualify them.</span></span> <span data-ttu-id="aea8c-110">Votre projet devrez peut-être également ajouter une référence à l’espace de noms ou type.</span><span class="sxs-lookup"><span data-stu-id="aea8c-110">Your project might also need to add a reference to the namespace or type.</span></span> <span data-ttu-id="aea8c-111">Pour plus d’informations, consultez « Importation d’éléments conteneurs » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span><span class="sxs-lookup"><span data-stu-id="aea8c-111">For more information, see "Importing Containing Elements" in [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>  
  
 <span data-ttu-id="aea8c-112">Si le compilateur ne peut pas trouver l’élément conteneur spécifié, il ne peut pas résoudre les références qui l’utilisent.</span><span class="sxs-lookup"><span data-stu-id="aea8c-112">If the compiler cannot find the specified containing element, then it cannot resolve references that use it.</span></span> <span data-ttu-id="aea8c-113">Si elle recherche l’élément, mais l’élément n’expose pas `Public` membres, aucune référence peut être réussie.</span><span class="sxs-lookup"><span data-stu-id="aea8c-113">If it finds the element but the element does not expose any `Public` members, then no reference can be successful.</span></span> <span data-ttu-id="aea8c-114">Dans les deux cas, il est sans signification pour importer l’élément.</span><span class="sxs-lookup"><span data-stu-id="aea8c-114">In either case it is meaningless to import the element.</span></span>  
  
 <span data-ttu-id="aea8c-115">Vous utilisez le **Concepteur de projet** pour spécifier les éléments à importer.</span><span class="sxs-lookup"><span data-stu-id="aea8c-115">You use the **Project Designer** to specify elements to import.</span></span> <span data-ttu-id="aea8c-116">Utilisez le **espaces de noms importés** section de la **références** page.</span><span class="sxs-lookup"><span data-stu-id="aea8c-116">Use the **Imported namespaces** section of the **References** page.</span></span> <span data-ttu-id="aea8c-117">Vous pouvez accéder à la **Concepteur de projets** en double-cliquant sur le **mon projet** icône dans **l’Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="aea8c-117">You can get to the **Project Designer** by double-clicking the **My Project** icon in **Solution Explorer**.</span></span>  
  
 <span data-ttu-id="aea8c-118">**ID d’erreur :** BC40057</span><span class="sxs-lookup"><span data-stu-id="aea8c-118">**Error ID:** BC40057</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="aea8c-119">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="aea8c-119">To correct this error</span></span>  
  
1. <span data-ttu-id="aea8c-120">Ouvrez le **Concepteur de projets** et basculez vers le **référence** page.</span><span class="sxs-lookup"><span data-stu-id="aea8c-120">Open the **Project Designer** and switch to the **Reference** page.</span></span>  
  
2. <span data-ttu-id="aea8c-121">Dans le **espaces de noms importés** section, vérifiez que l’élément conteneur est accessible à partir de votre projet.</span><span class="sxs-lookup"><span data-stu-id="aea8c-121">In the **Imported namespaces** section, verify that the containing element is accessible from your project.</span></span>  
  
3. <span data-ttu-id="aea8c-122">Vérifiez que l’élément conteneur expose au moins un `Public` membre.</span><span class="sxs-lookup"><span data-stu-id="aea8c-122">Verify that the containing element exposes at least one `Public` member.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aea8c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aea8c-123">See also</span></span>

- [<span data-ttu-id="aea8c-124">Page Références, Concepteur de projets (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="aea8c-124">References Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/references-page-project-designer-visual-basic)
- [<span data-ttu-id="aea8c-125">Gestion des propriétés des projets et des solutions</span><span class="sxs-lookup"><span data-stu-id="aea8c-125">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
- [<span data-ttu-id="aea8c-126">Public</span><span class="sxs-lookup"><span data-stu-id="aea8c-126">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="aea8c-127">Espaces de noms dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aea8c-127">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="aea8c-128">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="aea8c-128">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
