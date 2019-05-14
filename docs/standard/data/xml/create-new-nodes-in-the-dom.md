---
title: Création de nouveaux nœuds dans le DOM
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 6c2b9789-b61a-49f9-b33f-db01a945edf2
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59ac88b2e7c6b3ecd4d06c0183a2f8a7f4a9e2d4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64590248"
---
# <a name="create-new-nodes-in-the-dom"></a><span data-ttu-id="71aa5-102">Création de nouveaux nœuds dans le DOM</span><span class="sxs-lookup"><span data-stu-id="71aa5-102">Create New Nodes in the DOM</span></span>
<span data-ttu-id="71aa5-103">L'objet <xref:System.Xml.XmlDocument> possède une méthode de création de tous les types de nœuds.</span><span class="sxs-lookup"><span data-stu-id="71aa5-103">The <xref:System.Xml.XmlDocument> has a create method for all of the node types.</span></span> <span data-ttu-id="71aa5-104">À l'invite, donnez un nom à la méthode, au contenu ou autres paramètres pour les nœuds dotés de contenu (par exemple, un nœud de texte) et le nœud est créé.</span><span class="sxs-lookup"><span data-stu-id="71aa5-104">Supply the method with a name when required, and content or other parameters for those nodes that have content (for example, a text node), and the node is created.</span></span> <span data-ttu-id="71aa5-105">Les méthodes suivantes sont celles qui nécessitent un nom ainsi que quelques autres paramètres pour créer un nœud correct.</span><span class="sxs-lookup"><span data-stu-id="71aa5-105">The following methods are ones that need a name and a few other parameters filled to create an appropriate node.</span></span>  
  
- <xref:System.Xml.XmlDocument.CreateCDataSection%2A>  
  
- <xref:System.Xml.XmlDocument.CreateComment%2A>  
  
- <xref:System.Xml.XmlDocument.CreateDocumentFragment%2A>  
  
- <xref:System.Xml.XmlDocument.CreateDocumentType%2A>  
  
- <xref:System.Xml.XmlDocument.CreateElement%2A>  
  
- <xref:System.Xml.XmlDocument.CreateNode%2A>  
  
- <xref:System.Xml.XmlDocument.CreateProcessingInstruction%2A>  
  
- <xref:System.Xml.XmlDocument.CreateSignificantWhitespace%2A>  
  
- <xref:System.Xml.XmlDocument.CreateTextNode%2A>  
  
- <xref:System.Xml.XmlDocument.CreateWhitespace%2A>  
  
