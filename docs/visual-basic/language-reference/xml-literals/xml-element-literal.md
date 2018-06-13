---
title: Littéral d'élément XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralElement
helpviewer_keywords:
- XML element literal [Visual Basic]
- element literal [Visual Basic]
- XML literals [Visual Basic], element
ms.assetid: 95039642-7893-48b7-b23f-45a6c55d8f67
ms.openlocfilehash: 55d5d1410a65ea8c800bbd2b310907a6d6a61c61
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33605132"
---
# <a name="xml-element-literal-visual-basic"></a><span data-ttu-id="a457a-102">Littéral d'élément XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a457a-102">XML Element Literal (Visual Basic)</span></span>

<span data-ttu-id="a457a-103">Un littéral qui représente un <xref:System.Xml.Linq.XElement> objet.</span><span class="sxs-lookup"><span data-stu-id="a457a-103">A literal that represents an <xref:System.Xml.Linq.XElement> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a457a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a457a-104">Syntax</span></span>  
  
```xml  
<name [ attributeList ] />  
-or-  
<name [ attributeList ] > [ elementContents ] </[ name ]>  
```  
  
## <a name="parts"></a><span data-ttu-id="a457a-105">Composants</span><span class="sxs-lookup"><span data-stu-id="a457a-105">Parts</span></span>  
  
-   `<`  
  
     <span data-ttu-id="a457a-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a457a-106">Required.</span></span> <span data-ttu-id="a457a-107">Ouvre la balise d’élément initiale.</span><span class="sxs-lookup"><span data-stu-id="a457a-107">Opens the starting element tag.</span></span>  
  
-   `name`  
  
     <span data-ttu-id="a457a-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a457a-108">Required.</span></span> <span data-ttu-id="a457a-109">Nom de l'élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-109">Name of the element.</span></span> <span data-ttu-id="a457a-110">Le format est une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a457a-110">The format is one of the following:</span></span>  
  
    -   <span data-ttu-id="a457a-111">Texte littéral pour le nom de l’élément, sous la forme `[ePrefix:]eName`, où :</span><span class="sxs-lookup"><span data-stu-id="a457a-111">Literal text for the element name, of the form `[ePrefix:]eName`, where:</span></span>  
  
        |<span data-ttu-id="a457a-112">Élément</span><span class="sxs-lookup"><span data-stu-id="a457a-112">Part</span></span>|<span data-ttu-id="a457a-113">Description</span><span class="sxs-lookup"><span data-stu-id="a457a-113">Description</span></span>|  
        |---|---|  
        |`ePrefix`|<span data-ttu-id="a457a-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-114">Optional.</span></span> <span data-ttu-id="a457a-115">Préfixe d’espace de noms XML pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-115">XML namespace prefix for the element.</span></span> <span data-ttu-id="a457a-116">Doit être un espace de noms XML global défini avec un `Imports` instruction dans le fichier ou au niveau du projet, ou un espace de noms XML local défini dans cet élément ou un élément parent.</span><span class="sxs-lookup"><span data-stu-id="a457a-116">Must be a global XML namespace that is defined with an `Imports` statement in the file or at the project level, or a local XML namespace that is defined in this element or a parent element.</span></span>|  
        |`eName`|<span data-ttu-id="a457a-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a457a-117">Required.</span></span> <span data-ttu-id="a457a-118">Nom de l'élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-118">Name of the element.</span></span> <span data-ttu-id="a457a-119">Le format est une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a457a-119">The format is one of the following:</span></span><br /><br /> <span data-ttu-id="a457a-120">-Texte littéral.</span><span class="sxs-lookup"><span data-stu-id="a457a-120">-   Literal text.</span></span> <span data-ttu-id="a457a-121">Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-121">See [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span><br /><span data-ttu-id="a457a-122">-Incorporé expression sous la forme `<%= eNameExp %>`.</span><span class="sxs-lookup"><span data-stu-id="a457a-122">-   Embedded expression of the form `<%= eNameExp %>`.</span></span> <span data-ttu-id="a457a-123">Le type de `eNameExp` doit être `String` ou un type qui est implicitement convertible en <xref:System.Xml.Linq.XName>.</span><span class="sxs-lookup"><span data-stu-id="a457a-123">The type of `eNameExp` must be `String` or a type that is implicitly convertible to <xref:System.Xml.Linq.XName>.</span></span>|  
  
    -   <span data-ttu-id="a457a-124">Expression sous la forme incorporée `<%= nameExp %>`.</span><span class="sxs-lookup"><span data-stu-id="a457a-124">Embedded expression of the form `<%= nameExp %>`.</span></span> <span data-ttu-id="a457a-125">Le type de `nameExp` doit être `String` ou un type implicitement convertible en <xref:System.Xml.Linq.XName>.</span><span class="sxs-lookup"><span data-stu-id="a457a-125">The type of `nameExp` must be `String` or a type implicitly convertible to <xref:System.Xml.Linq.XName>.</span></span> <span data-ttu-id="a457a-126">Une expression incorporée n’est pas autorisée dans une balise de fermeture d’un élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-126">An embedded expression is not allowed in a closing tag of an element.</span></span>  
  
