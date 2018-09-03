---
title: Propriété d'axe enfant XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyChildAxis
helpviewer_keywords:
- Visual Basic code, accessing XML
- XML axis [Visual Basic], child
- child axis property [Visual Basic]
- XML child axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: 89a59d00-985e-4f5c-b59f-29b47bad11cb
ms.openlocfilehash: 0b504a9e368e5179d5f91faf7256445d7da47b1d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43484892"
---
# <a name="xml-child-axis-property-visual-basic"></a><span data-ttu-id="81cb5-102">Propriété d'axe enfant XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="81cb5-102">XML Child Axis Property (Visual Basic)</span></span>
<span data-ttu-id="81cb5-103">Fournit un accès aux enfants de l'un des éléments suivants : un objet <xref:System.Xml.Linq.XElement>, un objet <xref:System.Xml.Linq.XDocument>, une collection d'objets <xref:System.Xml.Linq.XElement> ou une collection d'objets <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="81cb5-103">Provides access to the children of one of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81cb5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81cb5-104">Syntax</span></span>  
  
```  
object.<child>  
```  
  
## <a name="parts"></a><span data-ttu-id="81cb5-105">Composants</span><span class="sxs-lookup"><span data-stu-id="81cb5-105">Parts</span></span>  
  
|<span data-ttu-id="81cb5-106">Terme</span><span class="sxs-lookup"><span data-stu-id="81cb5-106">Term</span></span>|<span data-ttu-id="81cb5-107">Définition</span><span class="sxs-lookup"><span data-stu-id="81cb5-107">Definition</span></span>|  
|---|---|  
|`object`|<span data-ttu-id="81cb5-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="81cb5-108">Required.</span></span> <span data-ttu-id="81cb5-109">Un objet <xref:System.Xml.Linq.XElement>, un objet <xref:System.Xml.Linq.XDocument>, une collection d'objets <xref:System.Xml.Linq.XElement> ou une collection d'objets <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="81cb5-109">An <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>|  
|<span data-ttu-id="81cb5-110">.<</span><span class="sxs-lookup"><span data-stu-id="81cb5-110">.<</span></span>|<span data-ttu-id="81cb5-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="81cb5-111">Required.</span></span> <span data-ttu-id="81cb5-112">Indique le début d'une propriété d'axe enfant.</span><span class="sxs-lookup"><span data-stu-id="81cb5-112">Denotes the start of a child axis property.</span></span>|  
|`child`|<span data-ttu-id="81cb5-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="81cb5-113">Required.</span></span> <span data-ttu-id="81cb5-114">Nom des nœuds enfants auxquels accéder, de la forme [`prefix``:`]`name`.</span><span class="sxs-lookup"><span data-stu-id="81cb5-114">Name of the child nodes to access, of the form [`prefix``:`]`name`.</span></span><br /><br /> <span data-ttu-id="81cb5-115">-   `Prefix` -Facultatif.</span><span class="sxs-lookup"><span data-stu-id="81cb5-115">-   `Prefix` - Optional.</span></span> <span data-ttu-id="81cb5-116">Préfixe d'espace de noms XML pour le nœud enfant.</span><span class="sxs-lookup"><span data-stu-id="81cb5-116">XML namespace prefix for the child node.</span></span> <span data-ttu-id="81cb5-117">Doit être un espace de noms XML global défini avec une instruction `Imports`.</span><span class="sxs-lookup"><span data-stu-id="81cb5-117">Must be a global XML namespace defined with an `Imports` statement.</span></span><br /><span data-ttu-id="81cb5-118">-   `Name` -Requis.</span><span class="sxs-lookup"><span data-stu-id="81cb5-118">-   `Name` - Required.</span></span> <span data-ttu-id="81cb5-119">Nom de nœud enfant local.</span><span class="sxs-lookup"><span data-stu-id="81cb5-119">Local child node name.</span></span> <span data-ttu-id="81cb5-120">Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="81cb5-120">See [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span>|  
|>|<span data-ttu-id="81cb5-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="81cb5-121">Required.</span></span> <span data-ttu-id="81cb5-122">Indique la fin d'une propriété d'axe enfant.</span><span class="sxs-lookup"><span data-stu-id="81cb5-122">Denotes the end of a child axis property.</span></span>|  
  
