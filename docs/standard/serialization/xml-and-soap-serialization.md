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
ms.openlocfilehash: d9dc68d8e7eced031af404aaec20784573c9930a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62028237"
---
# <a name="xml-and-soap-serialization"></a><span data-ttu-id="4c081-102">Sérialisation XML et SOAP</span><span class="sxs-lookup"><span data-stu-id="4c081-102">XML and SOAP Serialization</span></span>

<span data-ttu-id="4c081-103">La sérialisation XML convertit (sérialise) les champs et les propriétés publics d'un objet ou les paramètres et valeurs de retour des méthodes, en un flux de données XML conforme à un document de langage XSD (XML Schema Definition) spécifique.</span><span class="sxs-lookup"><span data-stu-id="4c081-103">XML serialization converts (serializes) the public fields and properties of an object, or the parameters and return values of methods, into an XML stream that conforms to a specific XML Schema definition language (XSD) document.</span></span> <span data-ttu-id="4c081-104">La sérialisation XML permet d'obtenir des classes fortement typées avec des propriétés et des champs publics convertis au format série (dans ce cas, XML) pour le stockage ou le transport.</span><span class="sxs-lookup"><span data-stu-id="4c081-104">XML serialization results in strongly typed classes with public properties and fields that are converted to a serial format (in this case, XML) for storage or transport.</span></span>

<span data-ttu-id="4c081-105">XML étant une norme ouverte, le flux de données XML peut être traité si nécessaire par toute application, quelle que soit la plateforme.</span><span class="sxs-lookup"><span data-stu-id="4c081-105">Because XML is an open standard, the XML stream can be processed by any application, as needed, regardless of platform.</span></span> <span data-ttu-id="4c081-106">Par exemple, les services Web XML créés à l'aide d'ASP.NET utilisent la classe <xref:System.Xml.Serialization.XmlSerializer> pour créer des flux de données XML qui passent des données entre des applications de services Web XML sur Internet ou des intranets.</span><span class="sxs-lookup"><span data-stu-id="4c081-106">For example, XML Web services created using ASP.NET use the <xref:System.Xml.Serialization.XmlSerializer> class to create XML streams that pass data between XML Web service applications throughout the Internet or on intranets.</span></span> <span data-ttu-id="4c081-107">Inversement, la désérialisation utilise le flux de données XML et reconstruit l'objet.</span><span class="sxs-lookup"><span data-stu-id="4c081-107">Conversely, deserialization takes such an XML stream and reconstructs the object.</span></span>

<span data-ttu-id="4c081-108">La sérialisation XML peut également être utilisée pour sérialiser des objets en flux XML se conformant à la spécification SOAP.</span><span class="sxs-lookup"><span data-stu-id="4c081-108">XML serialization can also be used to serialize objects into XML streams that conform to the SOAP specification.</span></span> <span data-ttu-id="4c081-109">SOAP est un protocole basé sur XML, conçu spécifiquement pour transporter des appels de procédure à l'aide de XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-109">SOAP is a protocol based on XML, designed specifically to transport procedure calls using XML.</span></span>

<span data-ttu-id="4c081-110">Pour sérialiser ou désérialiser des objets, utilisez la classe <xref:System.Xml.Serialization.XmlSerializer>.</span><span class="sxs-lookup"><span data-stu-id="4c081-110">To serialize or deserialize objects, use the <xref:System.Xml.Serialization.XmlSerializer> class.</span></span> <span data-ttu-id="4c081-111">Pour créer les classes à sérialiser, utilisez l'outil XML Schema Definition.</span><span class="sxs-lookup"><span data-stu-id="4c081-111">To create the classes to be serialized, use the XML Schema Definition tool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c081-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4c081-112">In This Section</span></span>

[<span data-ttu-id="4c081-113">Introduction à la sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="4c081-113">Introducing XML Serialization</span></span>](introducing-xml-serialization.md)  
<span data-ttu-id="4c081-114">Fournit une définition générale de la sérialisation, en particulier de la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-114">Provides a general definition of serialization, particularly XML serialization.</span></span>

[<span data-ttu-id="4c081-115">Guide pratique pour Sérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="4c081-115">How to: Serialize an Object</span></span>](how-to-serialize-an-object.md)  
<span data-ttu-id="4c081-116">Fournit des instructions pas à pas pour sérialiser un objet.</span><span class="sxs-lookup"><span data-stu-id="4c081-116">Provides step-by-step instructions for serializing an object.</span></span>

