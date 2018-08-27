---
title: Imports, instruction - Namespace de .NET et de Type (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Imports
- imports
helpviewer_keywords:
- declared element names [Visual Basic], qualification
- imports [Visual Basic]
- Imports statement [Visual Basic]
- aliases [Visual Basic], Imports statement
- container elements [Visual Basic]
- namespaces [Visual Basic], importing
- Imports statement [Visual Basic], syntax
- import aliases [Visual Basic]
- aliases [Visual Basic], import
- declared elements [Visual Basic], container elements
ms.assetid: 7062f8aa-d890-4232-9eed-92836e13fb6e
ms.openlocfilehash: 0211438e8b4c02fead910dd7a32e0df9ed73ddc5
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925596"
---
# <a name="imports-statement-net-namespace-and-type"></a><span data-ttu-id="6ef22-102">Imports, instruction (espace de noms et type .NET)</span><span class="sxs-lookup"><span data-stu-id="6ef22-102">Imports Statement (.NET Namespace and Type)</span></span>
<span data-ttu-id="6ef22-103">Active les noms d’être référencés sans qualification d’espace de noms de type.</span><span class="sxs-lookup"><span data-stu-id="6ef22-103">Enables type names to be referenced without namespace qualification.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ef22-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ef22-104">Syntax</span></span>  
  
```  
Imports [ aliasname = ] namespace  
-or-  
Imports [ aliasname = ] namespace.element  
```  
  
## <a name="parts"></a><span data-ttu-id="6ef22-105">Composants</span><span class="sxs-lookup"><span data-stu-id="6ef22-105">Parts</span></span>  
  
|<span data-ttu-id="6ef22-106">Terme</span><span class="sxs-lookup"><span data-stu-id="6ef22-106">Term</span></span>|<span data-ttu-id="6ef22-107">Définition</span><span class="sxs-lookup"><span data-stu-id="6ef22-107">Definition</span></span>|  
|---|---|  
|`aliasname`|<span data-ttu-id="6ef22-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6ef22-108">Optional.</span></span> <span data-ttu-id="6ef22-109">Un *alias d’importation* ou le nom par lequel le code peut faire référence à `namespace` au lieu de la chaîne de qualification complète.</span><span class="sxs-lookup"><span data-stu-id="6ef22-109">An *import alias* or name by which code can refer to `namespace` instead of the full qualification string.</span></span> <span data-ttu-id="6ef22-110">Consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="6ef22-110">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>|  
|`namespace`|<span data-ttu-id="6ef22-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6ef22-111">Required.</span></span> <span data-ttu-id="6ef22-112">Le nom qualifié complet de l’espace de noms importé.</span><span class="sxs-lookup"><span data-stu-id="6ef22-112">The fully qualified name of the namespace being imported.</span></span> <span data-ttu-id="6ef22-113">Une chaîne d’espaces de noms imbriquée à n’importe quel niveau.</span><span class="sxs-lookup"><span data-stu-id="6ef22-113">Can be a string of namespaces nested to any level.</span></span>|  
|`element`|<span data-ttu-id="6ef22-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6ef22-114">Optional.</span></span> <span data-ttu-id="6ef22-115">Le nom d’un élément de programmation déclaré dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6ef22-115">The name of a programming element declared in the namespace.</span></span> <span data-ttu-id="6ef22-116">Peut être n’importe quel élément de conteneur.</span><span class="sxs-lookup"><span data-stu-id="6ef22-116">Can be any container element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6ef22-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6ef22-117">Remarks</span></span>  
 <span data-ttu-id="6ef22-118">La `Imports` instruction permet aux types qui sont contenus dans un espace de noms donné pour être référencé directement.</span><span class="sxs-lookup"><span data-stu-id="6ef22-118">The `Imports`  statement enables types that are contained in a given namespace to be referenced directly.</span></span>  
  
 <span data-ttu-id="6ef22-119">Vous pouvez fournir un nom d’espace de noms unique ou une chaîne d’espaces de noms imbriqués.</span><span class="sxs-lookup"><span data-stu-id="6ef22-119">You can supply a single namespace name or a string of nested namespaces.</span></span> <span data-ttu-id="6ef22-120">Chaque espace de noms imbriqué est séparé de l’espace de noms au niveau supérieur suivant par une période (`.`), comme l’illustre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6ef22-120">Each nested namespace is separated from the next higher level namespace by a period (`.`), as the following example illustrates.</span></span>  
  
 `Imports System.Collections.Generic`  
  
 <span data-ttu-id="6ef22-121">Chaque fichier source peut contenir un nombre quelconque de `Imports` instructions.</span><span class="sxs-lookup"><span data-stu-id="6ef22-121">Each source file can contain any number of `Imports` statements.</span></span> <span data-ttu-id="6ef22-122">Ces derniers doivent respecter les déclarations d’option, tel que le `Option Strict` instruction et elles doivent précéder les déclarations d’élément de programmation, telles que `Module` ou `Class` instructions.</span><span class="sxs-lookup"><span data-stu-id="6ef22-122">These must follow any option declarations, such as the `Option Strict` statement, and they must precede any programming element declarations, such as `Module` or `Class` statements.</span></span>  
  
 <span data-ttu-id="6ef22-123">Vous pouvez utiliser `Imports` uniquement au niveau fichier.</span><span class="sxs-lookup"><span data-stu-id="6ef22-123">You can use `Imports` only at file level.</span></span> <span data-ttu-id="6ef22-124">Cela signifie que le contexte de déclaration pour l’importation doit être un fichier source et ne peut pas être un espace de noms, classe, structure, module, interface, procédure ou bloc.</span><span class="sxs-lookup"><span data-stu-id="6ef22-124">This means the declaration context for importation must be a source file, and cannot be a namespace, class, structure, module, interface, procedure, or block.</span></span>  
  
 <span data-ttu-id="6ef22-125">Notez que la `Imports` instruction ne rend pas les éléments à partir d’autres projets et assemblys disponibles à votre projet.</span><span class="sxs-lookup"><span data-stu-id="6ef22-125">Note that the `Imports` statement does not make elements from other projects and assemblies available to your project.</span></span> <span data-ttu-id="6ef22-126">L’importation ne prend pas la place de la définition d’une référence.</span><span class="sxs-lookup"><span data-stu-id="6ef22-126">Importing does not take the place of setting a reference.</span></span> <span data-ttu-id="6ef22-127">Elle supprime uniquement la nécessité pour qualifier des noms qui sont déjà disponibles pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="6ef22-127">It only removes the need to qualify names that are already available to your project.</span></span> <span data-ttu-id="6ef22-128">Pour plus d’informations, consultez « Importation d’éléments conteneurs » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span><span class="sxs-lookup"><span data-stu-id="6ef22-128">For more information, see "Importing Containing Elements" in [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6ef22-129">Vous pouvez définir implicite `Imports` instructions à l’aide de la [Page références, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="6ef22-129">You can define implicit `Imports` statements by using the [References Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic).</span></span> <span data-ttu-id="6ef22-130">Pour plus d’informations, consultez [Comment : ajouter ou supprimer des espaces de noms importés (Visual Basic)](/visualstudio/ide/how-to-add-or-remove-imported-namespaces-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="6ef22-130">For more information, see [How to: Add or Remove Imported Namespaces (Visual Basic)](/visualstudio/ide/how-to-add-or-remove-imported-namespaces-visual-basic).</span></span>  
  
## <a name="import-aliases"></a><span data-ttu-id="6ef22-131">Alias d’importation</span><span class="sxs-lookup"><span data-stu-id="6ef22-131">Import Aliases</span></span>  
 <span data-ttu-id="6ef22-132">Un *alias d’importation* définit l’alias pour un espace de noms ou un type.</span><span class="sxs-lookup"><span data-stu-id="6ef22-132">An *import alias* defines the alias for a namespace or type.</span></span> <span data-ttu-id="6ef22-133">Alias d’importation sont utiles lorsque vous avez besoin d’utiliser des éléments portant le même nom sont déclarées dans un ou plusieurs espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="6ef22-133">Import aliases are useful when you need to use items with the same name that are declared in one or more namespaces.</span></span> <span data-ttu-id="6ef22-134">Pour plus d’informations et un exemple, consultez « Qualification d’un nom d’élément » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span><span class="sxs-lookup"><span data-stu-id="6ef22-134">For more information and an example, see "Qualifying an Element Name" in [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>  
  
 <span data-ttu-id="6ef22-135">Vous ne devez pas déclarer un membre au niveau du module avec le même nom que `aliasname`.</span><span class="sxs-lookup"><span data-stu-id="6ef22-135">You should not declare a member at module level with the same name as `aliasname`.</span></span> <span data-ttu-id="6ef22-136">Si vous le faites, le compilateur Visual Basic utilise `aliasname` uniquement pour le membre déclaré et n’est plus le reconnaît comme un alias d’importation.</span><span class="sxs-lookup"><span data-stu-id="6ef22-136">If you do, the Visual Basic compiler uses `aliasname` only for the declared member and no longer recognizes it as an import alias.</span></span>  
  
 <span data-ttu-id="6ef22-137">Bien que la syntaxe utilisée pour déclarer un alias d’importation est utilisée comme celle-ci pour l’importation d’un préfixe d’espace de noms XML, les résultats sont différents.</span><span class="sxs-lookup"><span data-stu-id="6ef22-137">Although the syntax used for declaring an import alias is like that used for importing an XML namespace prefix, the results are different.</span></span> <span data-ttu-id="6ef22-138">Un alias d’importation peut être utilisé en tant qu’expression dans votre code, tandis qu’un préfixe d’espace de noms XML peut être utilisé uniquement dans les littéraux XML ou les propriétés d’axe XML comme préfixe pour un élément qualifié ou un nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="6ef22-138">An import alias can be used as an expression in your code, whereas an XML namespace prefix can be used only in XML literals or XML axis properties as the prefix for a qualified element or attribute name.</span></span>  
  
### <a name="element-names"></a><span data-ttu-id="6ef22-139">Noms des éléments</span><span class="sxs-lookup"><span data-stu-id="6ef22-139">Element Names</span></span>  
 <span data-ttu-id="6ef22-140">Si vous fournissez `element`, il doit représenter un *élément conteneur*, autrement dit, un élément de programmation qui permettre contenir d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="6ef22-140">If you supply `element`, it must represent a *container element*, that is, a programming element that can contain other elements.</span></span> <span data-ttu-id="6ef22-141">Éléments conteneurs incluent les classes, structures, modules, interfaces et énumérations.</span><span class="sxs-lookup"><span data-stu-id="6ef22-141">Container elements include classes, structures, modules, interfaces, and enumerations.</span></span>  
  
 <span data-ttu-id="6ef22-142">La portée des éléments mis à disposition par un `Imports` instruction varie selon que vous spécifiez `element`.</span><span class="sxs-lookup"><span data-stu-id="6ef22-142">The scope of the elements made available by an `Imports` statement depends on whether you specify `element`.</span></span> <span data-ttu-id="6ef22-143">Si vous spécifiez uniquement `namespace`, tous les identifie de façon unique nommé membres de cet espace de noms et d’éléments de conteneur au sein de cet espace de noms, sont disponibles sans qualification.</span><span class="sxs-lookup"><span data-stu-id="6ef22-143">If you specify only `namespace`, all uniquely named members of that namespace, and members of container elements within that namespace, are available without qualification.</span></span> <span data-ttu-id="6ef22-144">Si vous spécifiez à la fois `namespace` et `element`, seuls les membres de cet élément sont disponibles sans qualification.</span><span class="sxs-lookup"><span data-stu-id="6ef22-144">If you specify both `namespace` and `element`, only the members of that element are available without qualification.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6ef22-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ef22-145">Example</span></span>  
 <span data-ttu-id="6ef22-146">L’exemple suivant retourne tous les dossiers dans le répertoire C:\ à l’aide de la <xref:System.IO.DirectoryInfo> classe.</span><span class="sxs-lookup"><span data-stu-id="6ef22-146">The following example returns all the folders in the C:\ directory by using the <xref:System.IO.DirectoryInfo> class.</span></span>  
  
 <span data-ttu-id="6ef22-147">Le code n’a aucun `Imports` instructions en haut du fichier.</span><span class="sxs-lookup"><span data-stu-id="6ef22-147">The code has no `Imports` statements at the top of the file.</span></span> <span data-ttu-id="6ef22-148">Par conséquent, le `DirectoryInfo`, <xref:System.Text.StringBuilder>, et <xref:Microsoft.VisualBasic.ControlChars.CrLf> références sont entièrement qualifiées avec les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="6ef22-148">Therefore, the `DirectoryInfo`, <xref:System.Text.StringBuilder>, and <xref:Microsoft.VisualBasic.ControlChars.CrLf> references are all fully qualified with the namespaces.</span></span>  
  
 [!code-vb[VbVbalrStatements#152](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="6ef22-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ef22-149">Example</span></span>  
 <span data-ttu-id="6ef22-150">L’exemple suivant inclut `Imports` instructions pour les espaces de noms référencé.</span><span class="sxs-lookup"><span data-stu-id="6ef22-150">The following example includes `Imports` statements for the referenced namespaces.</span></span> <span data-ttu-id="6ef22-151">Par conséquent, les types n’ont pas à être complet avec les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="6ef22-151">Therefore, the types do not have to be fully qualified with the namespaces.</span></span>  
  
 [!code-vb[VbVbalrStatements#153](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_2.vb)]  
  
 [!code-vb[VbVbalrStatements#154](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_3.vb)]  
  
## <a name="example"></a><span data-ttu-id="6ef22-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ef22-152">Example</span></span>  
 <span data-ttu-id="6ef22-153">L’exemple suivant inclut `Imports` instructions qui créent des alias pour les espaces de noms référencé.</span><span class="sxs-lookup"><span data-stu-id="6ef22-153">The following example includes `Imports` statements that create aliases for the referenced namespaces.</span></span> <span data-ttu-id="6ef22-154">Les types sont qualifiées avec l’alias.</span><span class="sxs-lookup"><span data-stu-id="6ef22-154">The types are qualified with the aliases.</span></span>  
  
 [!code-vb[VbVbalrStatements#155](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_4.vb)]  
  
 [!code-vb[VbVbalrStatements#156](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_5.vb)]  
  
## <a name="example"></a><span data-ttu-id="6ef22-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ef22-155">Example</span></span>  
 <span data-ttu-id="6ef22-156">L’exemple suivant inclut `Imports` instructions qui créent des alias pour les types référencés.</span><span class="sxs-lookup"><span data-stu-id="6ef22-156">The following example includes `Imports` statements that create aliases for the referenced types.</span></span> <span data-ttu-id="6ef22-157">Alias sont utilisés pour spécifier les types.</span><span class="sxs-lookup"><span data-stu-id="6ef22-157">Aliases are used to specify the types.</span></span>  
  
 [!code-vb[VbVbalrStatements#157](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_6.vb)]  
  
 [!code-vb[VbVbalrStatements#158](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/imports-statement-net-namespace-and-type_7.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="6ef22-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ef22-158">See Also</span></span>  
 [<span data-ttu-id="6ef22-159">Namespace (instruction)</span><span class="sxs-lookup"><span data-stu-id="6ef22-159">Namespace Statement</span></span>](../../../visual-basic/language-reference/statements/namespace-statement.md)  
 [<span data-ttu-id="6ef22-160">Espaces de noms dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6ef22-160">Namespaces in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/namespaces.md)  
 [<span data-ttu-id="6ef22-161">Références et l’instruction Imports</span><span class="sxs-lookup"><span data-stu-id="6ef22-161">References and the Imports Statement</span></span>](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)  
 [<span data-ttu-id="6ef22-162">Imports (instruction) (espace de noms XML)</span><span class="sxs-lookup"><span data-stu-id="6ef22-162">Imports Statement (XML Namespace)</span></span>](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md)  
 [<span data-ttu-id="6ef22-163">Références aux éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="6ef22-163">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