- <xref:System.Xml.XmlDocument.CreateXmlDeclaration%2A>  
  
 <span data-ttu-id="71aa5-106">La création des autres types de nœuds exige d’autres opérations : il ne suffit pas de fournir des données à des paramètres.</span><span class="sxs-lookup"><span data-stu-id="71aa5-106">Other node types have more requirements than just providing data to parameters.</span></span>  
  
 <span data-ttu-id="71aa5-107">Pour plus d'informations sur les attributs, consultez [Création de nouveaux attributs pour des éléments du DOM](../../../../docs/standard/data/xml/creating-new-attributes-for-elements-in-the-dom.md).</span><span class="sxs-lookup"><span data-stu-id="71aa5-107">For information on attributes, see [Creating New Attributes for Elements in the DOM](../../../../docs/standard/data/xml/creating-new-attributes-for-elements-in-the-dom.md).</span></span> <span data-ttu-id="71aa5-108">Pour plus d’informations sur la validation des noms d’élément et d’attribut, consultez [Vérification des noms d’attribut et d’élément XML lors de la création de nœuds](../../../../docs/standard/data/xml/xml-element-and-attribute-name-verification-when-creating-new-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="71aa5-108">For information on element and attribute name validation, see [XML Element and Attribute Name Verification when Creating New Nodes](../../../../docs/standard/data/xml/xml-element-and-attribute-name-verification-when-creating-new-nodes.md).</span></span> <span data-ttu-id="71aa5-109">Pour plus d'informations sur la création de références d'entité, consultez [Création de nouvelles références d'entité](../../../../docs/standard/data/xml/creating-new-entity-references.md).</span><span class="sxs-lookup"><span data-stu-id="71aa5-109">For creating entity references, see [Creating New Entity References](../../../../docs/standard/data/xml/creating-new-entity-references.md).</span></span> <span data-ttu-id="71aa5-110">Pour plus d'informations sur la manière dont les espaces de noms influent sur le développement des références d'entité, consultez [Effet des espaces de noms sur le développement des références d'entité avec les nouveaux nœuds contenant des éléments et attributs](../../../../docs/standard/data/xml/namespace-affect-on-entity-ref-expansion-for-new-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="71aa5-110">For information on how namespaces affect the expansion of entity references, see [Namespace Affect on Entity Reference Expansion for New Nodes Containing Elements and Attributes](../../../../docs/standard/data/xml/namespace-affect-on-entity-ref-expansion-for-new-nodes.md).</span></span>  
  
 <span data-ttu-id="71aa5-111">Une fois de nouveaux nœuds créés, plusieurs méthodes sont disponibles pour insérer ces nœuds dans l'arborescence.</span><span class="sxs-lookup"><span data-stu-id="71aa5-111">Once new nodes are created, there are several methods available to insert them into the tree.</span></span> <span data-ttu-id="71aa5-112">Ce tableau répertorie ces méthodes et décrit la position qu'occupe le nouveau nœud dans le DOM (Document Object Model) XML.</span><span class="sxs-lookup"><span data-stu-id="71aa5-112">The table lists the methods with a description of where the new node appears in the XML Document Object Model (DOM).</span></span>  
  
|<span data-ttu-id="71aa5-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="71aa5-113">Method</span></span>|<span data-ttu-id="71aa5-114">Position du nœud</span><span class="sxs-lookup"><span data-stu-id="71aa5-114">Node placement</span></span>|  
|------------|--------------------|  
|<xref:System.Xml.XmlNode.InsertBefore%2A>|<span data-ttu-id="71aa5-115">Inséré avant le nœud de référence.</span><span class="sxs-lookup"><span data-stu-id="71aa5-115">Inserted before the reference node.</span></span> <span data-ttu-id="71aa5-116">Par exemple, pour insérer le nouveau nœud en position 5 :</span><span class="sxs-lookup"><span data-stu-id="71aa5-116">For example, to insert the new node in position 5:</span></span><br /><br /> `Dim refChild As XmlNode = node.ChildNodes(4) 'The reference is zero-based.node.InsertBefore(newChild, refChild);`<br /><br /> `XmlNode refChild = node.ChildNodes[4]; //The reference is zero-based. node.InsertBefore(newChild, refChild);`<br /><br /> <span data-ttu-id="71aa5-117">Pour plus d'informations, voir la méthode <xref:System.Xml.XmlNode.InsertBefore%2A>.</span><span class="sxs-lookup"><span data-stu-id="71aa5-117">For more information, see the <xref:System.Xml.XmlNode.InsertBefore%2A> method.</span></span>|  
|<xref:System.Xml.XmlNode.InsertAfter%2A>|<span data-ttu-id="71aa5-118">Inséré après le nœud de référence.</span><span class="sxs-lookup"><span data-stu-id="71aa5-118">Inserted after the reference node.</span></span> <span data-ttu-id="71aa5-119">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="71aa5-119">For example:</span></span><br /><br /> `node.InsertAfter(newChild, refChild)`<br /><br /> `node.InsertAfter(newChild, refChild);`<br /><br /> <span data-ttu-id="71aa5-120">Pour plus d'informations, voir la méthode <xref:System.Xml.XmlNode.InsertAfter%2A>.</span><span class="sxs-lookup"><span data-stu-id="71aa5-120">For more information, see the <xref:System.Xml.XmlNode.InsertAfter%2A> method.</span></span>|  
|<xref:System.Xml.XmlNode.AppendChild%2A>|<span data-ttu-id="71aa5-121">Ajoute le nœud à la fin de la liste des nœuds enfants du nœud donné.</span><span class="sxs-lookup"><span data-stu-id="71aa5-121">Adds the node to the end of the list of child nodes for the given node.</span></span> <span data-ttu-id="71aa5-122">Si le nœud ajouté est un objet <xref:System.Xml.XmlDocumentFragment>, l'ensemble du contenu du fragment de document est déplacé dans la liste des enfants de ce nœud.</span><span class="sxs-lookup"><span data-stu-id="71aa5-122">If the node being added is an <xref:System.Xml.XmlDocumentFragment>, the entire contents of the document fragment are moved into the child list of this node.</span></span> <span data-ttu-id="71aa5-123">Pour plus d'informations, voir la méthode <xref:System.Xml.XmlNode.AppendChild%2A>.</span><span class="sxs-lookup"><span data-stu-id="71aa5-123">For more information, see the <xref:System.Xml.XmlNode.AppendChild%2A> method.</span></span>|  
|<xref:System.Xml.XmlNode.PrependChild%2A>|<span data-ttu-id="71aa5-124">Ajoute le nœud au début de la liste des nœuds enfants du nœud donné.</span><span class="sxs-lookup"><span data-stu-id="71aa5-124">Adds the node to the beginning of the list of child nodes of the given node.</span></span> <span data-ttu-id="71aa5-125">Si le nœud ajouté est un objet <xref:System.Xml.XmlDocumentFragment>, l'ensemble du contenu du fragment de document est déplacé dans la liste des enfants de ce nœud.</span><span class="sxs-lookup"><span data-stu-id="71aa5-125">If the node being added is an <xref:System.Xml.XmlDocumentFragment>, the entire contents of the document fragment are moved into the child list of this node.</span></span> <span data-ttu-id="71aa5-126">Pour plus d'informations, voir la méthode <xref:System.Xml.XmlNode.PrependChild%2A>.</span><span class="sxs-lookup"><span data-stu-id="71aa5-126">For more information, see the <xref:System.Xml.XmlNode.PrependChild%2A> method.</span></span>|  
|<xref:System.Xml.XmlAttributeCollection.Append%2A>|<span data-ttu-id="71aa5-127">Ajoute un nœud <xref:System.Xml.XmlAttribute> à la fin de la collection d’attributs associée à un élément.</span><span class="sxs-lookup"><span data-stu-id="71aa5-127">Appends an <xref:System.Xml.XmlAttribute> node to the end of the attribute collection associated with an element.</span></span> <span data-ttu-id="71aa5-128">Pour plus d'informations, voir la méthode <xref:System.Xml.XmlAttributeCollection.Append%2A>.</span><span class="sxs-lookup"><span data-stu-id="71aa5-128">For more information, see the <xref:System.Xml.XmlAttributeCollection.Append%2A> method.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="71aa5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71aa5-129">See also</span></span>

- [<span data-ttu-id="71aa5-130">DOM (Document Object Model) XML</span><span class="sxs-lookup"><span data-stu-id="71aa5-130">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
