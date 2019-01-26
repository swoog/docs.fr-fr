---
title: Références et l'instruction Imports (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- assemblies [Visual Basic], namespaces
- references [Visual Basic], assembly
- namespaces [Visual Basic], assemblies
- referencing assemblies
- Imports statement [Visual Basic], referencing assemblies
- assemblies [Visual Basic], references
ms.assetid: 38149bd4-0a6f-4b31-b5f8-94a8c33f1600
ms.openlocfilehash: c50a25dc0802f275e5cd4e0068e1a68bf559abc1
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066036"
---
# <a name="references-and-the-imports-statement-visual-basic"></a><span data-ttu-id="e73bb-102">Références et l'instruction Imports (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e73bb-102">References and the Imports Statement (Visual Basic)</span></span>
<span data-ttu-id="e73bb-103">Vous pouvez proposer des objets externes à votre projet en choisissant le **ajouter une référence** commande sur le **projet** menu.</span><span class="sxs-lookup"><span data-stu-id="e73bb-103">You can make external objects available to your project by choosing the **Add Reference** command on the **Project** menu.</span></span> <span data-ttu-id="e73bb-104">Les références dans Visual Basic peuvent pointer vers des assemblys qui sont semblables à des bibliothèques de types, mais contiennent plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e73bb-104">References in Visual Basic can point to assemblies, which are like type libraries but contain more information.</span></span>  
  
