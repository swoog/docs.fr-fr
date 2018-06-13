---
title: Propriété d'axe d'attribut XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyAttributeAxis
helpviewer_keywords:
- attribute axis property [Visual Basic]
- Visual Basic code, accessing XML
- XML attribute axis property [Visual Basic]
- XML axis [Visual Basic], attribute
- XML [Visual Basic], accessing
ms.assetid: 7a4777e1-0618-4de9-9510-fb9ace2bf4db
ms.openlocfilehash: 3e02fd2ddc3928bdd2e9741737fc31fb2b16901c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604911"
---
# <a name="xml-attribute-axis-property-visual-basic"></a><span data-ttu-id="1f334-102">Propriété d'axe d'attribut XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1f334-102">XML Attribute Axis Property (Visual Basic)</span></span>
<span data-ttu-id="1f334-103">Fournit l’accès à la valeur d’un attribut pour un <xref:System.Xml.Linq.XElement> objet ou au premier élément dans une collection de <xref:System.Xml.Linq.XElement> objets.</span><span class="sxs-lookup"><span data-stu-id="1f334-103">Provides access to the value of an attribute for an <xref:System.Xml.Linq.XElement> object or to the first element in a collection of <xref:System.Xml.Linq.XElement> objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f334-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f334-104">Syntax</span></span>  
  
```  
      object.@attribute  
-or-  
object.@<attribute>  
```  
  
## <a name="parts"></a><span data-ttu-id="1f334-105">Composants</span><span class="sxs-lookup"><span data-stu-id="1f334-105">Parts</span></span>  
 `object`  
 <span data-ttu-id="1f334-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1f334-106">Required.</span></span> <span data-ttu-id="1f334-107">Un <xref:System.Xml.Linq.XElement> objet ou une collection de <xref:System.Xml.Linq.XElement> objets.</span><span class="sxs-lookup"><span data-stu-id="1f334-107">An <xref:System.Xml.Linq.XElement> object or a collection of <xref:System.Xml.Linq.XElement> objects.</span></span>  
  
 <span data-ttu-id="1f334-108">.@</span><span class="sxs-lookup"><span data-stu-id="1f334-108">.@</span></span>  
 <span data-ttu-id="1f334-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1f334-109">Required.</span></span> <span data-ttu-id="1f334-110">Indique le début de la propriété d’axe d’attribut.</span><span class="sxs-lookup"><span data-stu-id="1f334-110">Denotes the start of an attribute axis property.</span></span>  
  
 <  
 <span data-ttu-id="1f334-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f334-111">Optional.</span></span> <span data-ttu-id="1f334-112">Indique le début du nom de l’attribut lorsque `attribute` n’est pas un identificateur valide en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1f334-112">Denotes the beginning of the name of the attribute when `attribute` is not a valid identifier in Visual Basic.</span></span>  
  
 `attribute`  
 <span data-ttu-id="1f334-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1f334-113">Required.</span></span> <span data-ttu-id="1f334-114">Nom de l’attribut à laquelle accéder, sous la forme [`prefix`:]`name`.</span><span class="sxs-lookup"><span data-stu-id="1f334-114">Name of the attribute to access, of the form [`prefix`:]`name`.</span></span>  
  
