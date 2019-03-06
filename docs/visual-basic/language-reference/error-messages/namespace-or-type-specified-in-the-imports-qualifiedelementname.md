---
title: L'espace de noms ou le type spécifié dans les Imports '<qualifiedelementname>' ne contient aucun membre public ou est introuvable
ms.date: 07/20/2015
f1_keywords:
- bc40056
- vbc40056
helpviewer_keywords:
- BC40056
ms.assetid: b59f5754-444f-4378-9272-9678b437e84a
ms.openlocfilehash: 1873c0af7a251afd7754557f5dcb6aed13eb9f11
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357883"
---
# <a name="namespace-or-type-specified-in-the-imports-qualifiedelementname-doesnt-contain-any-public-member-or-cannot-be-found"></a><span data-ttu-id="62d6a-102">Namespace ou type spécifié dans les Imports'\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable</span><span class="sxs-lookup"><span data-stu-id="62d6a-102">Namespace or type specified in the Imports '\<qualifiedelementname>' doesn't contain any public member or cannot be found</span></span>

<span data-ttu-id="62d6a-103">Namespace ou type spécifié dans les Imports'\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="62d6a-103">Namespace or type specified in the Imports '\<qualifiedelementname>' doesn't contain any public member or cannot be found.</span></span> <span data-ttu-id="62d6a-104">Assurez-vous que l’espace de noms ou le type est défini et contient au moins un membre public.</span><span class="sxs-lookup"><span data-stu-id="62d6a-104">Make sure the namespace or the type is defined and contains at least one public member.</span></span> <span data-ttu-id="62d6a-105">Assurez-vous que le nom d’alias ne contient pas d’autres alias.</span><span class="sxs-lookup"><span data-stu-id="62d6a-105">Make sure the alias name doesn't contain other aliases.</span></span>

<span data-ttu-id="62d6a-106">Un `Imports` instruction spécifie un élément conteneur qui ne peut pas être trouvé ou ne définit pas `Public` membres.</span><span class="sxs-lookup"><span data-stu-id="62d6a-106">An `Imports` statement specifies a containing element that either cannot be found or does not define any `Public` members.</span></span>

<span data-ttu-id="62d6a-107">Un *contenant l’élément* peut être un espace de noms, une classe, une structure, un module, une interface ou une énumération.</span><span class="sxs-lookup"><span data-stu-id="62d6a-107">A *containing element* can be a namespace, class, structure, module, interface, or enumeration.</span></span> <span data-ttu-id="62d6a-108">L’élément conteneur contient des membres, tels que des variables, procédures ou d’autres éléments qui le contient.</span><span class="sxs-lookup"><span data-stu-id="62d6a-108">The containing element contains members, such as variables, procedures, or other containing elements.</span></span>

<span data-ttu-id="62d6a-109">L’objectif de l’importation consiste à autoriser votre code pour accéder aux membres de type ou espace de noms sans devoir les qualifier.</span><span class="sxs-lookup"><span data-stu-id="62d6a-109">The purpose of importing is to allow your code to access namespace or type members without having to qualify them.</span></span> <span data-ttu-id="62d6a-110">Votre projet devrez peut-être également ajouter une référence à l’espace de noms ou type.</span><span class="sxs-lookup"><span data-stu-id="62d6a-110">Your project might also need to add a reference to the namespace or type.</span></span> <span data-ttu-id="62d6a-111">Pour plus d’informations, consultez « Importation d’éléments conteneurs » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span><span class="sxs-lookup"><span data-stu-id="62d6a-111">For more information, see "Importing Containing Elements" in [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>

<span data-ttu-id="62d6a-112">Si le compilateur ne peut pas trouver l’élément conteneur spécifié, il ne peut pas résoudre les références qui l’utilisent.</span><span class="sxs-lookup"><span data-stu-id="62d6a-112">If the compiler cannot find the specified containing element, then it cannot resolve references that use it.</span></span> <span data-ttu-id="62d6a-113">Si elle recherche l’élément, mais l’élément n’expose pas `Public` membres, aucune référence peut être réussie.</span><span class="sxs-lookup"><span data-stu-id="62d6a-113">If it finds the element but the element does not expose any `Public` members, then no reference can be successful.</span></span> <span data-ttu-id="62d6a-114">Dans les deux cas, il est sans signification pour importer l’élément.</span><span class="sxs-lookup"><span data-stu-id="62d6a-114">In either case it is meaningless to import the element.</span></span>

<span data-ttu-id="62d6a-115">N’oubliez pas que si vous importez un élément de conteneur et lui affectez un alias d’importation, puis vous ne pouvez pas utiliser cet alias d’importation pour importer un autre élément.</span><span class="sxs-lookup"><span data-stu-id="62d6a-115">Keep in mind that if you import a containing element and assign an import alias to it, then you cannot use that import alias to import another element.</span></span> <span data-ttu-id="62d6a-116">Le code suivant génère une erreur du compilateur.</span><span class="sxs-lookup"><span data-stu-id="62d6a-116">The following code generates a compiler error.</span></span>

```vb
Imports winfrm = System.Windows.Forms

' The following statement is INVALID  because it reuses an import alias.

Imports behave = winfrm.Design.Behavior`
```

<span data-ttu-id="62d6a-117">**ID d’erreur :** BC40056</span><span class="sxs-lookup"><span data-stu-id="62d6a-117">**Error ID:** BC40056</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="62d6a-118">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="62d6a-118">To correct this error</span></span>

1. <span data-ttu-id="62d6a-119">Vérifiez que l’élément conteneur est accessible à partir de votre projet.</span><span class="sxs-lookup"><span data-stu-id="62d6a-119">Verify that the containing element is accessible from your project.</span></span>

2. <span data-ttu-id="62d6a-120">Vérifiez que la spécification de l’élément conteneur n’inclut pas de n’importe quel alias d’importation à partir d’une autre importation.</span><span class="sxs-lookup"><span data-stu-id="62d6a-120">Verify that the specification of the containing element does not include any import alias from another import.</span></span>

3. <span data-ttu-id="62d6a-121">Vérifiez que l’élément conteneur expose au moins un `Public` membre.</span><span class="sxs-lookup"><span data-stu-id="62d6a-121">Verify that the containing element exposes at least one `Public` member.</span></span>

## <a name="see-also"></a><span data-ttu-id="62d6a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62d6a-122">See also</span></span>

- [<span data-ttu-id="62d6a-123">Imports (instruction) (espace de noms et type .NET)</span><span class="sxs-lookup"><span data-stu-id="62d6a-123">Imports Statement (.NET Namespace and Type)</span></span>](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [<span data-ttu-id="62d6a-124">Namespace (instruction)</span><span class="sxs-lookup"><span data-stu-id="62d6a-124">Namespace Statement</span></span>](../../../visual-basic/language-reference/statements/namespace-statement.md)
- [<span data-ttu-id="62d6a-125">Public</span><span class="sxs-lookup"><span data-stu-id="62d6a-125">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)
- [<span data-ttu-id="62d6a-126">Espaces de noms dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="62d6a-126">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="62d6a-127">Références aux éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="62d6a-127">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
