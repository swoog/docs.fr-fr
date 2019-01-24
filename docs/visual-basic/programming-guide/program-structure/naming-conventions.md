---
title: Conventions d'affectation de noms Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- names [Visual Basic], Visual Basic rules
- naming conventions
- naming conventions [Visual Basic], Visual Basic
- Visual Basic code, naming conventions
- conventions [Visual Basic], Visual Basic coding
- names [Visual Basic], naming conventions
- naming conventions [Visual Basic], classes
ms.assetid: 164949a4-2a7c-4736-9d82-9c3078e2e56c
ms.openlocfilehash: ebb9d21e32993f2eb035993d32dc3de7d97b49f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672134"
---
# <a name="visual-basic-naming-conventions"></a><span data-ttu-id="505f3-102">Conventions d'affectation de noms Visual Basic</span><span class="sxs-lookup"><span data-stu-id="505f3-102">Visual Basic Naming Conventions</span></span>
<span data-ttu-id="505f3-103">Lorsque vous nommez un élément dans votre application Visual Basic, le premier caractère de ce nom doit être un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="505f3-103">When you name an element in your Visual Basic application, the first character of that name must be an alphabetic character or an underscore.</span></span> <span data-ttu-id="505f3-104">Notez, cependant, que les noms commençant par un trait de soulignement ne sont pas compatibles avec le [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span><span class="sxs-lookup"><span data-stu-id="505f3-104">Note, however, that names beginning with an underscore are not compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span></span>  
  
 <span data-ttu-id="505f3-105">Les suggestions suivantes s’appliquent à d’affectation de noms.</span><span class="sxs-lookup"><span data-stu-id="505f3-105">The following suggestions apply to naming.</span></span>  
  
-   <span data-ttu-id="505f3-106">Commencer chaque mot distinct dans un nom par une lettre majuscule, comme dans `FindLastRecord` et `RedrawMyForm`.</span><span class="sxs-lookup"><span data-stu-id="505f3-106">Begin each separate word in a name with a capital letter, as in `FindLastRecord` and `RedrawMyForm`.</span></span>  
  
-   <span data-ttu-id="505f3-107">Commencer les noms de fonction et de méthode avec un verbe, comme dans `InitNameArray` ou `CloseDialog`.</span><span class="sxs-lookup"><span data-stu-id="505f3-107">Begin function and method names with a verb, as in `InitNameArray` or `CloseDialog`.</span></span>  
  
-   <span data-ttu-id="505f3-108">Commencer une classe, structure, module et les noms de propriété par un nom, comme dans `EmployeeName` ou `CarAccessory`.</span><span class="sxs-lookup"><span data-stu-id="505f3-108">Begin class, structure, module, and property names with a noun, as in `EmployeeName` or `CarAccessory`.</span></span>  
  
-   <span data-ttu-id="505f3-109">Commencer les noms d’interface avec le préfixe « I », suivi d’un nom ou d’une expression nominale, comme `IComponent`, ou d’un adjectif décrivant le comportement de l’interface, comme `IPersistable`.</span><span class="sxs-lookup"><span data-stu-id="505f3-109">Begin interface names with the prefix "I", followed by a noun or a noun phrase, like `IComponent`, or with an adjective describing the interface's behavior, like `IPersistable`.</span></span> <span data-ttu-id="505f3-110">N’utilisent pas le caractère de soulignement et utilisez les abréviations avec parcimonie, étant donné que les abréviations peuvent entraîner une confusion.</span><span class="sxs-lookup"><span data-stu-id="505f3-110">Do not use the underscore, and use abbreviations sparingly, because abbreviations can cause confusion.</span></span>  
  
-   <span data-ttu-id="505f3-111">Commencer les noms de gestionnaires d’événements par un nom décrivant le type d’événement suivi par la «`EventHandler`« de suffixe, comme dans »`MouseEventHandler`».</span><span class="sxs-lookup"><span data-stu-id="505f3-111">Begin event handler names with a noun describing the type of event followed by the "`EventHandler`" suffix, as in "`MouseEventHandler`".</span></span>  
  
-   <span data-ttu-id="505f3-112">Dans les noms de classes d’arguments d’événement, ajoutez le «`EventArgs`« suffixe.</span><span class="sxs-lookup"><span data-stu-id="505f3-112">In names of event argument classes, include the "`EventArgs`" suffix.</span></span>  
  
-   <span data-ttu-id="505f3-113">Si un événement a un concept de « before » ou « after », utilisez un suffixe dans le présent ou passé, comme dans «`ControlAdd`« ou »`ControlAdded`».</span><span class="sxs-lookup"><span data-stu-id="505f3-113">If an event has a concept of "before" or "after," use a suffix in present or past tense, as in "`ControlAdd`" or "`ControlAdded`".</span></span>  
  
-   <span data-ttu-id="505f3-114">Pour les termes longs ou fréquemment utilisés, utilisez les abréviations pour limiter la longueur, par exemple, « HTML », au lieu de « Hypertext Markup Language ».</span><span class="sxs-lookup"><span data-stu-id="505f3-114">For long or frequently used terms, use abbreviations to keep name lengths reasonable, for example, "HTML", instead of "Hypertext Markup Language".</span></span> <span data-ttu-id="505f3-115">En règle générale, les noms de variables de plus de 32 caractères sont difficiles à lire sur un écran avec une faible résolution.</span><span class="sxs-lookup"><span data-stu-id="505f3-115">In general, variable names greater than 32 characters are difficult to read on a monitor set to a low resolution.</span></span> <span data-ttu-id="505f3-116">En outre, assurez-vous que vos abréviations sont cohérentes dans toute l’application.</span><span class="sxs-lookup"><span data-stu-id="505f3-116">Also, make sure your abbreviations are consistent throughout the entire application.</span></span> <span data-ttu-id="505f3-117">De manière aléatoire dans un projet entre « HTML » et « Hypertext Markup Language » peut prêter à confusion.</span><span class="sxs-lookup"><span data-stu-id="505f3-117">Randomly switching in a project between "HTML" and "Hypertext Markup Language" can lead to confusion.</span></span>  
  
-   <span data-ttu-id="505f3-118">Évitez d’utiliser des noms dans une portée interne sont les mêmes que les noms dans une portée externe.</span><span class="sxs-lookup"><span data-stu-id="505f3-118">Avoid using names in an inner scope that are the same as names in an outer scope.</span></span> <span data-ttu-id="505f3-119">Erreurs peuvent entraîner si la variable incorrecte est accessible.</span><span class="sxs-lookup"><span data-stu-id="505f3-119">Errors can result if the wrong variable is accessed.</span></span> <span data-ttu-id="505f3-120">En cas de conflit entre une variable et le mot clé du même nom, vous devez identifier le mot clé en le faisant précéder avec la bibliothèque de types appropriés.</span><span class="sxs-lookup"><span data-stu-id="505f3-120">If a conflict occurs between a variable and the keyword of the same name, you must identify the keyword by preceding it with the appropriate type library.</span></span> <span data-ttu-id="505f3-121">Par exemple, si vous disposez d’une variable appelée `Date`, vous pouvez utiliser la fonction intrinsèque `Date` fonction uniquement en appelant <xref:System.DateTime.Date%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="505f3-121">For example, if you have a variable called `Date`, you can use the intrinsic `Date` function only by calling <xref:System.DateTime.Date%2A?displayProperty=nameWithType>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="505f3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="505f3-122">See also</span></span>
- [<span data-ttu-id="505f3-123">Utilisation des mots clés comme noms d’éléments dans le code</span><span class="sxs-lookup"><span data-stu-id="505f3-123">Keywords as Element Names in Code</span></span>](../../../visual-basic/programming-guide/program-structure/keywords-as-element-names-in-code.md)
- [<span data-ttu-id="505f3-124">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="505f3-124">Me, My, MyBase, and MyClass</span></span>](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="505f3-125">Noms d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="505f3-125">Declared Element Names</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="505f3-126">Structure de programme et conventions de codage</span><span class="sxs-lookup"><span data-stu-id="505f3-126">Program Structure and Code Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [<span data-ttu-id="505f3-127">Informations de référence sur le langage Visual Basic</span><span class="sxs-lookup"><span data-stu-id="505f3-127">Visual Basic Language Reference</span></span>](../../../visual-basic/language-reference/index.md)