[<span data-ttu-id="4c081-117">Guide pratique pour Désérialiser un objet</span><span class="sxs-lookup"><span data-stu-id="4c081-117">How to: Deserialize an Object</span></span>](how-to-deserialize-an-object.md)  
<span data-ttu-id="4c081-118">Fournit des instructions pas à pas pour désérialiser un objet.</span><span class="sxs-lookup"><span data-stu-id="4c081-118">Provides step-by-step instructions for deserializing an object.</span></span>

[<span data-ttu-id="4c081-119">Exemples de sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="4c081-119">Examples of XML Serialization</span></span>](examples-of-xml-serialization.md)  
<span data-ttu-id="4c081-120">Fournit des exemples qui illustrent les points essentiels de la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-120">Provides examples that demonstrate the basics of XML serialization.</span></span>

[<span data-ttu-id="4c081-121">Outil XML Schema Definition et sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="4c081-121">The XML Schema Definition Tool and XML Serialization</span></span>](the-xml-schema-definition-tool-and-xml-serialization.md)  
<span data-ttu-id="4c081-122">Décrit comment utiliser l'outil XML Schema Definition pour créer des classes qui respectent un schéma de langage XSD particulier ou pour générer un schéma XML à partir d'un fichier .dll.</span><span class="sxs-lookup"><span data-stu-id="4c081-122">Describes how to use the XML Schema Definition tool to create classes that adhere to a particular XML Schema definition language (XSD) schema, or to generate an XML Schema from a .dll file.</span></span>

[<span data-ttu-id="4c081-123">Contrôle de la sérialisation XML à l’aide d’attributs</span><span class="sxs-lookup"><span data-stu-id="4c081-123">Controlling XML Serialization Using Attributes</span></span>](controlling-xml-serialization-using-attributes.md)  
<span data-ttu-id="4c081-124">Décrit comment contrôler la sérialisation à l'aide d'attributs.</span><span class="sxs-lookup"><span data-stu-id="4c081-124">Describes how to control serialization by using attributes.</span></span>

[<span data-ttu-id="4c081-125">Attributs qui contrôlent la sérialisation XML</span><span class="sxs-lookup"><span data-stu-id="4c081-125">Attributes That Control XML Serialization</span></span>](attributes-that-control-xml-serialization.md)  
<span data-ttu-id="4c081-126">Répertorie les attributs utilisés pour contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-126">Lists the attributes that are used to control XML serialization.</span></span>

[<span data-ttu-id="4c081-127">Guide pratique pour Spécifiez un nom d’élément différent pour un Stream XML</span><span class="sxs-lookup"><span data-stu-id="4c081-127">How to: Specify an Alternate Element Name for an XML Stream</span></span>](how-to-specify-an-alternate-element-name-for-an-xml-stream.md)  
<span data-ttu-id="4c081-128">Présente un scénario avancé illustrant comment générer plusieurs flux de données XML en substituant la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="4c081-128">Presents an advanced scenario showing how to generate multiple XML streams by overriding the serialization.</span></span>

[<span data-ttu-id="4c081-129">Guide pratique pour Contrôler la sérialisation de Classes dérivées</span><span class="sxs-lookup"><span data-stu-id="4c081-129">How to: Control Serialization of Derived Classes</span></span>](how-to-control-serialization-of-derived-classes.md)  
<span data-ttu-id="4c081-130">Fournit un exemple de procédure de contrôle de la sérialisation de classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="4c081-130">Provides an example of how to control the serialization of derived classes.</span></span>

[<span data-ttu-id="4c081-131">Guide pratique pour Qualifier l’élément XML et les noms d’attributs XML</span><span class="sxs-lookup"><span data-stu-id="4c081-131">How to: Qualify XML Element and XML Attribute Names</span></span>](how-to-qualify-xml-element-and-xml-attribute-names.md)  
<span data-ttu-id="4c081-132">Décrit comment définir et contrôler la manière dont les espaces de noms XML sont utilisés dans le flux de données XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-132">Describes how to define and control the way in which XML namespaces are used in the XML stream.</span></span>

[<span data-ttu-id="4c081-133">Sérialisation XML avec les services web XML</span><span class="sxs-lookup"><span data-stu-id="4c081-133">XML Serialization with XML Web Services</span></span>](xml-serialization-with-xml-web-services.md)  
<span data-ttu-id="4c081-134">Explique la manière dont la sérialisation XML est utilisée dans les services Web XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-134">Explains how XML serialization is used in XML Web services.</span></span>

