---
title: Sérialisation XML et SOAP
ms.date: 03/30/2017
helpviewer_keywords:
- SOAP, XML serialization
- XML serialization, SOAP
- serialization, SOAP
- serialization, about serialization
- XML serialization
- serialization
ms.assetid: 832ac524-21bc-419a-a27b-ca8bfc45840f
ms.openlocfilehash: 366a4a42ff0bf968e51e11a66fa81566a47c86ea
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44179427"
---
# <a name="xml-and-soap-serialization"></a><span data-ttu-id="010e7-102">Sérialisation XML et SOAP</span><span class="sxs-lookup"><span data-stu-id="010e7-102">XML and SOAP Serialization</span></span>

<span data-ttu-id="010e7-103">La sérialisation XML convertit (sérialise) les champs et les propriétés publics d'un objet ou les paramètres et valeurs de retour des méthodes, en un flux de données XML conforme à un document de langage XSD (XML Schema Definition) spécifique.</span><span class="sxs-lookup"><span data-stu-id="010e7-103">XML serialization converts (serializes) the public fields and properties of an object, or the parameters and return values of methods, into an XML stream that conforms to a specific XML Schema definition language (XSD) document.</span></span> <span data-ttu-id="010e7-104">La sérialisation XML permet d'obtenir des classes fortement typées avec des propriétés et des champs publics convertis au format série (dans ce cas, XML) pour le stockage ou le transport.</span><span class="sxs-lookup"><span data-stu-id="010e7-104">XML serialization results in strongly typed classes with public properties and fields that are converted to a serial format (in this case, XML) for storage or transport.</span></span>

<span data-ttu-id="010e7-105">XML étant une norme ouverte, le flux de données XML peut être traité si nécessaire par toute application, quelle que soit la plateforme.</span><span class="sxs-lookup"><span data-stu-id="010e7-105">Because XML is an open standard, the XML stream can be processed by any application, as needed, regardless of platform.</span></span> <span data-ttu-id="010e7-106">Par exemple, les services Web XML créés à l'aide d'ASP.NET utilisent la classe <xref:System.Xml.Serialization.XmlSerializer> pour créer des flux de données XML qui passent des données entre des applications de services Web XML sur Internet ou des intranets.</span><span class="sxs-lookup"><span data-stu-id="010e7-106">For example, XML Web services created using ASP.NET use the <xref:System.Xml.Serialization.XmlSerializer> class to create XML streams that pass data between XML Web service applications throughout the Internet or on intranets.</span></span> <span data-ttu-id="010e7-107">Inversement, la désérialisation utilise le flux de données XML et reconstruit l'objet.</span><span class="sxs-lookup"><span data-stu-id="010e7-107">Conversely, deserialization takes such an XML stream and reconstructs the object.</span></span>

<span data-ttu-id="010e7-108">La sérialisation XML peut également être utilisée pour sérialiser des objets en flux XML se conformant à la spécification SOAP.</span><span class="sxs-lookup"><span data-stu-id="010e7-108">XML serialization can also be used to serialize objects into XML streams that conform to the SOAP specification.</span></span> <span data-ttu-id="010e7-109">SOAP est un protocole basé sur XML, conçu spécifiquement pour transporter des appels de procédure à l'aide de XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-109">SOAP is a protocol based on XML, designed specifically to transport procedure calls using XML.</span></span>

<span data-ttu-id="010e7-110">Pour sérialiser ou désérialiser des objets, utilisez la classe <xref:System.Xml.Serialization.XmlSerializer>.</span><span class="sxs-lookup"><span data-stu-id="010e7-110">To serialize or deserialize objects, use the <xref:System.Xml.Serialization.XmlSerializer> class.</span></span> <span data-ttu-id="010e7-111">Pour créer les classes à sérialiser, utilisez l'outil XML Schema Definition.</span><span class="sxs-lookup"><span data-stu-id="010e7-111">To create the classes to be serialized, use the XML Schema Definition tool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="010e7-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="010e7-112">In This Section</span></span>

[<span data-ttu-id="010e7-113">Introduction à la sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="010e7-113">Introducing XML Serialization</span></span>](introducing-xml-serialization.md)  
<span data-ttu-id="010e7-114">Fournit une définition générale de la sérialisation, en particulier de la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-114">Provides a general definition of serialization, particularly XML serialization.</span></span>

[<span data-ttu-id="010e7-115">Guide pratique pour sérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="010e7-115">How to: Serialize an Object</span></span>](how-to-serialize-an-object.md)  
<span data-ttu-id="010e7-116">Fournit des instructions pas à pas pour sérialiser un objet.</span><span class="sxs-lookup"><span data-stu-id="010e7-116">Provides step-by-step instructions for serializing an object.</span></span>

