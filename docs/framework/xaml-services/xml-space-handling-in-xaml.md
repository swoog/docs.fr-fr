---
title: Gestion de xml:space en XAML
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], xml:space attribute
- XAML [XAML Services], white-space processing
- xml:space attribute [XAML Services]
- white-space processing [XAML Services]
ms.assetid: 5e1814f0-5b30-43d5-8c88-dede335a89d7
ms.openlocfilehash: d15bab1ad9234959048fa7b7c3fa2bbbeca5fe6e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938721"
---
# <a name="xmlspace-handling-in-xaml"></a><span data-ttu-id="41e96-102">Gestion de xml:space en XAML</span><span class="sxs-lookup"><span data-stu-id="41e96-102">xml:space Handling in XAML</span></span>
<span data-ttu-id="41e96-103">Le `xml:space` attribut est un attribut XML qui déclare le comportement de traitement des espaces blancs significatifs dans un élément objet.</span><span class="sxs-lookup"><span data-stu-id="41e96-103">The `xml:space` attribute is an XML-defined attribute that declares the significant white-space processing behavior within an object element.</span></span> <span data-ttu-id="41e96-104">Ce comportement s’applique pour tout le contenu (texte interne) contenu dans l’élément où `xml:space` est déclaré et s’étend également aux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="41e96-104">This behavior is relevant for all content (inner text) contained within the element where `xml:space` is declared, and also scopes to child elements.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="41e96-105">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="41e96-105">XAML Attribute Usage</span></span>  
  
```xaml  
<object xml:space="preserve" />  
```  
  
 <span data-ttu-id="41e96-106">\- ou -</span><span class="sxs-lookup"><span data-stu-id="41e96-106">\- or -</span></span>  
  
```xaml  
<object xml:space="default" />  
```  
  
## <a name="remarks"></a><span data-ttu-id="41e96-107">Notes</span><span class="sxs-lookup"><span data-stu-id="41e96-107">Remarks</span></span>  
 <span data-ttu-id="41e96-108">La définition de la `xml:space` attribut dans XAML, y compris ses deux valeurs possibles est dérivée de `xml:space` , défini comme un « attribut spécial » par les spécifications W3C pour XML.</span><span class="sxs-lookup"><span data-stu-id="41e96-108">The definition for the `xml:space` attribute in XAML including its two possible values is derived from `xml:space` as defined as a "special attribute" by W3C specifications for XML.</span></span>  
  
 <span data-ttu-id="41e96-109">La valeur par défaut de la `xml:space` attribut est la valeur littérale `"default"`.</span><span class="sxs-lookup"><span data-stu-id="41e96-109">The default value of the `xml:space` attribute is the literal value `"default"`.</span></span> <span data-ttu-id="41e96-110">Pour la valeur `"default"`, ou si `xml:space` n’est pas indiqué, le comportement d’analyse d’espace blanc significatif est la gestion par défaut, comme défini dans la rubrique [blancs en XAML traitement](whitespace-processing-in-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="41e96-110">For the value `"default"`, or if `xml:space` is not indicated at all, the behavior of significant white-space parsing is the default handling, as defined in the topic [White-space processing in XAML](whitespace-processing-in-xaml.md).</span></span>  
  
 <span data-ttu-id="41e96-111">Pour conserver les espaces blancs dans le contenu d’élément objet, spécifiez `xml:space="preserve"` sur cet élément objet.</span><span class="sxs-lookup"><span data-stu-id="41e96-111">To preserve white space within object element content, specify `xml:space="preserve"` on that object element.</span></span>  
  
 <span data-ttu-id="41e96-112">Dans la plupart des interprétations le `xml:space` effets et la valeur de l’attribut sont limitées aux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="41e96-112">Under most interpretations, the `xml:space` attribute effects and the value of the attribute are scoped to child elements.</span></span>  
  
 <span data-ttu-id="41e96-113">Pour obtenir une description complète de l’espace blanc-traitement dans XAML, consultez [blancs en XAML traitement](whitespace-processing-in-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="41e96-113">For a complete discussion of white-space processing in XAML, see [White-space processing in XAML](whitespace-processing-in-xaml.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41e96-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41e96-114">See also</span></span>

- [<span data-ttu-id="41e96-115">Espace blanc dans XAML de traitement</span><span class="sxs-lookup"><span data-stu-id="41e96-115">White-space processing in XAML</span></span>](whitespace-processing-in-xaml.md)
- [<span data-ttu-id="41e96-116">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="41e96-116">XAML Overview (WPF)</span></span>](../wpf/advanced/xaml-overview-wpf.md)
