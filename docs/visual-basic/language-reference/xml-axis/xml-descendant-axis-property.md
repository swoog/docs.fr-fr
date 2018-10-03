---
title: Propriété d'axe descendant XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyDescendantsAxis
helpviewer_keywords:
- Visual Basic code, accessing XML
- XML descendant axis property [Visual Basic]
- descendant axis property [Visual Baisc]
- XML axis [Visual Basic], descendant
- XML [Visual Basic], accessing
ms.assetid: a178f85b-5d54-438f-8479-40b62af6fe76
ms.openlocfilehash: 6040401ce3e98c835677be3c4cc7698013348f37
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48037107"
---
# <a name="xml-descendant-axis-property-visual-basic"></a><span data-ttu-id="1fc1a-102">Propriété d'axe descendant XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1fc1a-102">XML Descendant Axis Property (Visual Basic)</span></span>
<span data-ttu-id="1fc1a-103">Fournit l’accès aux descendants des éléments suivants : un <xref:System.Xml.Linq.XElement> objet, un <xref:System.Xml.Linq.XDocument> objet, une collection de <xref:System.Xml.Linq.XElement> objets, ou une collection de <xref:System.Xml.Linq.XDocument> objets.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-103">Provides access to the descendants of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fc1a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fc1a-104">Syntax</span></span>  
  
```  
object...<descendant>  
```  
  
## <a name="parts"></a><span data-ttu-id="1fc1a-105">Composants</span><span class="sxs-lookup"><span data-stu-id="1fc1a-105">Parts</span></span>  
 `object`  
 <span data-ttu-id="1fc1a-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-106">Required.</span></span> <span data-ttu-id="1fc1a-107">Un objet <xref:System.Xml.Linq.XElement>, un objet <xref:System.Xml.Linq.XDocument>, une collection d'objets <xref:System.Xml.Linq.XElement> ou une collection d'objets <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-107">An <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>  
  
 <span data-ttu-id="1fc1a-108">...<</span><span class="sxs-lookup"><span data-stu-id="1fc1a-108">...<</span></span>  
 <span data-ttu-id="1fc1a-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-109">Required.</span></span> <span data-ttu-id="1fc1a-110">Indique le début d’une propriété d’axe descendant.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-110">Denotes the start of a descendant axis property.</span></span>  
  
 `descendant`  
 <span data-ttu-id="1fc1a-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-111">Required.</span></span> <span data-ttu-id="1fc1a-112">Nom des nœuds descendants d’accès, sous la forme [`prefix``:`]`name`.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-112">Name of the descendant nodes to access, of the form [`prefix``:`]`name`.</span></span>  
  