|<span data-ttu-id="1f334-115">Élément</span><span class="sxs-lookup"><span data-stu-id="1f334-115">Part</span></span>|<span data-ttu-id="1f334-116">Description</span><span class="sxs-lookup"><span data-stu-id="1f334-116">Description</span></span>|  
|----------|-----------------|  
|`prefix`|<span data-ttu-id="1f334-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f334-117">Optional.</span></span> <span data-ttu-id="1f334-118">Préfixe d’espace de noms XML pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="1f334-118">XML namespace prefix for the attribute.</span></span> <span data-ttu-id="1f334-119">Doit être un espace de noms XML global défini avec une instruction `Imports`.</span><span class="sxs-lookup"><span data-stu-id="1f334-119">Must be a global XML namespace defined with an `Imports` statement.</span></span>|  
|`name`|<span data-ttu-id="1f334-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1f334-120">Required.</span></span> <span data-ttu-id="1f334-121">Nom d’attribut local.</span><span class="sxs-lookup"><span data-stu-id="1f334-121">Local attribute name.</span></span> <span data-ttu-id="1f334-122">Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1f334-122">See [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span>|  
  
 \>  
 <span data-ttu-id="1f334-123">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f334-123">Optional.</span></span> <span data-ttu-id="1f334-124">Indique la fin du nom de l’attribut lorsque `attribute` n’est pas un identificateur valide en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1f334-124">Denotes the end of the name of the attribute when `attribute` is not a valid identifier in Visual Basic.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1f334-125">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1f334-125">Return Value</span></span>  
 <span data-ttu-id="1f334-126">Chaîne qui contient la valeur de `attribute`.</span><span class="sxs-lookup"><span data-stu-id="1f334-126">A string that contains the value of `attribute`.</span></span> <span data-ttu-id="1f334-127">Si le nom d’attribut n’existe pas, `Nothing` est retourné.</span><span class="sxs-lookup"><span data-stu-id="1f334-127">If the attribute name does not exist, `Nothing` is returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1f334-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1f334-128">Remarks</span></span>  
 <span data-ttu-id="1f334-129">Vous pouvez utiliser une propriété d’axe XML attribut pour accéder à la valeur d’un attribut par nom d’un <xref:System.Xml.Linq.XElement> objet ou du premier élément dans une collection de <xref:System.Xml.Linq.XElement> objets.</span><span class="sxs-lookup"><span data-stu-id="1f334-129">You can use an XML attribute axis property to access the value of an attribute by name from an <xref:System.Xml.Linq.XElement> object or from the first element in a collection of <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="1f334-130">Vous pouvez récupérer une valeur d’attribut par nom ou ajouter un nouvel attribut à un élément en spécifiant un nouveau nom précédé par l’identificateur @.</span><span class="sxs-lookup"><span data-stu-id="1f334-130">You can retrieve an attribute value by name, or add a new attribute to an element by specifying a new name preceded by the @ identifier.</span></span>  
  
 <span data-ttu-id="1f334-131">Lorsque vous faites référence à un attribut XML à l’aide de l’identificateur @, la valeur d’attribut est retournée sous forme de chaîne et vous n’avez pas besoin de spécifier explicitement le <xref:System.Xml.Linq.XAttribute.Value%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="1f334-131">When you refer to an XML attribute using the @ identifier, the attribute value is returned as a string and you do not need to explicitly specify the <xref:System.Xml.Linq.XAttribute.Value%2A> property.</span></span>  
  
 <span data-ttu-id="1f334-132">Les règles d’affectation de noms pour les attributs XML diffèrent des règles d’affectation de noms des identificateurs de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1f334-132">The naming rules for XML attributes differ from the naming rules for Visual Basic identifiers.</span></span> <span data-ttu-id="1f334-133">Pour accéder à un attribut XML qui a un nom qui n’est pas un identificateur Visual Basic valid, placez le nom entre crochets pointus (\< et >).</span><span class="sxs-lookup"><span data-stu-id="1f334-133">To access an XML attribute that has a name that is not a valid Visual Basic identifier, enclose the name in angle brackets (\< and >).</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="1f334-134">Espaces de noms XML</span><span class="sxs-lookup"><span data-stu-id="1f334-134">XML Namespaces</span></span>  
 <span data-ttu-id="1f334-135">Le nom de la propriété d’axe d’attribut peut utiliser uniquement des préfixes d’espace de noms XML, déclarés globalement à l’aide de la `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="1f334-135">The name in an attribute axis property can use only XML namespace prefixes declared globally by using the `Imports` statement.</span></span> <span data-ttu-id="1f334-136">Il ne peut pas utiliser des préfixes d'espace de noms XML déclarés localement dans des littéraux d'éléments XML.</span><span class="sxs-lookup"><span data-stu-id="1f334-136">It cannot use XML namespace prefixes declared locally within XML element literals.</span></span> <span data-ttu-id="1f334-137">Pour plus d’informations, consultez [Imports, instruction (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="1f334-137">For more information, see [Imports Statement (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1f334-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f334-138">Example</span></span>  
 <span data-ttu-id="1f334-139">L’exemple suivant montre comment obtenir les valeurs des attributs XML nommés `type` à partir d’une collection d’éléments XML qui sont nommées `phone`.</span><span class="sxs-lookup"><span data-stu-id="1f334-139">The following example shows how to get the values of the XML attributes named `type` from a collection of XML elements that are named `phone`.</span></span>  
  
 [!code-vb[VbXMLSamples#12](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-attribute-axis-property_1.vb)]  
  
 <span data-ttu-id="1f334-140">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1f334-140">This code displays the following text:</span></span>  
  
 `<phoneTypes>`  
  
 `<type>home</type>`  
  
 `<type>work</type>`  
  
 `</phoneTypes>`  
  
## <a name="example"></a><span data-ttu-id="1f334-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f334-141">Example</span></span>  
 <span data-ttu-id="1f334-142">L’exemple suivant montre comment créer des attributs pour un élément XML de façon déclarative, dans le cadre du XML et dynamiquement en ajoutant un attribut à une instance d’un <xref:System.Xml.Linq.XElement> objet.</span><span class="sxs-lookup"><span data-stu-id="1f334-142">The following example shows how to create attributes for an XML element both declaratively, as part of the XML, and dynamically by adding an attribute to an instance of an <xref:System.Xml.Linq.XElement> object.</span></span> <span data-ttu-id="1f334-143">Le `type` attribut est créé de façon déclarative et `owner` attribut est créé dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="1f334-143">The `type` attribute is created declaratively and the `owner` attribute is created dynamically.</span></span>  
  
 [!code-vb[VbXMLSamples#44](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-attribute-axis-property_2.vb)]  
  
 <span data-ttu-id="1f334-144">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1f334-144">This code displays the following text:</span></span>  
  
```xml  
<phone type="home" owner="Harris, Phyllis">206-555-0144</phone>  
```  
  
## <a name="example"></a><span data-ttu-id="1f334-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f334-145">Example</span></span>  
 <span data-ttu-id="1f334-146">L’exemple suivant utilise la syntaxe de crochets pointus pour obtenir la valeur de l’attribut XML nommé `number-type`, qui n’est pas un identificateur valide en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1f334-146">The following example uses the angle bracket syntax to get the value of the XML attribute named `number-type`, which is not a valid identifier in Visual Basic.</span></span>  
  
 [!code-vb[VbXMLSamples#13](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-attribute-axis-property_3.vb)]  
  
 <span data-ttu-id="1f334-147">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1f334-147">This code displays the following text:</span></span>  
  
 `Phone type: work`  
  
## <a name="example"></a><span data-ttu-id="1f334-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f334-148">Example</span></span>  
 <span data-ttu-id="1f334-149">L'exemple suivant déclare `ns` en tant que préfixe d'espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="1f334-149">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="1f334-150">Il utilise ensuite le préfixe de l’espace de noms pour créer un littéral XML et accéder au premier nœud enfant avec le nom qualifié «`ns:name`».</span><span class="sxs-lookup"><span data-stu-id="1f334-150">It then uses the prefix of the namespace to create an XML literal and access the first child node with the qualified name "`ns:name`".</span></span>  
  
 [!code-vb[VbXMLSamples#14](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-attribute-axis-property_4.vb)]  
  
 <span data-ttu-id="1f334-151">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1f334-151">This code displays the following text:</span></span>  
  
 `Phone type: home`  
  
## <a name="see-also"></a><span data-ttu-id="1f334-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f334-152">See Also</span></span>  
 <xref:System.Xml.Linq.XElement>  
 [<span data-ttu-id="1f334-153">Propriétés d’axe XML</span><span class="sxs-lookup"><span data-stu-id="1f334-153">XML Axis Properties</span></span>](../../../visual-basic/language-reference/xml-axis/xml-axis-properties.md)  
 [<span data-ttu-id="1f334-154">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="1f334-154">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)  
 [<span data-ttu-id="1f334-155">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1f334-155">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [<span data-ttu-id="1f334-156">Nom des attributs et des éléments XML déclarés</span><span class="sxs-lookup"><span data-stu-id="1f334-156">Names of Declared XML Elements and Attributes</span></span>](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