[<span data-ttu-id="4c081-135">Guide pratique pour Sérialiser un objet comme un Stream XML encodés en SOAP</span><span class="sxs-lookup"><span data-stu-id="4c081-135">How to: Serialize an Object as a SOAP-Encoded XML Stream</span></span>](how-to-serialize-an-object-as-a-soap-encoded-xml-stream.md)  
<span data-ttu-id="4c081-136">Décrit comment utiliser le <xref:System.Xml.Serialization.XmlSerializer> classe pour créer des flux XML SOAP encodés qui est conforme à la section 5 du document World Wide Web Consortium (W3C) intitulée [Simple objet Access Protocol (SOAP) 1.1](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/).</span><span class="sxs-lookup"><span data-stu-id="4c081-136">Describes how to use the <xref:System.Xml.Serialization.XmlSerializer> class to create encoded SOAP XML streams that conform to section 5 of the World Wide Web Consortium (W3C) document titled [Simple Object Access Protocol (SOAP) 1.1](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/).</span></span>

[<span data-ttu-id="4c081-137">Guide pratique pour Substituer la sérialisation du XML SOAP encodé</span><span class="sxs-lookup"><span data-stu-id="4c081-137">How to: Override Encoded SOAP XML Serialization</span></span>](how-to-override-encoded-soap-xml-serialization.md)  
<span data-ttu-id="4c081-138">Décrit le processus permettant de substituer la sérialisation XML d'objets sous forme de messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="4c081-138">Describes the process for overriding XML serialization of objects as SOAP messages.</span></span>

[<span data-ttu-id="4c081-139">Attributs qui contrôlent la sérialisation encodée selon le protocole SOAP</span><span class="sxs-lookup"><span data-stu-id="4c081-139">Attributes That Control Encoded SOAP Serialization</span></span>](attributes-that-control-encoded-soap-serialization.md)  
<span data-ttu-id="4c081-140">Répertorie les attributs utilisés pour contrôler la sérialisation encodée selon le protocole SOAP.</span><span class="sxs-lookup"><span data-stu-id="4c081-140">Lists the attributes that are used to control SOAP-encoded serialization.</span></span>

[<span data-ttu-id="4c081-141">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="4c081-141">\<system.xml.serialization> Element</span></span>](system-xml-serialization-element.md)  
<span data-ttu-id="4c081-142">Élément de configuration de niveau supérieur permettant de contrôler la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="4c081-142">The top-level configuration element for controlling XML serialization.</span></span>

[<span data-ttu-id="4c081-143">\<dateTimeSerialization>, élément</span><span class="sxs-lookup"><span data-stu-id="4c081-143">\<dateTimeSerialization> Element</span></span>](datetimeserialization-element.md)  
<span data-ttu-id="4c081-144">Contrôle le mode de sérialisation d'objets <xref:System.DateTime>.</span><span class="sxs-lookup"><span data-stu-id="4c081-144">Controls the serialization mode of <xref:System.DateTime> objects.</span></span>

[<span data-ttu-id="4c081-145">\<schemaImporterExtensions>, élément</span><span class="sxs-lookup"><span data-stu-id="4c081-145">\<schemaImporterExtensions> Element</span></span>](schemaimporterextensions-element.md)  
<span data-ttu-id="4c081-146">Contient des types utilisés par la classe <xref:System.Xml.Serialization.XmlSchemaImporter>.</span><span class="sxs-lookup"><span data-stu-id="4c081-146">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> class.</span></span>

[<span data-ttu-id="4c081-147">\<Ajouter > élément pour \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="4c081-147">\<add> Element for \<schemaImporterExtensions></span></span>](add-element-for-schemaimporterextensions.md)  
<span data-ttu-id="4c081-148">Ajoute des types utilisés par la classe <xref:System.Xml.Serialization.XmlSchemaImporter>.</span><span class="sxs-lookup"><span data-stu-id="4c081-148">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> class.</span></span>

## <a name="related-sections"></a><span data-ttu-id="4c081-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c081-149">Related Sections</span></span>

<span data-ttu-id="4c081-150">[Création de services Web XML à l’aide de clients de service Web XML et ASP.NET](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/7bkzywba(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4c081-150">[XML Web Services Created Using ASP.NET and XML Web Service Clients](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/7bkzywba(v=vs.100))</span></span>  
<span data-ttu-id="4c081-151">Fournit des rubriques qui décrivent et expliquent comment programmer des services Web XML à l'aide d'ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="4c081-151">Provides topics that describe and explain how to program XML Web services using ASP.NET.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c081-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c081-152">See also</span></span>

- [<span data-ttu-id="4c081-153">Sérialisation binaire</span><span class="sxs-lookup"><span data-stu-id="4c081-153">Binary Serialization</span></span>](binary-serialization.md)
