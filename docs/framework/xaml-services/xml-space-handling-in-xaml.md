---
title: Gestion de xml:space en XAML
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], xml:space attribute
- XAML [XAML Services], white-space processing
- xml:space attribute [XAML Services]
- white-space processing [XAML Services]
ms.assetid: 5e1814f0-5b30-43d5-8c88-dede335a89d7
ms.openlocfilehash: 051cb6b3a314509e9593ee570fd659098670e88b
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925855"
---
# <a name="xmlspace-handling-in-xaml"></a><span data-ttu-id="ee9d4-102">Gestion de xml:space en XAML</span><span class="sxs-lookup"><span data-stu-id="ee9d4-102">xml:space Handling in XAML</span></span>
<span data-ttu-id="ee9d4-103">Le `xml:space` attribut est un attribut XML qui déclare le comportement de traitement des espaces blancs significatifs dans un élément objet.</span><span class="sxs-lookup"><span data-stu-id="ee9d4-103">The `xml:space` attribute is an XML-defined attribute that declares the significant white-space processing behavior within an object element.</span></span> <span data-ttu-id="ee9d4-104">Ce comportement s’applique pour tout le contenu (texte interne) contenu dans l’élément où `xml:space` est déclaré et s’étend également aux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="ee9d4-104">This behavior is relevant for all content (inner text) contained within the element where `xml:space` is declared, and also scopes to child elements.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="ee9d4-105">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="ee9d4-105">XAML Attribute Usage</span></span>  
  
```xaml  
<object xml:space="preserve" />  
```  
  
 <span data-ttu-id="ee9d4-106">\- ou -</span><span class="sxs-lookup"><span data-stu-id="ee9d4-106">\- or -</span></span>  
  
```xaml  
<object xml:space="default" />  
```  
  
## <a name="remarks"></a><span data-ttu-id="ee9d4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ee9d4-107">Remarks</span></span>  
 <span data-ttu-id="ee9d4-108">La définition de la `xml:space` attribut dans XAML, y compris ses deux valeurs possibles est dérivée de `xml:space` , défini comme un « attribut spécial » par les spécifications W3C pour XML.</span><span class="sxs-lookup"><span data-stu-id="ee9d4-108">The definition for the `xml:space` attribute in XAML including its two possible values is derived from `xml:space` as defined as a "special attribute" by W3C specifications for XML.</span></span>  
  
 <span data-ttu-id="ee9d4-109">La valeur par défaut de la `xml:space` attribut est la valeur littérale `"default"`.</span><span class="sxs-lookup"><span data-stu-id="ee9d4-109">The default value of the `xml:space` attribute is the literal value `"default"`.</span></span> <span data-ttu-id="ee9d4-110">Pour la valeur `"default"`, ou si `xml:space` n’est pas indiqué, le comportement d’analyse d’espace blanc significatif est la gestion par défaut, comme défini dans la rubrique [blancs en XAML traitement](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="ee9d4-110">For the value `"default"`, or if `xml:space` is not indicated at all, the behavior of significant white-space parsing is the default handling, as defined in the topic [White-space processing in XAML](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span></span>  
  
 <span data-ttu-id="ee9d4-111">Pour conserver les espaces blancs dans le contenu d’élément objet, spécifiez `xml:space="preserve"` sur cet élément objet.</span><span class="sxs-lookup"><span data-stu-id="ee9d4-111">To preserve white space within object element content, specify `xml:space="preserve"` on that object element.</span></span>  
  
 <span data-ttu-id="ee9d4-112">Dans la plupart des interprétations le `xml:space` effets et la valeur de l’attribut sont limitées aux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="ee9d4-112">Under most interpretations, the `xml:space` attribute effects and the value of the attribute are scoped to child elements.</span></span>  
  
 <span data-ttu-id="ee9d4-113">Pour obtenir une description complète de l’espace blanc-traitement dans XAML, consultez [blancs en XAML traitement](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="ee9d4-113">For a complete discussion of white-space processing in XAML, see [White-space processing in XAML](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee9d4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee9d4-114">See Also</span></span>  
 [<span data-ttu-id="ee9d4-115">Espace blanc dans XAML de traitement</span><span class="sxs-lookup"><span data-stu-id="ee9d4-115">White-space processing in XAML</span></span>](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md)  
 [<span data-ttu-id="ee9d4-116">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="ee9d4-116">XAML Overview (WPF)</span></span>](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
