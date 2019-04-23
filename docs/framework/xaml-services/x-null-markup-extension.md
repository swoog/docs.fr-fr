---
title: x:Null, extension de balisage
ms.date: 03/30/2017
f1_keywords:
- NullExtension
- x:NullExtension
- x:Null
- "Null"
- xNull
helpviewer_keywords:
- Null markup extension in XAML [XAML Services]
- x:Null markup extension [XAML Services]
- XAML [XAML Services], x:Null markup extension
ms.assetid: 2e3ccc21-4996-481d-91b5-3910d8b3bfa3
ms.openlocfilehash: e46d8561b62d9137d4fed4df447338a97fc0577b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59100806"
---
# <a name="xnull-markup-extension"></a><span data-ttu-id="b57ad-102">x:Null, extension de balisage</span><span class="sxs-lookup"><span data-stu-id="b57ad-102">x:Null Markup Extension</span></span>
<span data-ttu-id="b57ad-103">Spécifie `null` en tant que valeur pour un membre XAML.</span><span class="sxs-lookup"><span data-stu-id="b57ad-103">Specifies `null` as a value for a XAML member.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="b57ad-104">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="b57ad-104">XAML Attribute Usage</span></span>  
  
```xaml  
<object property="{x:Null}" .../>  
```  
  
## <a name="remarks"></a><span data-ttu-id="b57ad-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b57ad-105">Remarks</span></span>  
 <span data-ttu-id="b57ad-106">Le mot clé pour une référence null dans C# et [!INCLUDE[TLA#tla_cpp](../../../includes/tlasharptla-cpp-md.md)] a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b57ad-106">The keyword for a null reference in C# and [!INCLUDE[TLA#tla_cpp](../../../includes/tlasharptla-cpp-md.md)] is null.</span></span> <span data-ttu-id="b57ad-107">Le mot clé Microsoft Visual Basic pour une référence null est `Nothing`, mais vous utilisez toujours `{x:Null}` en tant que l’utilisation XAML, quel que soit le langage de code-behind associer avec le XAML.</span><span class="sxs-lookup"><span data-stu-id="b57ad-107">The Microsoft Visual Basic keyword for a null reference is `Nothing`, but you always use `{x:Null}` as the XAML usage regardless which code-behind language you associate with the XAML.</span></span>  
  
 <span data-ttu-id="b57ad-108">Le `x:Null` extension de balisage ne possède aucune propriété définissable.</span><span class="sxs-lookup"><span data-stu-id="b57ad-108">The `x:Null` markup extension has no settable properties.</span></span>  
  
 <span data-ttu-id="b57ad-109">L’utilisation d’une valeur null est souvent associée à l’exposition des membres XAML d’un type CLR <xref:System.Nullable%601> valeur.</span><span class="sxs-lookup"><span data-stu-id="b57ad-109">A null usage is often associated with the XAML member exposure of a CLR <xref:System.Nullable%601> value.</span></span>  
  
 <span data-ttu-id="b57ad-110">Le `x:Null` extension de balisage, comme toutes les extensions de balisage XAML, utilise les accolades (`{,}`) pour la gestion des valeurs d’attribut soient autre chose que des littéraux ou des références de gestionnaire d’événements de séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="b57ad-110">The `x:Null` markup extension, like all XAML markup extensions, uses the braces (`{,}`) for escaping the handling of attribute values to be other than literals or event-handler references.</span></span> <span data-ttu-id="b57ad-111">Syntaxe d’attribut est la syntaxe plus fréquemment utilisée avec cette extension de balisage.</span><span class="sxs-lookup"><span data-stu-id="b57ad-111">Attribute syntax is the syntax most frequently used with this markup extension.</span></span> <span data-ttu-id="b57ad-112">Syntaxe d’élément objet `<x:Null />` est techniquement possible, mais est rarement utilisé, car le `x:Null` extension de balisage n’a pas les paramètres positionnels ou les arguments de construction.</span><span class="sxs-lookup"><span data-stu-id="b57ad-112">An object element syntax `<x:Null />` is technically possible, but is rarely used because the `x:Null` markup extension has no positional parameters or construction arguments.</span></span>  
  
 <span data-ttu-id="b57ad-113">Pour plus d’informations sur les extensions de balisage, consultez [Extensions de balisage et WPF XAML](../wpf/advanced/markup-extensions-and-wpf-xaml.md).</span><span class="sxs-lookup"><span data-stu-id="b57ad-113">For information about markup extensions, see [Markup Extensions and WPF XAML](../wpf/advanced/markup-extensions-and-wpf-xaml.md).</span></span>  
  
 <span data-ttu-id="b57ad-114">Dans les Services XAML .NET Framework, la gestion de cette extension de balisage est définie par le <xref:System.Windows.Markup.NullExtension> classe.</span><span class="sxs-lookup"><span data-stu-id="b57ad-114">In .NET Framework XAML Services, the handling for this markup extension is defined by the <xref:System.Windows.Markup.NullExtension> class.</span></span>  
  
## <a name="wpf-usage-notes"></a><span data-ttu-id="b57ad-115">Remarques sur l’utilisation WPF</span><span class="sxs-lookup"><span data-stu-id="b57ad-115">WPF Usage Notes</span></span>  
 <span data-ttu-id="b57ad-116">Notez que `null` n’est pas nécessairement la valeur initiale non définie pour une propriété de dépendance de type référence.</span><span class="sxs-lookup"><span data-stu-id="b57ad-116">Note that `null` is not necessarily the initial unset value for a reference-type dependency property.</span></span> <span data-ttu-id="b57ad-117">La valeur par défaut initiale peut varier pour chaque propriété de dépendance et peut être basée sur les métadonnées spécifiques à la propriété.</span><span class="sxs-lookup"><span data-stu-id="b57ad-117">The initial default value can vary for each dependency property and can be based on property-specific metadata.</span></span> <span data-ttu-id="b57ad-118">De nombreuses propriétés de dépendance n’acceptent pas `null` en tant que valeur, par le biais de balisage ou le code en raison de leurs implémentations de rappel de validation.</span><span class="sxs-lookup"><span data-stu-id="b57ad-118">Many dependency properties do not accept `null` as a value, either through markup or code because of their validation callback implementations.</span></span> <span data-ttu-id="b57ad-119">Pour plus d’informations sur les propriétés de dépendance, consultez [vue d’ensemble des propriétés de dépendance](../wpf/advanced/dependency-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b57ad-119">For more information about dependency properties, see [Dependency Properties Overview](../wpf/advanced/dependency-properties-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b57ad-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b57ad-120">See also</span></span>

- <xref:System.Windows.DependencyProperty.UnsetValue>
- [<span data-ttu-id="b57ad-121">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="b57ad-121">XAML Overview (WPF)</span></span>](../wpf/advanced/xaml-overview-wpf.md)
- [<span data-ttu-id="b57ad-122">Extensions de balisage et XAML WPF</span><span class="sxs-lookup"><span data-stu-id="b57ad-122">Markup Extensions and WPF XAML</span></span>](../wpf/advanced/markup-extensions-and-wpf-xaml.md)
