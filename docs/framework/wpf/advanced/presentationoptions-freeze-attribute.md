---
title: PresentationOptions:Freeze, attribut
ms.date: 03/30/2017
helpviewer_keywords:
- Freeze attribute [WPF]
- Freezable elements [WPF]
- PresentationOptions prefix [WPF]
ms.assetid: 391032dd-2fba-4804-bb8a-3b071797a9f4
ms.openlocfilehash: 3ff4a3221392d6b247d0a486e4e1f0406f539362
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378858"
---
# <a name="presentationoptionsfreeze-attribute"></a><span data-ttu-id="f83e2-102">PresentationOptions:Freeze, attribut</span><span class="sxs-lookup"><span data-stu-id="f83e2-102">PresentationOptions:Freeze Attribute</span></span>
<span data-ttu-id="f83e2-103">Définit le <xref:System.Windows.Freezable.IsFrozen%2A> état `true` sur la contenant <xref:System.Windows.Freezable> élément.</span><span class="sxs-lookup"><span data-stu-id="f83e2-103">Sets the <xref:System.Windows.Freezable.IsFrozen%2A> state to `true` on the containing <xref:System.Windows.Freezable> element.</span></span> <span data-ttu-id="f83e2-104">Comportement par défaut un <xref:System.Windows.Freezable> sans le `PresentationOptions:Freeze` attribut spécifié est que <xref:System.Windows.Freezable.IsFrozen%2A> est `false` au moment de la charge et selon que vous général <xref:System.Windows.Freezable> comportement lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f83e2-104">Default behavior for a <xref:System.Windows.Freezable> without the `PresentationOptions:Freeze` attribute specified is that <xref:System.Windows.Freezable.IsFrozen%2A> is `false` at load time, and dependent on general <xref:System.Windows.Freezable> behavior at runtime.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="f83e2-105">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="f83e2-105">XAML Attribute Usage</span></span>  
  
```  
<object  
  xmlns:PresentationOptions="http://schemas.microsoft.com/winfx/2006/xaml/presentation/options"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="PresentationOptions">  
    <freezableElement PresentationOptions:Freeze="true"/>  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="f83e2-106">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="f83e2-106">XAML Values</span></span>  
  
|||  
|-|-|  
|`PresentationOptions`|<span data-ttu-id="f83e2-107">Un préfixe d’espace de noms XML, qui peut être n’importe quelle chaîne de préfixe valide conformément à la spécification XML 1.0.</span><span class="sxs-lookup"><span data-stu-id="f83e2-107">An XML namespace prefix, which can be any valid prefix string, per the XML 1.0 specification.</span></span> <span data-ttu-id="f83e2-108">Le préfixe `PresentationOptions` est utilisé à des fins d’identification dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="f83e2-108">The prefix `PresentationOptions` is used for identification purposes in this documentation.</span></span>|  
|`freezableElement`|<span data-ttu-id="f83e2-109">Un élément qui instancie toute classe dérivée de <xref:System.Windows.Freezable>.</span><span class="sxs-lookup"><span data-stu-id="f83e2-109">An element that instantiates any derived class of <xref:System.Windows.Freezable>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f83e2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f83e2-110">Remarks</span></span>  
 <span data-ttu-id="f83e2-111">Le `Freeze` attribut est le seul attribut ou élément de programmation défini dans le `http://schemas.microsoft.com/winfx/2006/xaml/presentation/options` espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="f83e2-111">The `Freeze` attribute is the only attribute or other programming element defined in the `http://schemas.microsoft.com/winfx/2006/xaml/presentation/options` XML namespace.</span></span> <span data-ttu-id="f83e2-112">Le `Freeze` attribut existe dans cet espace de noms spécial spécifiquement afin qu’il peut être désigné comme pouvant être ignoré, à l’aide de [mc : Ignorable, attribut](mc-ignorable-attribute.md) dans le cadre des déclarations d’élément racine.</span><span class="sxs-lookup"><span data-stu-id="f83e2-112">The `Freeze` attribute exists in this special namespace specifically so that it can be designated as ignorable, using [mc:Ignorable Attribute](mc-ignorable-attribute.md) as part of the root element declarations.</span></span> <span data-ttu-id="f83e2-113">La raison qui `Freeze` doit pouvoir être ignoré n’étant donné que tous les [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] implémentations de processeur sont en mesure de figer un <xref:System.Windows.Freezable> au moment du chargement ; cette fonctionnalité n’est pas dans le cadre de la [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] spécification.</span><span class="sxs-lookup"><span data-stu-id="f83e2-113">The reason that `Freeze` must be able to be ignorable is because not all [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor implementations are able to freeze a <xref:System.Windows.Freezable> at load time; this capability is not part of the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] specification.</span></span>  
  
 <span data-ttu-id="f83e2-114">La possibilité de traiter la `Freeze` attribut spécifiquement intégré à la [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur traite [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] pour les applications compilées.</span><span class="sxs-lookup"><span data-stu-id="f83e2-114">The ability to process the `Freeze` attribute is specifically built in to the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor that processes [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] for compiled applications.</span></span> <span data-ttu-id="f83e2-115">L’attribut n’est pas pris en charge par n’importe quelle classe, et la syntaxe d’attribut n’est pas extensible ou modifiable.</span><span class="sxs-lookup"><span data-stu-id="f83e2-115">The attribute is not supported by any class, and the attribute syntax is not extensible or modifiable.</span></span> <span data-ttu-id="f83e2-116">Si vous implémentez votre propre [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur, vous pouvez choisir du comportement de gel en parallèle la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur lors du traitement de la `Freeze` attribut sur <xref:System.Windows.Freezable> éléments au moment du chargement.</span><span class="sxs-lookup"><span data-stu-id="f83e2-116">If you are implementing your own [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor you can choose to parallel the freezing behavior of the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processor when processing the `Freeze` attribute on <xref:System.Windows.Freezable> elements at load time.</span></span>  
  
 <span data-ttu-id="f83e2-117">N’importe quelle valeur pour la `Freeze` attribut autre que `true` (non sensible à la casse) génère une erreur de temps de chargement.</span><span class="sxs-lookup"><span data-stu-id="f83e2-117">Any value for the `Freeze` attribute other than `true` (not case sensitive) generates a load time error.</span></span> <span data-ttu-id="f83e2-118">(En spécifiant le `Freeze` sous la forme `false` n’est pas une erreur, mais qui est déjà le paramètre par défaut, par conséquent, pour `false` n’a aucun effet).</span><span class="sxs-lookup"><span data-stu-id="f83e2-118">(Specifying the `Freeze` attribute as `false` is not an error, but that is already the default, so setting to `false` does nothing).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f83e2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f83e2-119">See also</span></span>
- <xref:System.Windows.Freezable>
- [<span data-ttu-id="f83e2-120">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="f83e2-120">Freezable Objects Overview</span></span>](freezable-objects-overview.md)
- [<span data-ttu-id="f83e2-121">mc:Ignorable, attribut</span><span class="sxs-lookup"><span data-stu-id="f83e2-121">mc:Ignorable Attribute</span></span>](mc-ignorable-attribute.md)
