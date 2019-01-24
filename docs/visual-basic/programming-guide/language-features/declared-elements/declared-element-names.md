---
title: Noms d'éléments déclarés (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- declared elements [Visual Basic], case sensitivity
- names [Visual Basic], Visual Basic rules
- naming conventions [Visual Basic]
- element names [Visual Basic]
- declared elements [Visual Basic], identifiers
- declarations [Visual Basic], elements
- declared elements [Visual Basic], valid names
- '[] escape characters [Visual Basic]'
- names [Visual Basic], elements
- declaration statements [Visual Basic], declared elements
- declaring elements [Visual Basic]
- identifiers [Visual Basic], declared elements
- case sensitivity, declared element names
- escape characters [Visual Basic]
- names [Visual Basic], declared elements
- declared elements [Visual Basic], about declared elements
- escaped names [Visual Basic]
- declared elements [Visual Basic], names
- names [Visual Basic], naming conventions
- identifiers [Visual Basic], elements
ms.assetid: 09d8843b-c0dc-4afe-9dab-87c439a69e66
ms.openlocfilehash: 5311bba92043d3fded34a5d9337b6af13e213d4a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573385"
---
# <a name="declared-element-names-visual-basic"></a><span data-ttu-id="ddb5b-102">Noms d'éléments déclarés (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ddb5b-102">Declared Element Names (Visual Basic)</span></span>
<span data-ttu-id="ddb5b-103">Chaque élément déclaré a un nom, également appelé un *identificateur*, qui est utilisé par le code pour faire référence à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-103">Every declared element has a name, also called an *identifier*, which is what the code uses to refer to it.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="ddb5b-104">Règles</span><span class="sxs-lookup"><span data-stu-id="ddb5b-104">Rules</span></span>  
 <span data-ttu-id="ddb5b-105">Un nom d’élément dans Visual Basic doit respecter les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddb5b-105">An element name in Visual Basic must observe the following rules:</span></span>  
  
-   <span data-ttu-id="ddb5b-106">Il doit commencer par un caractère alphabétique ou un trait de soulignement (`_`).</span><span class="sxs-lookup"><span data-stu-id="ddb5b-106">It must begin with an alphabetic character or an underscore (`_`).</span></span>  
  
-   <span data-ttu-id="ddb5b-107">Il doit uniquement contenir des caractères alphabétiques, des chiffres décimaux et des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-107">It must only contain alphabetic characters, decimal digits, and underscores.</span></span>  
  
-   <span data-ttu-id="ddb5b-108">Il doit contenir au moins un caractère alphabétique ou un chiffre décimal s’il commence par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-108">It must contain at least one alphabetic character or decimal digit if it begins with an underscore.</span></span>  
  
-   <span data-ttu-id="ddb5b-109">Il ne doit pas être plus de 1023 caractères.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-109">It must not be more than 1023 characters long.</span></span>  
  
 <span data-ttu-id="ddb5b-110">La longueur maximale de 1023 caractères s’applique également à la chaîne entière d’un nom qualifié complet, tel que `outerNamespace.middleNamespace.innerNamespace.thisClass.thisElement`.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-110">The length limit of 1023 characters also applies to the entire string of a fully qualified name, such as `outerNamespace.middleNamespace.innerNamespace.thisClass.thisElement`.</span></span>  
  
 <span data-ttu-id="ddb5b-111">L’exemple suivant montre certains noms d’élément valide.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-111">The following example shows some valid element names.</span></span>  
  
 `aB123__45`  
  
 `_567`  
  
 <span data-ttu-id="ddb5b-112">L’exemple suivant montre certains noms d’élément non valide.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-112">The following example shows some invalid element names.</span></span> <span data-ttu-id="ddb5b-113">Le premier contient uniquement un trait de soulignement, le second commence par un chiffre décimal et le troisième contient un caractère non valide ($).</span><span class="sxs-lookup"><span data-stu-id="ddb5b-113">The first contains only an underscore, the second begins with a decimal digit, and the third contains an invalid character ($).</span></span>  
  
 `' Three INVALID element names`  
  
 `_`  
  
 `12ABC`  
  
 `xyz$wv`  
  
