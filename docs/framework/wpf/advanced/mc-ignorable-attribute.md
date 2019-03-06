---
title: mc:Ignorable, attribut
ms.date: 03/30/2017
helpviewer_keywords:
- mc XML namespace prefix [WPF]
- mc:Ignorable attribute
- XML [WPF], mc namespace prefix
- XAML [WPF], mc:Ignorable attribute
- mc:ProcessContent attribute
- XAML [WPF], mc:ProcessContent attribute
ms.assetid: acd9a6ef-b7ca-4146-abb6-60f3b366e9ec
ms.openlocfilehash: 432df80fca58311d1c0931d9ba3b224fc9e271ff
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57375387"
---
# <a name="mcignorable-attribute"></a><span data-ttu-id="d4d18-102">mc:Ignorable, attribut</span><span class="sxs-lookup"><span data-stu-id="d4d18-102">mc:Ignorable Attribute</span></span>
<span data-ttu-id="d4d18-103">Spécifie les [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] préfixes d’espace de noms rencontrés dans un fichier de balisage peuvent être ignorés par un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur.</span><span class="sxs-lookup"><span data-stu-id="d4d18-103">Specifies which [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] namespace prefixes encountered in a markup file may be ignored by a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor.</span></span> <span data-ttu-id="d4d18-104">Le `mc:Ignorable` attribut prend en charge la compatibilité du balisage à la fois pour le mappage d’espace de noms personnalisé et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="d4d18-104">The `mc:Ignorable` attribute supports markup compatibility both for custom namespace mapping and for [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] versioning.</span></span>  
  
## <a name="xaml-attribute-usage-single-prefix"></a><span data-ttu-id="d4d18-105">Utilisation d’attributs XAML (un seul préfixe)</span><span class="sxs-lookup"><span data-stu-id="d4d18-105">XAML Attribute Usage (Single Prefix)</span></span>  
  
```  
<object  
  xmlns:ignorablePrefix="ignorableUri"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix"...>  
    <ignorablePrefix1:ThisElementCanBeIgnored/>  
</object>  
```  
  
## <a name="xaml-attribute-usage-two-prefixes"></a><span data-ttu-id="d4d18-106">Utilisation d’attributs XAML (deux préfixes)</span><span class="sxs-lookup"><span data-stu-id="d4d18-106">XAML Attribute Usage (Two Prefixes)</span></span>  
  
