---
title: 'Procédure : Enregistrer une propriété jointe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- attached properties [WPF], registering
- registering attached properties [WPF]
ms.assetid: eb47bd94-0451-4f8d-8fb6-95f7812ac05b
ms.openlocfilehash: 4c678a64b62b8f4db24cf39ffbafac52e56c9982
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137629"
---
# <a name="how-to-register-an-attached-property"></a><span data-ttu-id="f3e7a-102">Procédure : Enregistrer une propriété jointe</span><span class="sxs-lookup"><span data-stu-id="f3e7a-102">How to: Register an Attached Property</span></span>
<span data-ttu-id="f3e7a-103">Cet exemple montre comment inscrire une propriété jointe et fournir des accesseurs publics pour pouvoir utiliser la propriété en [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] et dans le code.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-103">This example shows how to register an attached property and provide public accessors so that you can use the property in both [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] and code.</span></span> <span data-ttu-id="f3e7a-104">Les propriétés jointes sont un concept de syntaxe défini par [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="f3e7a-104">Attached properties are a syntax concept defined by [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span> <span data-ttu-id="f3e7a-105">La plupart des propriétés jointes pour les types [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont également implémentées en tant que propriétés de dépendance.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-105">Most attached properties for [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] types are also implemented as dependency properties.</span></span> <span data-ttu-id="f3e7a-106">Vous pouvez utiliser les propriétés de dépendance sur n’importe quel <xref:System.Windows.DependencyObject> types.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-106">You can use dependency properties on any <xref:System.Windows.DependencyObject> types.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f3e7a-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f3e7a-107">Example</span></span>  
 <span data-ttu-id="f3e7a-108">L’exemple suivant montre comment inscrire une propriété jointe comme une propriété de dépendance à l’aide de la <xref:System.Windows.DependencyProperty.RegisterAttached%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="f3e7a-108">The following example shows how to register an attached property as a dependency property, by using the <xref:System.Windows.DependencyProperty.RegisterAttached%2A> method.</span></span> <span data-ttu-id="f3e7a-109">La classe de fournisseur a la possibilité de fournir des métadonnées par défaut pour la propriété qui s’appliquent quand celle-ci est utilisée sur une autre classe, à moins que cette classe ne substitue les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-109">The provider class has the option of providing default metadata for the property that is applicable when the property is used on another class, unless that class overrides the metadata.</span></span> <span data-ttu-id="f3e7a-110">Dans cet exemple, la valeur par défaut de la propriété `IsBubbleSource` est définie sur `false`.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-110">In this example, the default value of the `IsBubbleSource` property is set to `false`.</span></span>  
  
 <span data-ttu-id="f3e7a-111">La classe de fournisseur pour une propriété jointe (même si elle n’est pas inscrite en tant que propriété de dépendance) doit fournir des accesseurs get et set statiques qui respectent la convention d’affectation de noms `Set`*[NomPropriétéJointe]* et `Get`*[NomPropriétéJointe]*.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-111">The provider class for an attached property (even if it is not registered as a dependency property) must provide static get and set accessors that follow the naming convention `Set`*[AttachedPropertyName]* and `Get`*[AttachedPropertyName]*.</span></span> <span data-ttu-id="f3e7a-112">Ces accesseurs sont nécessaires pour que le lecteur [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] puisse reconnaître la propriété en tant qu’attribut en [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] et résoudre les types appropriés.</span><span class="sxs-lookup"><span data-stu-id="f3e7a-112">These accessors are required so that the acting [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] reader can recognize the property as an attribute in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] and resolve the appropriate types.</span></span>  
  
 [!code-csharp[WPFAquariumSln#RegisterAttachedBubbler](~/samples/snippets/csharp/VS_Snippets_Wpf/WPFAquariumSln/CSharp/WPFAquariumObjects/Class1.cs#registerattachedbubbler)]
 [!code-vb[WPFAquariumSln#RegisterAttachedBubbler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WPFAquariumSln/visualbasic/wpfaquariumobjects/class1.vb#registerattachedbubbler)]  
  
## <a name="see-also"></a><span data-ttu-id="f3e7a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3e7a-113">See also</span></span>

- <xref:System.Windows.DependencyProperty>
- [<span data-ttu-id="f3e7a-114">Vue d’ensemble des propriétés de dépendance</span><span class="sxs-lookup"><span data-stu-id="f3e7a-114">Dependency Properties Overview</span></span>](dependency-properties-overview.md)
- [<span data-ttu-id="f3e7a-115">Propriétés de dépendance personnalisées</span><span class="sxs-lookup"><span data-stu-id="f3e7a-115">Custom Dependency Properties</span></span>](custom-dependency-properties.md)
- [<span data-ttu-id="f3e7a-116">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="f3e7a-116">How-to Topics</span></span>](properties-how-to-topics.md)