-   `attributeList`  
  
     <span data-ttu-id="a457a-127">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-127">Optional.</span></span> <span data-ttu-id="a457a-128">Liste d’attributs déclarés dans le littéral.</span><span class="sxs-lookup"><span data-stu-id="a457a-128">List of attributes declared in the literal.</span></span>  
  
     `attribute [ attribute ... ]`  
  
     <span data-ttu-id="a457a-129">Chaque `attribute` a l’une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a457a-129">Each `attribute` has one of the following syntaxes:</span></span>  
  
    -   <span data-ttu-id="a457a-130">Attribut d’affectation, sous la forme `[aPrefix:]aName=aValue`, où :</span><span class="sxs-lookup"><span data-stu-id="a457a-130">Attribute assignment, of the form `[aPrefix:]aName=aValue`, where:</span></span>  
  
        |<span data-ttu-id="a457a-131">Élément</span><span class="sxs-lookup"><span data-stu-id="a457a-131">Part</span></span>|<span data-ttu-id="a457a-132">Description</span><span class="sxs-lookup"><span data-stu-id="a457a-132">Description</span></span>|  
        |---|---|  
        |`aPrefix`|<span data-ttu-id="a457a-133">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-133">Optional.</span></span> <span data-ttu-id="a457a-134">Préfixe d’espace de noms XML pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="a457a-134">XML namespace prefix for the attribute.</span></span> <span data-ttu-id="a457a-135">Doit être un espace de noms XML global défini avec un `Imports` instruction ou un espace de noms XML local défini dans cet élément ou un élément parent.</span><span class="sxs-lookup"><span data-stu-id="a457a-135">Must be a global XML namespace that is defined with an `Imports` statement, or a local XML namespace that is defined in this element or a parent element.</span></span>|  
        |`aName`|<span data-ttu-id="a457a-136">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a457a-136">Required.</span></span> <span data-ttu-id="a457a-137">Nom de l'attribut.</span><span class="sxs-lookup"><span data-stu-id="a457a-137">Name of the attribute.</span></span> <span data-ttu-id="a457a-138">Le format est une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a457a-138">The format is one of the following:</span></span><br /><br /> <span data-ttu-id="a457a-139">-Texte littéral.</span><span class="sxs-lookup"><span data-stu-id="a457a-139">-   Literal text.</span></span> <span data-ttu-id="a457a-140">Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-140">See [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span><br /><span data-ttu-id="a457a-141">-Incorporé expression sous la forme `<%= aNameExp %>`.</span><span class="sxs-lookup"><span data-stu-id="a457a-141">-   Embedded expression of the form `<%= aNameExp %>`.</span></span> <span data-ttu-id="a457a-142">Le type de `aNameExp` doit être `String` ou un type qui est implicitement convertible en <xref:System.Xml.Linq.XName>.</span><span class="sxs-lookup"><span data-stu-id="a457a-142">The type of `aNameExp` must be `String` or a type that is implicitly convertible to <xref:System.Xml.Linq.XName>.</span></span>|  
        |`aValue`|<span data-ttu-id="a457a-143">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-143">Optional.</span></span> <span data-ttu-id="a457a-144">Valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="a457a-144">Value of the attribute.</span></span> <span data-ttu-id="a457a-145">Le format est une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a457a-145">The format is one of the following:</span></span><br /><br /> <span data-ttu-id="a457a-146">-Texte littéral, entourée guillemets.</span><span class="sxs-lookup"><span data-stu-id="a457a-146">-   Literal text, enclosed in quotation marks.</span></span><br /><span data-ttu-id="a457a-147">-Incorporé expression sous la forme `<%= aValueExp %>`.</span><span class="sxs-lookup"><span data-stu-id="a457a-147">-   Embedded expression of the form `<%= aValueExp %>`.</span></span> <span data-ttu-id="a457a-148">N’importe quel type est autorisé.</span><span class="sxs-lookup"><span data-stu-id="a457a-148">Any type is allowed.</span></span>|  
  
    -   <span data-ttu-id="a457a-149">Expression sous la forme incorporée `<%= aExp %>`.</span><span class="sxs-lookup"><span data-stu-id="a457a-149">Embedded expression of the form `<%= aExp %>`.</span></span>  
  