[<span data-ttu-id="010e7-117">Guide pratique pour désérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="010e7-117">How to: Deserialize an Object</span></span>](how-to-deserialize-an-object.md)  
<span data-ttu-id="010e7-118">Fournit des instructions pas à pas pour désérialiser un objet.</span><span class="sxs-lookup"><span data-stu-id="010e7-118">Provides step-by-step instructions for deserializing an object.</span></span>

[<span data-ttu-id="010e7-119">Exemples de sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="010e7-119">Examples of XML Serialization</span></span>](examples-of-xml-serialization.md)  
<span data-ttu-id="010e7-120">Fournit des exemples qui illustrent les points essentiels de la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-120">Provides examples that demonstrate the basics of XML serialization.</span></span>

[<span data-ttu-id="010e7-121">Outil XML Schema Definition et sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="010e7-121">The XML Schema Definition Tool and XML Serialization</span></span>](the-xml-schema-definition-tool-and-xml-serialization.md)  
<span data-ttu-id="010e7-122">Décrit comment utiliser l'outil XML Schema Definition pour créer des classes qui respectent un schéma de langage XSD particulier ou pour générer un schéma XML à partir d'un fichier .dll.</span><span class="sxs-lookup"><span data-stu-id="010e7-122">Describes how to use the XML Schema Definition tool to create classes that adhere to a particular XML Schema definition language (XSD) schema, or to generate an XML Schema from a .dll file.</span></span>

[<span data-ttu-id="010e7-123">Contrôle de la sérialisation XML à l’aide d’attributs</span><span class="sxs-lookup"><span data-stu-id="010e7-123">Controlling XML Serialization Using Attributes</span></span>](controlling-xml-serialization-using-attributes.md)  
<span data-ttu-id="010e7-124">Décrit comment contrôler la sérialisation à l'aide d'attributs.</span><span class="sxs-lookup"><span data-stu-id="010e7-124">Describes how to control serialization by using attributes.</span></span>

[<span data-ttu-id="010e7-125">Attributs qui contrôlent la sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="010e7-125">Attributes That Control XML Serialization</span></span>](attributes-that-control-xml-serialization.md)  
<span data-ttu-id="010e7-126">Répertorie les attributs utilisés pour contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-126">Lists the attributes that are used to control XML serialization.</span></span>

[<span data-ttu-id="010e7-127">Guide pratique pour spécifier un nom d’élément différent pour un flux XML</span><span class="sxs-lookup"><span data-stu-id="010e7-127">How to: Specify an Alternate Element Name for an XML Stream</span></span>](how-to-specify-an-alternate-element-name-for-an-xml-stream.md)  
<span data-ttu-id="010e7-128">Présente un scénario avancé illustrant comment générer plusieurs flux de données XML en substituant la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="010e7-128">Presents an advanced scenario showing how to generate multiple XML streams by overriding the serialization.</span></span>

[<span data-ttu-id="010e7-129">Guide pratique pour contrôler la sérialisation de classes dérivées</span><span class="sxs-lookup"><span data-stu-id="010e7-129">How to: Control Serialization of Derived Classes</span></span>](how-to-control-serialization-of-derived-classes.md)  
<span data-ttu-id="010e7-130">Fournit un exemple de procédure de contrôle de la sérialisation de classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="010e7-130">Provides an example of how to control the serialization of derived classes.</span></span>

[<span data-ttu-id="010e7-131">Guide pratique pour qualifier des noms d’éléments XML et des noms d’attributs XML</span><span class="sxs-lookup"><span data-stu-id="010e7-131">How to: Qualify XML Element and XML Attribute Names</span></span>](how-to-qualify-xml-element-and-xml-attribute-names.md)  
<span data-ttu-id="010e7-132">Décrit comment définir et contrôler la manière dont les espaces de noms XML sont utilisés dans le flux de données XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-132">Describes how to define and control the way in which XML namespaces are used in the XML stream.</span></span>

[<span data-ttu-id="010e7-133">Sérialisation XML avec les services web XML</span><span class="sxs-lookup"><span data-stu-id="010e7-133">XML Serialization with XML Web Services</span></span>](xml-serialization-with-xml-web-services.md)  
<span data-ttu-id="010e7-134">Explique la manière dont la sérialisation XML est utilisée dans les services Web XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-134">Explains how XML serialization is used in XML Web services.</span></span>

