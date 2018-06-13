---
title: Gestion de xml:space en XAML
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], xml:space attribute
- XAML [XAML Services], whitespace processing
- xml:space attribute [XAML Services]
- whitespace processing [XAML Services]
ms.assetid: 5e1814f0-5b30-43d5-8c88-dede335a89d7
ms.openlocfilehash: af971ad9ea74e123b939ff8d8488e4e45c5d4aed
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563465"
---
# <a name="xmlspace-handling-in-xaml"></a><span data-ttu-id="59ade-102">Gestion de xml:space en XAML</span><span class="sxs-lookup"><span data-stu-id="59ade-102">xml:space Handling in XAML</span></span>
<span data-ttu-id="59ade-103">Le `xml:space` attribut est un attribut XML qui déclare le comportement de traitement des espaces blancs significatifs dans un élément objet.</span><span class="sxs-lookup"><span data-stu-id="59ade-103">The `xml:space` attribute is an XML-defined attribute that declares the significant whitespace processing behavior within an object element.</span></span> <span data-ttu-id="59ade-104">Ce comportement ne s’applique à tout le contenu (texte interne) contenu dans l’élément où `xml:space` est déclarée et s’étend également aux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="59ade-104">This behavior is relevant for all content (inner text) contained within the element where `xml:space` is declared, and also scopes to child elements.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="59ade-105">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="59ade-105">XAML Attribute Usage</span></span>  
  
```xaml  
<object xml:space="preserve" />  
```  
  
 <span data-ttu-id="59ade-106">\- ou -</span><span class="sxs-lookup"><span data-stu-id="59ade-106">\- or -</span></span>  
  
```xaml  
<object xml:space="default" />  
```  
  
## <a name="remarks"></a><span data-ttu-id="59ade-107">Notes</span><span class="sxs-lookup"><span data-stu-id="59ade-107">Remarks</span></span>  
 <span data-ttu-id="59ade-108">La définition de la `xml:space` attribut en XAML, y compris ses deux valeurs possibles est dérivée de `xml:space` , défini comme un « attribut spécial » par les spécifications W3C pour XML.</span><span class="sxs-lookup"><span data-stu-id="59ade-108">The definition for the `xml:space` attribute in XAML including its two possible values is derived from `xml:space` as defined as a "special attribute" by W3C specifications for XML.</span></span>  
  
 <span data-ttu-id="59ade-109">La valeur par défaut de la `xml:space` attribut est la valeur littérale `"default"`.</span><span class="sxs-lookup"><span data-stu-id="59ade-109">The default value of the `xml:space` attribute is the literal value `"default"`.</span></span> <span data-ttu-id="59ade-110">Pour la valeur `"default"`, ou si `xml:space` n’est pas indiqué, le comportement de l’analyse d’un espace blanc significatif est la gestion par défaut, tel que défini dans la rubrique [traitement des espaces blancs en XAML](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="59ade-110">For the value `"default"`, or if `xml:space` is not indicated at all, the behavior of significant whitespace parsing is the default handling, as defined in the topic [Whitespace Processing in XAML](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span></span>  
  
 <span data-ttu-id="59ade-111">Pour conserver l’espace blanc dans le contenu d’élément objet, spécifiez `xml:space="preserve"` sur cet élément objet.</span><span class="sxs-lookup"><span data-stu-id="59ade-111">To preserve whitespace within object element content, specify `xml:space="preserve"` on that object element.</span></span>  
  
 <span data-ttu-id="59ade-112">Dans la plupart des interprétations le `xml:space` effets et la valeur de l’attribut sont limitées aux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="59ade-112">Under most interpretations, the `xml:space` attribute effects and the value of the attribute are scoped to child elements.</span></span>  
  
 <span data-ttu-id="59ade-113">Pour obtenir une description complète des espaces blancs en XAML de traitement, consultez [traitement des espaces blancs en XAML](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="59ade-113">For a complete discussion of whitespace processing in XAML, see [Whitespace Processing in XAML](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59ade-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ade-114">See Also</span></span>  
 [<span data-ttu-id="59ade-115">Traitement des espaces blancs en XAML</span><span class="sxs-lookup"><span data-stu-id="59ade-115">Whitespace Processing in XAML</span></span>](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md)  
 [<span data-ttu-id="59ade-116">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="59ade-116">XAML Overview (WPF)</span></span>](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