|<span data-ttu-id="1fc1a-113">Élément</span><span class="sxs-lookup"><span data-stu-id="1fc1a-113">Part</span></span>|<span data-ttu-id="1fc1a-114">Description</span><span class="sxs-lookup"><span data-stu-id="1fc1a-114">Description</span></span>|  
|----------|-----------------|  
|`prefix`|<span data-ttu-id="1fc1a-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-115">Optional.</span></span> <span data-ttu-id="1fc1a-116">Préfixe d’espace de noms XML pour le nœud descendant.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-116">XML namespace prefix for the descendant node.</span></span> <span data-ttu-id="1fc1a-117">Doit être un espace de noms XML global qui est défini à l’aide un `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-117">Must be a global XML namespace that is defined by using an `Imports` statement.</span></span>|  
|`name`|<span data-ttu-id="1fc1a-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-118">Required.</span></span> <span data-ttu-id="1fc1a-119">Nom local du nœud descendant.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-119">Local name of the descendant node.</span></span> <span data-ttu-id="1fc1a-120">Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1a-120">See [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span>|  
  
 \>  
 <span data-ttu-id="1fc1a-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-121">Required.</span></span> <span data-ttu-id="1fc1a-122">Indique la fin d’une propriété d’axe descendant.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-122">Denotes the end of a descendant axis property.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1fc1a-123">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1fc1a-123">Return Value</span></span>  
 <span data-ttu-id="1fc1a-124">Collection d'objets <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-124">A collection of <xref:System.Xml.Linq.XElement> objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1fc1a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1fc1a-125">Remarks</span></span>  
 <span data-ttu-id="1fc1a-126">Vous pouvez utiliser une propriété d’axe descendant XML pour accéder aux nœuds descendants par nom à partir d’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> objet, ou à partir d’une collection de <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> objets.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-126">You can use an XML descendant axis property to access descendant nodes by name from an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object, or from a collection of <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> objects.</span></span> <span data-ttu-id="1fc1a-127">Utilisez le code XML `Value` propriété pour accéder à la valeur du premier nœud descendant dans la collection retournée.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-127">Use the XML `Value` property to access the value of the first descendant node in the returned collection.</span></span> <span data-ttu-id="1fc1a-128">Pour plus d’informations, consultez [propriété de valeur XML](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1a-128">For more information, see [XML Value Property](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span></span>  
  
 <span data-ttu-id="1fc1a-129">Le compilateur Visual Basic convertit des propriétés d’axes descendants en appels à la <xref:System.Xml.Linq.XContainer.Descendants%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="1fc1a-129">The Visual Basic compiler converts descendant axis properties into calls to the <xref:System.Xml.Linq.XContainer.Descendants%2A> method.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="1fc1a-130">Espaces de noms XML</span><span class="sxs-lookup"><span data-stu-id="1fc1a-130">XML Namespaces</span></span>  
 <span data-ttu-id="1fc1a-131">Le nom dans une propriété d’axe descendant peut utiliser uniquement les espaces de noms XML déclarés globalement avec le `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-131">The name in a descendant axis property can use only XML namespaces declared globally with the `Imports` statement.</span></span> <span data-ttu-id="1fc1a-132">Il ne peut pas utiliser les espaces de noms XML déclarés localement dans les littéraux d’élément XML.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-132">It cannot use XML namespaces declared locally within XML element literals.</span></span> <span data-ttu-id="1fc1a-133">Pour plus d’informations, consultez [instruction Imports (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1a-133">For more information, see [Imports Statement (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1fc1a-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="1fc1a-134">Example</span></span>  
 <span data-ttu-id="1fc1a-135">L’exemple suivant montre comment accéder à la valeur du premier nœud descendant nommé `name` et les valeurs de tous les nœuds descendants nommés `phone` à partir de la `contacts` objet.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-135">The following example shows how to access the value of the first descendant node named `name` and the values of all descendant nodes named `phone` from the `contacts` object.</span></span>  
  
 [!code-vb[VbXMLSamples#25](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-descendant-axis-property_1.vb)]  
  
 <span data-ttu-id="1fc1a-136">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1fc1a-136">This code displays the following text:</span></span>  
  
 `Name: Patrick Hines`  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a><span data-ttu-id="1fc1a-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="1fc1a-137">Example</span></span>  
 <span data-ttu-id="1fc1a-138">L'exemple suivant déclare `ns` en tant que préfixe d'espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-138">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="1fc1a-139">Il utilise ensuite le préfixe de l’espace de noms pour créer un littéral XML et accéder à la valeur du premier nœud enfant avec le nom qualifié `ns:name`.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-139">It then uses the prefix of the namespace to create an XML literal and access the value of the first child node with the qualified name `ns:name`.</span></span>  
  
 [!code-vb[VbXMLSamples#26](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-descendant-axis-property_2.vb)]  
  
 <span data-ttu-id="1fc1a-140">Ce code affiche le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1fc1a-140">This code displays the following text:</span></span>  
  
 `Name: Patrick Hines`  
  
## <a name="see-also"></a><span data-ttu-id="1fc1a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fc1a-141">See Also</span></span>  
 <xref:System.Xml.Linq.XElement>  
 [<span data-ttu-id="1fc1a-142">Propriétés d’axe XML</span><span class="sxs-lookup"><span data-stu-id="1fc1a-142">XML Axis Properties</span></span>](../../../visual-basic/language-reference/xml-axis/index.md)  
 [<span data-ttu-id="1fc1a-143">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="1fc1a-143">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)  
 [<span data-ttu-id="1fc1a-144">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1fc1a-144">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [<span data-ttu-id="1fc1a-145">Nom des attributs et des éléments XML déclarés</span><span class="sxs-lookup"><span data-stu-id="1fc1a-145">Names of Declared XML Elements and Attributes</span></span>](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