> [!CAUTION]
>  <span data-ttu-id="ddb5b-114">Les noms d’élément commençant par un trait de soulignement (`_`) ne font pas partie de la [indépendance du langage et composants indépendants du langage](../../../../standard/language-independence-and-language-independent-components.md) (CLS), le code conforme CLS ne peut pas utiliser un composant qui définit les noms de ce type.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-114">Element names starting with an underscore (`_`) are not part of the [Language Independence and Language-Independent Components](../../../../standard/language-independence-and-language-independent-components.md) (CLS), so CLS-compliant code cannot use a component that defines such names.</span></span> <span data-ttu-id="ddb5b-115">Toutefois, un trait de soulignement dans n’importe quelle autre position dans un nom d’élément est conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-115">However, an underscore in any other position in an element name is CLS-compliant.</span></span>  
  
### <a name="name-length-guidelines"></a><span data-ttu-id="ddb5b-116">Instructions de longueur de nom</span><span class="sxs-lookup"><span data-stu-id="ddb5b-116">Name Length Guidelines</span></span>  
 <span data-ttu-id="ddb5b-117">Dans la pratique, votre nom doit être aussi courte que possible tout en identifiant clairement la nature de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-117">As a practical matter, your name should be as short as possible while still clearly identifying the nature of the element.</span></span> <span data-ttu-id="ddb5b-118">Cela améliore la lisibilité de votre code et réduit la taille de ligne de longueur et le fichier source.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-118">This improves the readability of your code and reduces line length and source-file size.</span></span>  
  
 <span data-ttu-id="ddb5b-119">En revanche, votre nom ne doit pas être si court que ne pas correctement décrit ce que l’élément représente et comment votre code l’utilise.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-119">On the other hand, your name should not be so short that it does not adequately describe what the element represents and how your code uses it.</span></span> <span data-ttu-id="ddb5b-120">Ceci est important pour la lisibilité de votre code.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-120">This is important for the readability of your code.</span></span> <span data-ttu-id="ddb5b-121">Si quelqu'un d’autre tente de le comprendre, ou si vous avez vous-même l’observer beaucoup de temps après que l’avoir écrit, noms d’éléments appropriés peuvent enregistrer un temps considérable.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-121">If somebody else is trying to understand it, or if you yourself are looking at it a long time after you wrote it, suitable element names can save a considerable amount of time.</span></span>  
  
## <a name="escaped-names"></a><span data-ttu-id="ddb5b-122">Noms d’échappement</span><span class="sxs-lookup"><span data-stu-id="ddb5b-122">Escaped Names</span></span>  
 <span data-ttu-id="ddb5b-123">En règle générale, un nom d’élément doit correspond à aucun des mots clés réservés par Visual Basic, tel que `Case` ou `Friend`.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-123">Generally, an element name must not match any of the keywords reserved by Visual Basic, such as `Case` or `Friend`.</span></span> <span data-ttu-id="ddb5b-124">Toutefois, vous pouvez définir un *nom échappement*, qui est placé entre crochets (`[ ]`).</span><span class="sxs-lookup"><span data-stu-id="ddb5b-124">However, you can define an *escaped name*, which is enclosed by brackets (`[ ]`).</span></span> <span data-ttu-id="ddb5b-125">Un nom d’échappement peut correspondre à n’importe quel mot clé Visual Basic, dans la mesure où les crochets supprimer toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-125">An escaped name can match any Visual Basic keyword, since the brackets remove any ambiguity.</span></span> <span data-ttu-id="ddb5b-126">Vous utilisez également les crochets lorsque vous faites référence au nom ultérieurement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-126">You also use the brackets when you refer to the name later in your code.</span></span>  
  
 <span data-ttu-id="ddb5b-127">En règle générale, vous devez utiliser des noms échappés uniquement lorsque :</span><span class="sxs-lookup"><span data-stu-id="ddb5b-127">In general, you should use escaped names only when:</span></span>  
  
-   <span data-ttu-id="ddb5b-128">Votre code a migré à partir d’une version antérieure de Visual Basic qui n’a pas réservé le mot clé utilisé en tant que nom ; ou</span><span class="sxs-lookup"><span data-stu-id="ddb5b-128">Your code has migrated from a previous version of Visual Basic that did not reserve the keyword being used as a name; or</span></span>  
  