-   `/>`  
  
     <span data-ttu-id="a457a-150">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-150">Optional.</span></span> <span data-ttu-id="a457a-151">Indique que l’élément est un élément vide, sans contenu.</span><span class="sxs-lookup"><span data-stu-id="a457a-151">Indicates that the element is an empty element, without content.</span></span>  
  
-   `>`  
  
     <span data-ttu-id="a457a-152">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a457a-152">Required.</span></span> <span data-ttu-id="a457a-153">Met fin à la balise d’élément initiale ou vide.</span><span class="sxs-lookup"><span data-stu-id="a457a-153">Ends the beginning or empty element tag.</span></span>  
  
-   `elementContents`  
  
     <span data-ttu-id="a457a-154">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-154">Optional.</span></span> <span data-ttu-id="a457a-155">Contenu de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-155">Content of the element.</span></span>  
  
     `content [ content ... ]`  
  
     <span data-ttu-id="a457a-156">Chaque `content` peut prendre l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a457a-156">Each `content` can be one of the following:</span></span>  
  
    -   <span data-ttu-id="a457a-157">Texte littéral.</span><span class="sxs-lookup"><span data-stu-id="a457a-157">Literal text.</span></span> <span data-ttu-id="a457a-158">Tous les espaces blancs dans `elementContents` devient significatif si du texte littéral est.</span><span class="sxs-lookup"><span data-stu-id="a457a-158">All the white space in `elementContents` becomes significant if there is any literal text.</span></span>  
  
    -   <span data-ttu-id="a457a-159">Expression sous la forme incorporée `<%= contentExp %>`.</span><span class="sxs-lookup"><span data-stu-id="a457a-159">Embedded expression of the form `<%= contentExp %>`.</span></span>  
  
    -   <span data-ttu-id="a457a-160">Littéral d’élément XML.</span><span class="sxs-lookup"><span data-stu-id="a457a-160">XML element literal.</span></span>  
  
    -   <span data-ttu-id="a457a-161">Littéral de commentaire XML.</span><span class="sxs-lookup"><span data-stu-id="a457a-161">XML comment literal.</span></span> <span data-ttu-id="a457a-162">Consultez [littéral de commentaire XML](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-162">See [XML Comment Literal](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md).</span></span>  
  
    -   <span data-ttu-id="a457a-163">Instruction de traitement XML littéral.</span><span class="sxs-lookup"><span data-stu-id="a457a-163">XML processing instruction literal.</span></span> <span data-ttu-id="a457a-164">Consultez [littéral d’Instruction de traitement XML](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-164">See [XML Processing Instruction Literal](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md).</span></span>  
  
    -   <span data-ttu-id="a457a-165">Littéral CDATA XML.</span><span class="sxs-lookup"><span data-stu-id="a457a-165">XML CDATA literal.</span></span> <span data-ttu-id="a457a-166">Consultez [littéral CDATA XML](../../../visual-basic/language-reference/xml-literals/xml-cdata-literal.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-166">See [XML CDATA Literal](../../../visual-basic/language-reference/xml-literals/xml-cdata-literal.md).</span></span>  
  
-   `</[name]>`  
  
     <span data-ttu-id="a457a-167">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="a457a-167">Optional.</span></span> <span data-ttu-id="a457a-168">Représente la balise de fermeture de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-168">Represents the closing tag for the element.</span></span> <span data-ttu-id="a457a-169">Le paramètre facultatif `name` paramètre n’est pas autorisé lorsqu’il est le résultat d’une expression incorporée.</span><span class="sxs-lookup"><span data-stu-id="a457a-169">The optional `name` parameter is not allowed when it is the result of an embedded expression.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a457a-170">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a457a-170">Return Value</span></span>  
 <span data-ttu-id="a457a-171">Objet <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="a457a-171">An <xref:System.Xml.Linq.XElement> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a457a-172">Notes</span><span class="sxs-lookup"><span data-stu-id="a457a-172">Remarks</span></span>  
 <span data-ttu-id="a457a-173">Vous pouvez utiliser la syntaxe de littéral d’élément XML pour créer <xref:System.Xml.Linq.XElement> objets dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a457a-173">You can use the XML element literal syntax to create <xref:System.Xml.Linq.XElement> objects in your code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a457a-174">Un littéral XML peut couvrir plusieurs lignes sans utiliser de caractères de continuation de ligne.</span><span class="sxs-lookup"><span data-stu-id="a457a-174">An XML literal can span multiple lines without using line continuation characters.</span></span> <span data-ttu-id="a457a-175">Cette fonctionnalité vous permet de copier le contenu d’un document XML et le coller directement dans un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a457a-175">This feature enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="a457a-176">Les expressions incorporées du formulaire `<%= exp %>` vous permettent d’ajouter des informations dynamiques à un littéral d’élément XML.</span><span class="sxs-lookup"><span data-stu-id="a457a-176">Embedded expressions of the form `<%= exp %>` enable you to add dynamic information to an XML element literal.</span></span> <span data-ttu-id="a457a-177">Pour plus d’informations, consultez [Expressions incorporées en XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-177">For more information, see [Embedded Expressions in XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span></span>  
  
 <span data-ttu-id="a457a-178">Le compilateur Visual Basic convertit le littéral d’élément XML en appels à la <xref:System.Xml.Linq.XElement.%23ctor%2A> constructeur et, si nécessaire, le <xref:System.Xml.Linq.XAttribute.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="a457a-178">The Visual Basic compiler converts the XML element literal into calls to the <xref:System.Xml.Linq.XElement.%23ctor%2A> constructor and, if it is required, the <xref:System.Xml.Linq.XAttribute.%23ctor%2A> constructor.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="a457a-179">Espaces de noms XML</span><span class="sxs-lookup"><span data-stu-id="a457a-179">XML Namespaces</span></span>  
 <span data-ttu-id="a457a-180">Les préfixes d’espace de noms XML sont utiles lorsque vous avez besoin de créer des littéraux XML avec des éléments du même espace de noms plusieurs fois dans le code.</span><span class="sxs-lookup"><span data-stu-id="a457a-180">XML namespace prefixes are useful when you have to create XML literals with elements from the same namespace many times in code.</span></span> <span data-ttu-id="a457a-181">Vous pouvez utiliser les préfixes d’espace de noms XML globaux, que vous définissez à l’aide de la `Imports` instruction, ou les préfixes locaux, que vous définissez à l’aide de la `xmlns:xmlPrefix="xmlNamespace"` la syntaxe d’attribut.</span><span class="sxs-lookup"><span data-stu-id="a457a-181">You can use global XML namespace prefixes, which you define by using the `Imports` statement, or local prefixes, which you define by using the `xmlns:xmlPrefix="xmlNamespace"` attribute syntax.</span></span> <span data-ttu-id="a457a-182">Pour plus d’informations, consultez [Imports, instruction (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="a457a-182">For more information, see [Imports Statement (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span></span>  
  
 <span data-ttu-id="a457a-183">Conformément aux règles de portée pour les espaces de noms XML, les préfixes locaux sont prioritaires sur les préfixes globaux.</span><span class="sxs-lookup"><span data-stu-id="a457a-183">In accordance with the scoping rules for XML namespaces, local prefixes take precedence over global prefixes.</span></span> <span data-ttu-id="a457a-184">Toutefois, si un littéral XML définit un espace de noms XML, cet espace de noms n’est pas disponible pour les expressions qui apparaissent dans une expression incorporée.</span><span class="sxs-lookup"><span data-stu-id="a457a-184">However, if an XML literal defines an XML namespace, that namespace is not available to expressions that appear in an embedded expression.</span></span> <span data-ttu-id="a457a-185">L’expression incorporée peut accéder uniquement l’espace de noms XML global.</span><span class="sxs-lookup"><span data-stu-id="a457a-185">The embedded expression can access only the global XML namespace.</span></span>  
  
 <span data-ttu-id="a457a-186">Le compilateur Visual Basic convertit chaque espace de noms XML global utilisé par un littéral XML dans une définition d’espace de noms locale dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="a457a-186">The Visual Basic compiler converts each global XML namespace that is used by an XML literal into a one local namespace definition in the generated code.</span></span> <span data-ttu-id="a457a-187">Espaces de noms XML globaux qui ne sont pas utilisés n’apparaissent pas dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="a457a-187">Global XML namespaces that are not used do not appear in the generated code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a457a-188">Exemple</span><span class="sxs-lookup"><span data-stu-id="a457a-188">Example</span></span>  
 <span data-ttu-id="a457a-189">L’exemple suivant montre comment créer un élément XML simple qui a deux éléments vides imbriqués.</span><span class="sxs-lookup"><span data-stu-id="a457a-189">The following example shows how to create a simple XML element that has two nested empty elements.</span></span>  
  
 [!code-vb[VbXMLSamples#20](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-element-literal_1.vb)]  
  
 <span data-ttu-id="a457a-190">L’exemple affiche le texte suivant.</span><span class="sxs-lookup"><span data-stu-id="a457a-190">The example displays the following text.</span></span> <span data-ttu-id="a457a-191">Notez que le littéral conserve la structure des éléments vides.</span><span class="sxs-lookup"><span data-stu-id="a457a-191">Notice that the literal preserves the structure of the empty elements.</span></span>  
  
```xml  
<outer>  
  <inner1></inner1>  
  <inner2 />  
</outer>  
```  
  
## <a name="example"></a><span data-ttu-id="a457a-192">Exemple</span><span class="sxs-lookup"><span data-stu-id="a457a-192">Example</span></span>  
 <span data-ttu-id="a457a-193">L’exemple suivant montre comment utiliser des expressions incorporées pour nommer un élément et de créer des attributs.</span><span class="sxs-lookup"><span data-stu-id="a457a-193">The following example shows how to use embedded expressions to name an element and create attributes.</span></span>  
  
 [!code-vb[VbXMLSamples#21](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-element-literal_2.vb)]  
  
 <span data-ttu-id="a457a-194">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="a457a-194">This code displays the following text:</span></span>  
  
```xml  
<book isbn="1234" author="My Author" year="1999" title="My Book" />  
```  
  
## <a name="example"></a><span data-ttu-id="a457a-195">Exemple</span><span class="sxs-lookup"><span data-stu-id="a457a-195">Example</span></span>  
 <span data-ttu-id="a457a-196">L'exemple suivant déclare `ns` en tant que préfixe d'espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="a457a-196">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="a457a-197">Ensuite, il utilise le préfixe de l’espace de noms pour créer un littéral XML et affiche la forme finale de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-197">It then uses the prefix of the namespace to create an XML literal and displays the element's final form.</span></span>  
  
 [!code-vb[VbXMLSamples#22](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-element-literal_3.vb)]  
  
 <span data-ttu-id="a457a-198">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="a457a-198">This code displays the following text:</span></span>  
  
```xml  
<ns:outer xmlns:ns="http://SomeNamespace">  
  <ns:middle xmlns:ns="http://NewNamespace">  
    <ns:inner1 />  
    <inner2 xmlns="http://SomeNamespace" />  
  </ns:middle>  
</ns:outer>  
```  
  
 <span data-ttu-id="a457a-199">Notez que le compilateur a converti le préfixe d’espace de noms XML global dans une définition de préfixe pour l’espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="a457a-199">Notice that the compiler converted the prefix of the global XML namespace into a prefix definition for the XML namespace.</span></span> <span data-ttu-id="a457a-200">Le \<ns:middle > élément redéfinit le préfixe d’espace de noms XML pour le \<ns:inner1 > élément.</span><span class="sxs-lookup"><span data-stu-id="a457a-200">The \<ns:middle> element redefines the XML namespace prefix for the \<ns:inner1> element.</span></span> <span data-ttu-id="a457a-201">Toutefois, le \<ns:inner2 > élément utilise l’espace de noms défini par le `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="a457a-201">However, the \<ns:inner2> element uses the namespace defined by the `Imports` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a457a-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a457a-202">See Also</span></span>  
 <xref:System.Xml.Linq.XElement>  
 [<span data-ttu-id="a457a-203">Nom des attributs et des éléments XML déclarés</span><span class="sxs-lookup"><span data-stu-id="a457a-203">Names of Declared XML Elements and Attributes</span></span>](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)  
 [<span data-ttu-id="a457a-204">Littéraux de commentaires XML</span><span class="sxs-lookup"><span data-stu-id="a457a-204">XML Comment Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md)  
 [<span data-ttu-id="a457a-205">Littéral CDATA XML</span><span class="sxs-lookup"><span data-stu-id="a457a-205">XML CDATA Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-cdata-literal.md)  
 [<span data-ttu-id="a457a-206">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="a457a-206">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)  
 [<span data-ttu-id="a457a-207">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a457a-207">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [<span data-ttu-id="a457a-208">Expressions incorporées en XML</span><span class="sxs-lookup"><span data-stu-id="a457a-208">Embedded Expressions in XML</span></span>](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)  
 [<span data-ttu-id="a457a-209">Imports (instruction) (espace de noms XML)</span><span class="sxs-lookup"><span data-stu-id="a457a-209">Imports Statement (XML Namespace)</span></span>](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md)
