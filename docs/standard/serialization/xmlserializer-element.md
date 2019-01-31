---
title: Élément <xmlSerializer>
ms.date: 03/30/2017
helpviewer_keywords:
- <xmlSerializer> element
- XML serialization, configuration
- xmlSerializer element
ms.assetid: d129d10c-3eb7-45d9-8098-5fa853825e47
ms.openlocfilehash: 2919e8d4c1af858973ff3d2b58b4d3bc4f925527
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55258251"
---
# <a name="xmlserializer-element"></a><span data-ttu-id="7c303-102">\<xmlSerializer > élément</span><span class="sxs-lookup"><span data-stu-id="7c303-102">\<xmlSerializer> Element</span></span>
<span data-ttu-id="7c303-103">Spécifie si un contrôle supplémentaire de la progression de <xref:System.Xml.Serialization.XmlSerializer> est effectué.</span><span class="sxs-lookup"><span data-stu-id="7c303-103">Specifies whether an additional check of progress of the <xref:System.Xml.Serialization.XmlSerializer> is done.</span></span>  
  
 <span data-ttu-id="7c303-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="7c303-104">\<configuration></span></span>  
<span data-ttu-id="7c303-105">\<system.xml.serialization></span><span class="sxs-lookup"><span data-stu-id="7c303-105">\<system.xml.serialization></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c303-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c303-106">Syntax</span></span>  
  
```xml  
<xmlSerializer checkDeserializerAdvance = "true"|"false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7c303-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7c303-107">Attributes and Elements</span></span>  
 <span data-ttu-id="7c303-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7c303-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7c303-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c303-109">Attributes</span></span>  
  
|<span data-ttu-id="7c303-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="7c303-110">Attribute</span></span>|<span data-ttu-id="7c303-111">Description</span><span class="sxs-lookup"><span data-stu-id="7c303-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7c303-112">**checkDeserializeAdvances**</span><span class="sxs-lookup"><span data-stu-id="7c303-112">**checkDeserializeAdvances**</span></span>|<span data-ttu-id="7c303-113">Spécifie si la progression de <xref:System.Xml.Serialization.XmlSerializer> est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="7c303-113">Specifies whether the progress of the <xref:System.Xml.Serialization.XmlSerializer> is checked.</span></span> <span data-ttu-id="7c303-114">Affectez "true" ou "false" à l'attribut.</span><span class="sxs-lookup"><span data-stu-id="7c303-114">Set the attribute to "true" or "false".</span></span> <span data-ttu-id="7c303-115">La valeur par défaut est "true".</span><span class="sxs-lookup"><span data-stu-id="7c303-115">The default is "true".</span></span>|  
|<span data-ttu-id="7c303-116">**useLegacySerializationGeneration**</span><span class="sxs-lookup"><span data-stu-id="7c303-116">**useLegacySerializationGeneration**</span></span>|<span data-ttu-id="7c303-117">Spécifie si <xref:System.Xml.Serialization.XmlSerializer> utilise la génération de sérialisation héritée qui génère des assemblys en écrivant le code C# dans un fichier, puis en le compilant dans un assembly.</span><span class="sxs-lookup"><span data-stu-id="7c303-117">Specifies whether the <xref:System.Xml.Serialization.XmlSerializer> uses legacy serialization generation which generates assemblies by writing C# code to a file and then compiling it to an assembly.</span></span> <span data-ttu-id="7c303-118">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="7c303-118">The default is **false**.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7c303-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7c303-119">Child Elements</span></span>  
 <span data-ttu-id="7c303-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7c303-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7c303-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7c303-121">Parent Elements</span></span>  
  
|<span data-ttu-id="7c303-122">Élément</span><span class="sxs-lookup"><span data-stu-id="7c303-122">Element</span></span>|<span data-ttu-id="7c303-123">Description</span><span class="sxs-lookup"><span data-stu-id="7c303-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7c303-124">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="7c303-124">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)|<span data-ttu-id="7c303-125">Contient des paramètres de configuration pour les classes <xref:System.Xml.Serialization.XmlSerializer> et <xref:System.Xml.Serialization.XmlSchemaImporter>.</span><span class="sxs-lookup"><span data-stu-id="7c303-125">Contains configuration settings for the <xref:System.Xml.Serialization.XmlSerializer> and <xref:System.Xml.Serialization.XmlSchemaImporter> classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7c303-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7c303-126">Remarks</span></span>  
 <span data-ttu-id="7c303-127">Par défaut, le <xref:System.Xml.Serialization.XmlSerializer> fournit une couche supplémentaire de sécurité contre des attaques par déni de service potentielles lors de la désérialisation de données non fiables.</span><span class="sxs-lookup"><span data-stu-id="7c303-127">By default, the <xref:System.Xml.Serialization.XmlSerializer> provides an additional layer of security against potential denial of service attacks when deserializing untrusted data.</span></span> <span data-ttu-id="7c303-128">Pour ce faire, il tente de détecter des boucles infinies pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="7c303-128">It does so by attempting to detect infinite loops during deserialization.</span></span> <span data-ttu-id="7c303-129">Si une telle condition est détectée, une exception est levée avec le message suivant : « Erreur interne : Échec de la désérialisation avancer sur le flux sous-jacent. »</span><span class="sxs-lookup"><span data-stu-id="7c303-129">If such a condition is detected, an exception is thrown with the following message: "Internal error: deserialization failed to advance over underlying stream."</span></span>  
  
 <span data-ttu-id="7c303-130">Le fait de recevoir ce message n'indique pas nécessairement qu'une attaque par déni de service est en cours.</span><span class="sxs-lookup"><span data-stu-id="7c303-130">Receiving this message does not necessarily indicate that a denial of service attack is in progress.</span></span> <span data-ttu-id="7c303-131">Dans de rares circonstances, le mécanisme de détection de boucles infinies génère un faux positif et l'exception est levée pour un message entrant légitime.</span><span class="sxs-lookup"><span data-stu-id="7c303-131">In some rare circumstances, the infinite loop detection mechanism produces a false positive and the exception is thrown for a legitimate incoming message.</span></span> <span data-ttu-id="7c303-132">Si vous voyez, dans votre application, que des messages légitimes sont rejetés par cette couche de protection supplémentaire, définissez l’attribut **checkDeserializeAdvances** sur la valeur false.</span><span class="sxs-lookup"><span data-stu-id="7c303-132">If you find that in your particular application legitimate messages are being rejected by this extra layer of protection, set **checkDeserializeAdvances** attribute to "false".</span></span>  
  
## <a name="example"></a><span data-ttu-id="7c303-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c303-133">Example</span></span>  
 <span data-ttu-id="7c303-134">L’exemple de code suivant assigne la valeur false à l’attribut **checkDeserializeAdvances**.</span><span class="sxs-lookup"><span data-stu-id="7c303-134">The following code example sets the **checkDeserializeAdvances** attribute to "false".</span></span>  
  
```xml  
<configuration>  
  <system.xml.serialization>  
    <xmlSerializer checkDeserializeAdvances="false" />  
  </system.xml.serialization>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7c303-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c303-135">See also</span></span>

- <xref:System.Xml.Serialization.XmlSerializer>
- [<span data-ttu-id="7c303-136">\<system.xml.serialization>, élément</span><span class="sxs-lookup"><span data-stu-id="7c303-136">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
- [<span data-ttu-id="7c303-137">Sérialisation XML et SOAP</span><span class="sxs-lookup"><span data-stu-id="7c303-137">XML and SOAP Serialization</span></span>](../../../docs/standard/serialization/xml-and-soap-serialization.md)
