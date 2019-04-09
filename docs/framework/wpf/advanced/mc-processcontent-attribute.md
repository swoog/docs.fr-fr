---
title: mc:ProcessContent, attribut
ms.date: 03/30/2017
helpviewer_keywords:
- mc:ProcessContent attribute
- XAML [WPF], mc:ProcessContent attribute
ms.assetid: 2689b2c8-b4dc-4b71-b9bd-f95e619122d7
ms.openlocfilehash: 865b1a3ccc30ff5efab4b08956bf7ba2bba4769c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59110584"
---
# <a name="mcprocesscontent-attribute"></a><span data-ttu-id="607b3-102">mc:ProcessContent, attribut</span><span class="sxs-lookup"><span data-stu-id="607b3-102">mc:ProcessContent Attribute</span></span>
<span data-ttu-id="607b3-103">Spécifie les [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] éléments doivent toujours avoir contenu traité par les éléments parents pertinents, même si l’élément parent immédiat peut être ignoré par un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur en raison de la spécification [mc : Ignorable, attribut](mc-ignorable-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="607b3-103">Specifies which [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] elements should still have content processed by relevant parent elements, even if the immediate parent element may be ignored by a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor due to specifying [mc:Ignorable Attribute](mc-ignorable-attribute.md).</span></span> <span data-ttu-id="607b3-104">Le `mc:ProcessContent` attribut prend en charge la compatibilité du balisage à la fois pour le mappage d’espace de noms personnalisé et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="607b3-104">The `mc:ProcessContent` attribute supports markup compatibility both for custom namespace mapping and for [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] versioning.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="607b3-105">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="607b3-105">XAML Attribute Usage</span></span>  
  
```  
<object  
  xmlns:ignorablePrefix="ignorableUri"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix"...  
  mc:ProcessContent="ignorablePrefix:ThisElementCanBeIgnored"  
>  
    <ignorablePrefix:ThisElementCanBeIgnored>  
        [content]  
    </ignorablePrefix:ThisElementCanBeIgnored>  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="607b3-106">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="607b3-106">XAML Values</span></span>  
  
|||  
|-|-|  
|*<span data-ttu-id="607b3-107">ignorablePrefix</span><span class="sxs-lookup"><span data-stu-id="607b3-107">ignorablePrefix</span></span>*|<span data-ttu-id="607b3-108">N’importe quelle chaîne de préfixe valide, conformément à la spécification XML 1.0.</span><span class="sxs-lookup"><span data-stu-id="607b3-108">Any valid prefix string, per the XML 1.0 specification.</span></span>|  
|*<span data-ttu-id="607b3-109">ignorableUri</span><span class="sxs-lookup"><span data-stu-id="607b3-109">ignorableUri</span></span>*|<span data-ttu-id="607b3-110">N’importe quel URI valide pour la désignation d’un espace de noms, conformément à la spécification XML 1.0.</span><span class="sxs-lookup"><span data-stu-id="607b3-110">Any valid URI for designating a namespace, per the XML 1.0 specification.</span></span>|  
|*<span data-ttu-id="607b3-111">ThisElementCanBeIgnored</span><span class="sxs-lookup"><span data-stu-id="607b3-111">ThisElementCanBeIgnored</span></span>*|<span data-ttu-id="607b3-112">Un élément qui peut être ignoré par [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] implémentations de processeur, si le type sous-jacent ne peut pas être résolu.</span><span class="sxs-lookup"><span data-stu-id="607b3-112">An element that can be ignored by [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] processor implementations, if the underlying type cannot be resolved.</span></span>|  
|*<span data-ttu-id="607b3-113">[content]</span><span class="sxs-lookup"><span data-stu-id="607b3-113">[content]</span></span>*|<span data-ttu-id="607b3-114">*ThisElementCanBeIgnored* est marqué comme pouvant être ignoré.</span><span class="sxs-lookup"><span data-stu-id="607b3-114">*ThisElementCanBeIgnored* is marked ignorable.</span></span> <span data-ttu-id="607b3-115">Si le processeur ignore cet élément, *[content]* est traité par *objet*.</span><span class="sxs-lookup"><span data-stu-id="607b3-115">If the processor ignores that element, *[content]* is processed by *object*.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="607b3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="607b3-116">Remarks</span></span>  
 <span data-ttu-id="607b3-117">Par défaut, un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur ignore le contenu d’un élément ignoré.</span><span class="sxs-lookup"><span data-stu-id="607b3-117">By default, a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor will ignore content within an ignored element.</span></span> <span data-ttu-id="607b3-118">Vous pouvez spécifier un élément spécifique par `mc:ProcessContent`et un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur continue à traiter le contenu dans l’élément ignoré.</span><span class="sxs-lookup"><span data-stu-id="607b3-118">You can specify a specific element by `mc:ProcessContent`, and a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor will continue to process the content within the ignored element.</span></span> <span data-ttu-id="607b3-119">Cela doit généralement être utilisé si le contenu est imbriqué dans plusieurs balises, au moins un d'entre eux peut être ignoré et au moins un d'entre eux n’est pas peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="607b3-119">This would typically be used if the content is nested within several tags, at least one of which is ignorable and at least one of which is not ignorable.</span></span>  
  
 <span data-ttu-id="607b3-120">Plusieurs préfixes peuvent être spécifiés dans l’attribut, à l’aide d’un espace de séparation, par exemple : `mc:ProcessContent="ignore:Element1 ignore:Element2"`.</span><span class="sxs-lookup"><span data-stu-id="607b3-120">Multiple prefixes may be specified in the attribute, using a space separator, for example: `mc:ProcessContent="ignore:Element1 ignore:Element2"`.</span></span>  
  
 <span data-ttu-id="607b3-121">Le [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] espace de noms définit les autres éléments et attributs qui ne sont pas documentés dans cette zone de la [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)].</span><span class="sxs-lookup"><span data-stu-id="607b3-121">The [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] namespace defines other elements and attributes that are not documented within this area of the [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)].</span></span> <span data-ttu-id="607b3-122">Pour plus d’informations, consultez [spécification de compatibilité du balisage XML](https://go.microsoft.com/fwlink/?LinkId=73824).</span><span class="sxs-lookup"><span data-stu-id="607b3-122">For more information, see [XML Markup Compatibility Specification](https://go.microsoft.com/fwlink/?LinkId=73824).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="607b3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="607b3-123">See also</span></span>

- [<span data-ttu-id="607b3-124">mc:Ignorable, attribut</span><span class="sxs-lookup"><span data-stu-id="607b3-124">mc:Ignorable Attribute</span></span>](mc-ignorable-attribute.md)
- [<span data-ttu-id="607b3-125">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="607b3-125">XAML Overview (WPF)</span></span>](xaml-overview-wpf.md)