[<span data-ttu-id="010e7-135">Guide pratique pour sérialiser un objet en tant que flux XML encodé selon le protocole SOAP</span><span class="sxs-lookup"><span data-stu-id="010e7-135">How to: Serialize an Object as a SOAP-Encoded XML Stream</span></span>](how-to-serialize-an-object-as-a-soap-encoded-xml-stream.md)  
<span data-ttu-id="010e7-136">Décrit comment utiliser le <xref:System.Xml.Serialization.XmlSerializer> classe pour créer des flux XML SOAP encodés qui est conforme à la section 5 du document World Wide Web Consortium (W3C) intitulée [Simple objet Access Protocol (SOAP) 1.1](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/).</span><span class="sxs-lookup"><span data-stu-id="010e7-136">Describes how to use the <xref:System.Xml.Serialization.XmlSerializer> class to create encoded SOAP XML streams that conform to section 5 of the World Wide Web Consortium (W3C) document titled [Simple Object Access Protocol (SOAP) 1.1](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/).</span></span>

[<span data-ttu-id="010e7-137">Guide pratique pour remplacer la sérialisation XML encodée selon le protocole SOAP</span><span class="sxs-lookup"><span data-stu-id="010e7-137">How to: Override Encoded SOAP XML Serialization</span></span>](how-to-override-encoded-soap-xml-serialization.md)  
<span data-ttu-id="010e7-138">Décrit le processus permettant de substituer la sérialisation XML d'objets sous forme de messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="010e7-138">Describes the process for overriding XML serialization of objects as SOAP messages.</span></span>

[<span data-ttu-id="010e7-139">Attributs qui contrôlent la sérialisation encodée selon le protocole SOAP</span><span class="sxs-lookup"><span data-stu-id="010e7-139">Attributes That Control Encoded SOAP Serialization</span></span>](attributes-that-control-encoded-soap-serialization.md)  
<span data-ttu-id="010e7-140">Répertorie les attributs utilisés pour contrôler la sérialisation encodée selon le protocole SOAP.</span><span class="sxs-lookup"><span data-stu-id="010e7-140">Lists the attributes that are used to control SOAP-encoded serialization.</span></span>

[<span data-ttu-id="010e7-141">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="010e7-141">\<system.xml.serialization> Element</span></span>](system-xml-serialization-element.md)  
<span data-ttu-id="010e7-142">Élément de configuration de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="010e7-142">The top-level configuration element for controlling XML serialization.</span></span>

[<span data-ttu-id="010e7-143">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="010e7-143">\<dateTimeSerialization> Element</span></span>](datetimeserialization-element.md)  
<span data-ttu-id="010e7-144">Contrôle le mode de sérialisation d'objets <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="010e7-144">Controls the serialization mode of <xref:System.DateTime> objects.</span></span>

[<span data-ttu-id="010e7-145">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="010e7-145">\<schemaImporterExtensions> Element</span></span>](schemaimporterextensions-element.md)  
<span data-ttu-id="010e7-146">Contient des types utilisés par la classe <xref:System.Xml.Serialization.XmlSchemaImporter>.</span><span class="sxs-lookup"><span data-stu-id="010e7-146">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> class.</span></span>

[<span data-ttu-id="010e7-147">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="010e7-147">\<add> Element for \<schemaImporterExtensions></span></span>](add-element-for-schemaimporterextensions.md)  
<span data-ttu-id="010e7-148">Ajoute des types utilisés par la classe <xref:System.Xml.Serialization.XmlSchemaImporter>.</span><span class="sxs-lookup"><span data-stu-id="010e7-148">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> class.</span></span>

## <a name="related-sections"></a><span data-ttu-id="010e7-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="010e7-149">Related Sections</span></span>

[<span data-ttu-id="010e7-150">Technologies de développement avancées</span><span class="sxs-lookup"><span data-stu-id="010e7-150">Advanced Development Technologies</span></span>](https://msdn.microsoft.com/library/c4a7e341-f0c6-4df4-a74f-223387ac6e4e)  
<span data-ttu-id="010e7-151">Fournit des liens vers d'autres informations sur les tâches et les techniques de développement sophistiquées dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="010e7-151">Provides links to more information on sophisticated development tasks and techniques in the .NET Framework.</span></span>

[<span data-ttu-id="010e7-152">Création de services Web XML à l’aide de clients de service Web XML et ASP.NET</span><span class="sxs-lookup"><span data-stu-id="010e7-152">XML Web Services Created Using ASP.NET and XML Web Service Clients</span></span>](https://msdn.microsoft.com/library/1e64af78-d705-4384-b08d-591a45f4379c)  
<span data-ttu-id="010e7-153">Fournit des rubriques qui décrivent et expliquent comment programmer des services Web XML à l'aide d'ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="010e7-153">Provides topics that describe and explain how to program XML Web services using ASP.NET.</span></span>

## <a name="see-also"></a><span data-ttu-id="010e7-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="010e7-154">See also</span></span>

- [<span data-ttu-id="010e7-155">Sérialisation binaire</span><span class="sxs-lookup"><span data-stu-id="010e7-155">Binary Serialization</span></span>](binary-serialization.md)