## <a name="the-imports-statement"></a><span data-ttu-id="e73bb-105">L’instruction Imports</span><span class="sxs-lookup"><span data-stu-id="e73bb-105">The Imports Statement</span></span>  
 <span data-ttu-id="e73bb-106">Assemblys incluent un ou plusieurs espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="e73bb-106">Assemblies include one or more namespaces.</span></span> <span data-ttu-id="e73bb-107">Lorsque vous ajoutez une référence à un assembly, vous pouvez également ajouter un `Imports` instruction à un module qui contrôle la visibilité des espaces de noms de l’assembly dans le module.</span><span class="sxs-lookup"><span data-stu-id="e73bb-107">When you add a reference to an assembly, you can also add an `Imports` statement to a module that controls the visibility of that assembly's namespaces within the module.</span></span> <span data-ttu-id="e73bb-108">La `Imports` instruction offre une portée qui vous permet d’utiliser uniquement la partie de l’espace de noms nécessaire pour fournir une référence unique.</span><span class="sxs-lookup"><span data-stu-id="e73bb-108">The `Imports` statement provides a scoping context that lets you use only the portion of the namespace necessary to supply a unique reference.</span></span>  
  
 <span data-ttu-id="e73bb-109">La `Imports` instruction présente la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="e73bb-109">The `Imports` statement has the following syntax:</span></span>  
  
 `Imports [Aliasname =] Namespace`  
  
 <span data-ttu-id="e73bb-110">`Aliasname` fait référence à un nom court, que vous pouvez utiliser dans du code pour faire référence à un espace de noms importé.</span><span class="sxs-lookup"><span data-stu-id="e73bb-110">`Aliasname` refers to a short name you can use within code to refer to an imported namespace.</span></span> <span data-ttu-id="e73bb-111">`Namespace` est un espace de noms disponible via une référence de projet, une définition dans le projet, ou via un précédent `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="e73bb-111">`Namespace` is a namespace available through either a project reference, through a definition within the project, or through a previous `Imports` statement.</span></span>  
  
 <span data-ttu-id="e73bb-112">Un module peut contenir un nombre quelconque de `Imports` instructions.</span><span class="sxs-lookup"><span data-stu-id="e73bb-112">A module may contain any number of `Imports` statements.</span></span> <span data-ttu-id="e73bb-113">Ils doivent apparaître après n’importe quel `Option` instructions, le cas échéant, mais avant tout autre code.</span><span class="sxs-lookup"><span data-stu-id="e73bb-113">They must appear after any `Option` statements, if present, but before any other code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e73bb-114">Ne confondez pas les références de projet avec le `Imports` instruction ou la `Declare` instruction.</span><span class="sxs-lookup"><span data-stu-id="e73bb-114">Do not confuse project references with the `Imports` statement or the `Declare` statement.</span></span> <span data-ttu-id="e73bb-115">Références de projet à disposition des objets externes, tels que les objets dans les assemblys, aux projets Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e73bb-115">Project references make external objects, such as objects in assemblies, available to Visual Basic projects.</span></span> <span data-ttu-id="e73bb-116">La `Imports` instruction permet de simplifier l’accès aux références de projet, mais ne donne pas accès à ces objets.</span><span class="sxs-lookup"><span data-stu-id="e73bb-116">The `Imports` statement is used to simplify access to project references, but does not provide access to these objects.</span></span> <span data-ttu-id="e73bb-117">La `Declare` instruction est utilisée pour déclarer une référence à une procédure externe dans une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="e73bb-117">The `Declare` statement is used to declare a reference to an external procedure in a dynamic-link library (DLL).</span></span>  
  
## <a name="using-aliases-with-the-imports-statement"></a><span data-ttu-id="e73bb-118">L’utilisation d’alias avec l’instruction Imports</span><span class="sxs-lookup"><span data-stu-id="e73bb-118">Using Aliases with the Imports Statement</span></span>  
 <span data-ttu-id="e73bb-119">La `Imports` instruction facilite accès aux méthodes des classes en éliminant la nécessité pour typer explicitement les noms qualifiés complets de références.</span><span class="sxs-lookup"><span data-stu-id="e73bb-119">The `Imports` statement makes it easier to access methods of classes by eliminating the need to explicitly type the fully qualified names of references.</span></span> <span data-ttu-id="e73bb-120">Les alias vous permettent d’attribuer un nom plus convivial à seulement une partie d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e73bb-120">Aliases let you assign a friendlier name to just one part of a namespace.</span></span> <span data-ttu-id="e73bb-121">Par exemple, la retour chariot/ligne flux séquence qui provoque un seul élément de texte à afficher sur plusieurs lignes fait partie de la <xref:Microsoft.VisualBasic.ControlChars> module dans le <xref:Microsoft.VisualBasic?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e73bb-121">For example, the carriage return/line feed sequence that causes a single piece of text to be displayed on multiple lines is part of the <xref:Microsoft.VisualBasic.ControlChars> module in the <xref:Microsoft.VisualBasic?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="e73bb-122">Pour utiliser cette constante dans un programme sans alias, vous devez taper le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e73bb-122">To use this constant in a program without an alias, you would need to type the following code:</span></span>  
  
 [!code-vb[VbVbalrApplication#3](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_1.vb)]  
  
 <span data-ttu-id="e73bb-123">`Imports` instructions doivent toujours être les premières lignes immédiatement après les `Option` instructions dans un module.</span><span class="sxs-lookup"><span data-stu-id="e73bb-123">`Imports` statements must always be the first lines immediately following any `Option` statements in a module.</span></span> <span data-ttu-id="e73bb-124">Le fragment de code suivant montre comment importer et affecter un alias pour le <xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType> module :</span><span class="sxs-lookup"><span data-stu-id="e73bb-124">The following code fragment shows how to import and assign an alias to the <xref:Microsoft.VisualBasic.ControlChars?displayProperty=nameWithType> module:</span></span>  
  
 [!code-vb[VbVbalrApplication#4](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_2.vb)]  
  
 <span data-ttu-id="e73bb-125">Références ultérieures à cet espace de noms peuvent être considérablement plus courts :</span><span class="sxs-lookup"><span data-stu-id="e73bb-125">Future references to this namespace can be considerably shorter:</span></span>  
  
 [!code-vb[VbVbalrApplication#5](../../../visual-basic/programming-guide/program-structure/codesnippet/VisualBasic/references-and-the-imports-statement_3.vb)]  
  
 <span data-ttu-id="e73bb-126">Si un `Imports` instruction n’inclut pas un nom d’alias, les éléments définis dans l’espace de noms importé peuvent être utilisés dans le module sans qualification.</span><span class="sxs-lookup"><span data-stu-id="e73bb-126">If an `Imports` statement does not include an alias name, elements defined within the imported namespace can be used in the module without qualification.</span></span> <span data-ttu-id="e73bb-127">Si le nom d’alias est spécifié, il doit être utilisé comme qualificateur pour les noms contenus dans cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e73bb-127">If the alias name is specified, it must be used as a qualifier for names contained within that namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e73bb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e73bb-128">See also</span></span>

- <xref:Microsoft.VisualBasic.ControlChars>
- <xref:Microsoft.VisualBasic>
- [<span data-ttu-id="e73bb-129">Espaces de noms dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e73bb-129">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="e73bb-130">Assemblys et le Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="e73bb-130">Assemblies and the Global Assembly Cache</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)
- [<span data-ttu-id="e73bb-131">Guide pratique pour créer et utiliser des assemblys à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e73bb-131">How to: Create and Use Assemblies Using the Command Line</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/how-to-create-and-use-assemblies-using-the-command-line.md)
- [<span data-ttu-id="e73bb-132">Imports (instruction) (espace de noms et type .NET)</span><span class="sxs-lookup"><span data-stu-id="e73bb-132">Imports Statement (.NET Namespace and Type)</span></span>](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