```  
<object  
  xmlns:ignorablePrefix1="ignorableUri"  
  xmlns:ignorablePrefix2="ignorableUri2"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix1 ignorablePrefix2"...>  
    <ignorablePrefix1:ThisElementCanBeIgnored/>  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="d4d18-107">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="d4d18-107">XAML Values</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d4d18-108">*ignorablePrefix, ignorablePrefix1, etc.*</span><span class="sxs-lookup"><span data-stu-id="d4d18-108">*ignorablePrefix, ignorablePrefix1, etc.*</span></span>|<span data-ttu-id="d4d18-109">N’importe quelle chaîne de préfixe valide, conformément à la spécification XML 1.0.</span><span class="sxs-lookup"><span data-stu-id="d4d18-109">Any valid prefix string, per the XML 1.0 specification.</span></span>|  
|<span data-ttu-id="d4d18-110">*ignorableUri*</span><span class="sxs-lookup"><span data-stu-id="d4d18-110">*ignorableUri*</span></span>|<span data-ttu-id="d4d18-111">N’importe quel URI valide pour la désignation d’un espace de noms, conformément à la spécification XML 1.0.</span><span class="sxs-lookup"><span data-stu-id="d4d18-111">Any valid URI for designating a namespace, per the XML 1.0 specification.</span></span>|  
|<span data-ttu-id="d4d18-112">*ThisElementCanBeIgnored*</span><span class="sxs-lookup"><span data-stu-id="d4d18-112">*ThisElementCanBeIgnored*</span></span>|<span data-ttu-id="d4d18-113">Un élément qui peut être ignoré par [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] implémentations de processeur, si le type sous-jacent ne peut pas être résolu.</span><span class="sxs-lookup"><span data-stu-id="d4d18-113">An element that can be ignored by [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] processor implementations, if the underlying type cannot be resolved.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d4d18-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d4d18-114">Remarks</span></span>  
 <span data-ttu-id="d4d18-115">Le `mc` [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] préfixe d’espace de noms est la convention de préfixe recommandé à utiliser lors du mappage le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] espace de noms de compatibilité [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d4d18-115">The `mc` [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] namespace prefix is the recommended prefix convention to use when mapping the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] compatibility namespace [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)].</span></span>  
  
 <span data-ttu-id="d4d18-116">Éléments ou attributs où la partie préfixe de nom de l’élément sont identifiés comme `mc:Ignorable` ne déclenchent pas d’erreurs lors du traitement par un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur.</span><span class="sxs-lookup"><span data-stu-id="d4d18-116">Elements or attributes where the prefix portion of the element name are identified as `mc:Ignorable` will not raise errors when processed by a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor.</span></span> <span data-ttu-id="d4d18-117">Si cet attribut n’a pas pu être résolu en un type sous-jacent ou la construction de programmation, cet élément est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d4d18-117">If that attribute could not be resolved to an underlying type or programming construct, then that element is ignored.</span></span> <span data-ttu-id="d4d18-118">Notez toutefois que les éléments ignorés peuvent générer des erreurs d’analyse supplémentaires pour les spécifications d’éléments supplémentaires qui sont les effets de cet élément n’est pas traitée.</span><span class="sxs-lookup"><span data-stu-id="d4d18-118">Note however that ignored elements might still generate additional parsing errors for additional element requirements that are side effects of that element not being processed.</span></span> <span data-ttu-id="d4d18-119">Par exemple, un modèle de contenu d’élément particulier peut nécessiter un seul élément enfant, mais si l’élément enfant spécifié était dans un `mc:Ignorable` préfixe et l’élément enfant spécifié n’a pas pu être résolue en un type, puis le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur peut génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="d4d18-119">For instance, a particular element content model might require exactly one child element, but if the specified child element was in an `mc:Ignorable` prefix, and the specified child element could not be resolved to a type, then the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor might raise an error.</span></span>  
  
 <span data-ttu-id="d4d18-120">`mc:Ignorable` s’applique uniquement aux mappages d’espace de noms pour les chaînes d’identificateur.</span><span class="sxs-lookup"><span data-stu-id="d4d18-120">`mc:Ignorable` only applies to namespace mappings to identifier strings.</span></span> <span data-ttu-id="d4d18-121">`mc:Ignorable` ne s’applique pas aux mappages d’espace de noms dans des assemblys, qui spécifient un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] espace de noms et un assembly (ou par défaut le fichier exécutable actuel en tant que l’assembly).</span><span class="sxs-lookup"><span data-stu-id="d4d18-121">`mc:Ignorable` does not apply to namespace mappings into assemblies, which specify a [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] namespace and an assembly (or default to the current executable as the assembly).</span></span>  
  
 <span data-ttu-id="d4d18-122">Si vous implémentez un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur, votre implémentation de processeur ne doit pas déclencher l’analyse ou de traitement des erreurs sur la résolution de type pour tout élément ou attribut est qualifié par un préfixe qui est identifié comme `mc:Ignorable`.</span><span class="sxs-lookup"><span data-stu-id="d4d18-122">If you are implementing a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor, your processor implementation must not raise parsing or processing errors on type resolution for any element or attribute that is qualified by a prefix that is identified as `mc:Ignorable`.</span></span> <span data-ttu-id="d4d18-123">Mais votre implémentation de processeur peut toujours déclencher des exceptions qui sont le résultat d’un élément ne parvient pas à charger ou être traitées, comme l’exemple d’élément enfant de celui donné précédemment secondaire.</span><span class="sxs-lookup"><span data-stu-id="d4d18-123">But your processor implementation can still raise exceptions that are a secondary result of an element failing to load or be processed, such as the one-child element example given earlier.</span></span>  
  
 <span data-ttu-id="d4d18-124">Par défaut, un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur ignore le contenu d’un élément ignoré.</span><span class="sxs-lookup"><span data-stu-id="d4d18-124">By default, a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor will ignore content within an ignored element.</span></span> <span data-ttu-id="d4d18-125">Toutefois, vous pouvez spécifier un attribut supplémentaire, [MC : ProcessContent attribut](mc-processcontent-attribute.md), afin de demander la poursuite du traitement du contenu d’un élément ignoré par l’élément parent disponible suivant.</span><span class="sxs-lookup"><span data-stu-id="d4d18-125">However, you can specify an additional attribute, [mc:ProcessContent Attribute](mc-processcontent-attribute.md), to require continued processing of content within an ignored element by the next available parent element.</span></span>  
  
 <span data-ttu-id="d4d18-126">Plusieurs préfixes peuvent être spécifiés dans l’attribut, à l’aide d’un ou plusieurs caractères d’espace blanc comme séparateur, par exemple : `mc:Ignorable="ignore1 ignore2"`.</span><span class="sxs-lookup"><span data-stu-id="d4d18-126">Multiple prefixes can be specified in the attribute, using one or more white-space characters as the separator, for example: `mc:Ignorable="ignore1 ignore2"`.</span></span>  

 <span data-ttu-id="d4d18-127">Le [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] espace de noms définit les autres éléments et attributs qui ne sont pas documentés dans cette zone de la [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d4d18-127">The [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] namespace defines other elements and attributes that are not documented within this area of the [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)].</span></span> <span data-ttu-id="d4d18-128">Pour plus d’informations, consultez [spécification de compatibilité du balisage XML](/office/open-xml/introduction-to-markup-compatibility#markup-compatibility-in-the-open-xml-file-formats-specification).</span><span class="sxs-lookup"><span data-stu-id="d4d18-128">For more information, see [XML Markup Compatibility Specification](/office/open-xml/introduction-to-markup-compatibility#markup-compatibility-in-the-open-xml-file-formats-specification).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4d18-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d18-129">See also</span></span>
- <xref:System.Windows.Markup.XamlReader>
- [<span data-ttu-id="d4d18-130">PresentationOptions:Freeze, attribut</span><span class="sxs-lookup"><span data-stu-id="d4d18-130">PresentationOptions:Freeze Attribute</span></span>](presentationoptions-freeze-attribute.md)
- [<span data-ttu-id="d4d18-131">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="d4d18-131">XAML Overview (WPF)</span></span>](xaml-overview-wpf.md)
- [<span data-ttu-id="d4d18-132">Documents dans WPF</span><span class="sxs-lookup"><span data-stu-id="d4d18-132">Documents in WPF</span></span>](documents-in-wpf.md)