-   <span data-ttu-id="ddb5b-129">Vous travaillez avec le code écrit dans un autre langage dans lequel le mot clé donné n’est pas réservé.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-129">You are working with code written in another language in which the given keyword is not reserved.</span></span>  
  
 <span data-ttu-id="ddb5b-130">Sinon, vous devez envisager de renommer l’élément si son nom est en conflit avec un mot clé.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-130">Otherwise, you should consider renaming the element if its name conflicts with a keyword.</span></span> <span data-ttu-id="ddb5b-131">L’environnement de développement intégré (IDE) fournit un moyen simple de le faire.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-131">The integrated development environment (IDE) provides an easy way to do this.</span></span> <span data-ttu-id="ddb5b-132">Pour plus d’informations, consultez [Refactoring](/visualstudio/vb-ide/refactoring-vb).</span><span class="sxs-lookup"><span data-stu-id="ddb5b-132">For more information, see [Refactoring](/visualstudio/vb-ide/refactoring-vb).</span></span>  
  
## <a name="case-sensitivity-in-names"></a><span data-ttu-id="ddb5b-133">Respecte la casse dans les noms</span><span class="sxs-lookup"><span data-stu-id="ddb5b-133">Case Sensitivity in Names</span></span>  
 <span data-ttu-id="ddb5b-134">Noms d’éléments dans Visual Basic respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-134">Element names in Visual Basic are case-insensitive.</span></span> <span data-ttu-id="ddb5b-135">Cela signifie que lorsque le compilateur compare deux noms qui diffèrent uniquement par la casse des lettres, il les interprète comme le même nom.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-135">This means that when the compiler compares two names that differ in alphabetic case only, it interprets them as the same name.</span></span> <span data-ttu-id="ddb5b-136">Par exemple, il considère que `ABC` et `abc` font référence au même élément déclaré.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-136">For example, it considers `ABC` and `abc` to refer to the same declared element.</span></span>  
  
 <span data-ttu-id="ddb5b-137">Toutefois, le common language runtime (CLR) utilise la liaison de la casse.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-137">However, the common language runtime (CLR) uses case-sensitive binding.</span></span> <span data-ttu-id="ddb5b-138">Ainsi, quand vous générez un assembly ou une DLL et que vous le mettez à disposition d’autres assemblys, la casse de vos noms est respectée.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-138">Therefore, when you produce an assembly or a DLL and make it available to other assemblies, your names are no longer case-insensitive.</span></span> <span data-ttu-id="ddb5b-139">Par exemple, si vous définissez une classe avec un élément nommé `ABC`et que d’autres assemblys utilisent votre classe par le biais du Common Language Runtime, ils doivent faire référence à l’élément en tant que `ABC`.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-139">For example, if you define a class with an element called `ABC`, and other assemblies make use of your class through the common language runtime, they must refer to the element as `ABC`.</span></span> <span data-ttu-id="ddb5b-140">Si vous recompilez votre classe par la suite et modifier le nom de l’élément à `abc`, les autres assemblys utilisent votre classe peuvent ne plus accéder à cet élément.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-140">If you subsequently recompile your class and change the element's name to `abc`, the other assemblies using your class could no longer access that element.</span></span> <span data-ttu-id="ddb5b-141">Ainsi, quand vous publiez une version mise à jour d’un assembly, vous ne devez pas modifier la casse des éléments publics.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-141">Therefore, when you release an updated version of an assembly, you should not change the alphabetic case of any public elements.</span></span>  
  
## <a name="names-and-locales"></a><span data-ttu-id="ddb5b-142">Noms et paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="ddb5b-142">Names and Locales</span></span>  
 <span data-ttu-id="ddb5b-143">Comparaison des noms est indépendante des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-143">Comparison of names is independent of locale.</span></span> <span data-ttu-id="ddb5b-144">Si deux noms correspondent dans des paramètres régionaux, ils sont garanties à faire correspondre dans tous les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-144">If two names match in one locale, they are guaranteed to match in all locales.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddb5b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddb5b-145">See also</span></span>
- [<span data-ttu-id="ddb5b-146">Éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="ddb5b-146">Declared Elements</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/index.md)
- [<span data-ttu-id="ddb5b-147">Caractéristiques d’éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="ddb5b-147">Declared Element Characteristics</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)
- [<span data-ttu-id="ddb5b-148">Références aux éléments déclarés</span><span class="sxs-lookup"><span data-stu-id="ddb5b-148">References to Declared Elements</span></span>](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [<span data-ttu-id="ddb5b-149">Instructions</span><span class="sxs-lookup"><span data-stu-id="ddb5b-149">Statements</span></span>](../../../../visual-basic/language-reference/statements/index.md)