## <a name="return-value"></a><span data-ttu-id="81cb5-123">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="81cb5-123">Return Value</span></span>  
 <span data-ttu-id="81cb5-124">Collection d'objets <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="81cb5-124">A collection of <xref:System.Xml.Linq.XElement> objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="81cb5-125">Notes</span><span class="sxs-lookup"><span data-stu-id="81cb5-125">Remarks</span></span>  
 <span data-ttu-id="81cb5-126">Vous pouvez utiliser une propriété d'axe enfant XML pour accéder aux nœuds enfants par nom, à partir d'un objet <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument>, ou à partir d'une collection d'objets <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="81cb5-126">You can use an XML child axis property to access child nodes by name from an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object, or from a collection of <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> objects.</span></span> <span data-ttu-id="81cb5-127">Utilisez la propriété XML `Value` pour accéder à la valeur du premier nœud enfant dans la collection retournée.</span><span class="sxs-lookup"><span data-stu-id="81cb5-127">Use the XML `Value` property to access the value of the first child node in the returned collection.</span></span> <span data-ttu-id="81cb5-128">Pour plus d’informations, consultez [propriété de valeur XML](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span><span class="sxs-lookup"><span data-stu-id="81cb5-128">For more information, see [XML Value Property](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span></span>  
  
 <span data-ttu-id="81cb5-129">Le compilateur Visual Basic convertit des propriétés d’axes enfants en appels à la <xref:System.Xml.Linq.XContainer.Elements%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="81cb5-129">The Visual Basic compiler converts child axis properties to calls to the <xref:System.Xml.Linq.XContainer.Elements%2A> method.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="81cb5-130">Espaces de noms XML</span><span class="sxs-lookup"><span data-stu-id="81cb5-130">XML Namespaces</span></span>  
 <span data-ttu-id="81cb5-131">Le nom inclus dans une propriété d'axe enfant peut utiliser uniquement des préfixes d'espace de noms XML déclarés globalement à l'aide de l'instruction `Imports`.</span><span class="sxs-lookup"><span data-stu-id="81cb5-131">The name in a child axis property can use only XML namespace prefixes declared globally with the `Imports` statement.</span></span> <span data-ttu-id="81cb5-132">Il ne peut pas utiliser des préfixes d'espace de noms XML déclarés localement dans des littéraux d'éléments XML.</span><span class="sxs-lookup"><span data-stu-id="81cb5-132">It cannot use XML namespace prefixes declared locally within XML element literals.</span></span> <span data-ttu-id="81cb5-133">Pour plus d’informations, consultez [instruction Imports (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="81cb5-133">For more information, see [Imports Statement (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="81cb5-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="81cb5-134">Example</span></span>  
 <span data-ttu-id="81cb5-135">L'exemple suivant montre comment accéder aux nœuds enfants nommés `phone` à partir de l'objet `contact`.</span><span class="sxs-lookup"><span data-stu-id="81cb5-135">The following example shows how to access the child nodes named `phone` from the `contact` object.</span></span>  
  
 [!code-vb[VbXMLSamples#17](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-child-axis-property_1.vb)]  
  
 <span data-ttu-id="81cb5-136">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="81cb5-136">This code displays the following text:</span></span>  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a><span data-ttu-id="81cb5-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="81cb5-137">Example</span></span>  
 <span data-ttu-id="81cb5-138">L'exemple suivant montre comment accéder aux nœuds enfants nommés `phone` à partir de la collection retournée par la propriété d'axe enfant `contact` de l'objet `contacts`.</span><span class="sxs-lookup"><span data-stu-id="81cb5-138">The following example shows how to access the child nodes named `phone` from the collection returned by the `contact` child axis property of the `contacts` object.</span></span>  
  
 [!code-vb[VbXMLSamples#18](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-child-axis-property_2.vb)]  
  
 <span data-ttu-id="81cb5-139">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="81cb5-139">This code displays the following text:</span></span>  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a><span data-ttu-id="81cb5-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="81cb5-140">Example</span></span>  
 <span data-ttu-id="81cb5-141">L'exemple suivant déclare `ns` en tant que préfixe d'espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="81cb5-141">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="81cb5-142">Il utilise ensuite le préfixe de l'espace de noms pour créer un littéral XML et accéder au premier nœud enfant avec le nom qualifié `ns:name`.</span><span class="sxs-lookup"><span data-stu-id="81cb5-142">It then uses the prefix of the namespace to create an XML literal and access the first child node with the qualified name `ns:name`.</span></span>  
  
 [!code-vb[VbXMLSamples#19](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-child-axis-property_3.vb)]  
  
 <span data-ttu-id="81cb5-143">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="81cb5-143">This code displays the following text:</span></span>  
  
 `Patrick Hines`  
  
## <a name="see-also"></a><span data-ttu-id="81cb5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81cb5-144">See Also</span></span>  
 <xref:System.Xml.Linq.XElement>  
 [<span data-ttu-id="81cb5-145">Propriétés d’axe XML</span><span class="sxs-lookup"><span data-stu-id="81cb5-145">XML Axis Properties</span></span>](../../../visual-basic/language-reference/xml-axis/index.md)  
 [<span data-ttu-id="81cb5-146">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="81cb5-146">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)  
 [<span data-ttu-id="81cb5-147">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="81cb5-147">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [<span data-ttu-id="81cb5-148">Nom des attributs et des éléments XML déclarés</span><span class="sxs-lookup"><span data-stu-id="81cb5-148">Names of Declared XML Elements and Attributes</span></span>](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
