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
# <a name="presentationoptionsfreeze-attribute"></a>PresentationOptions:Freeze, attribut
Définit le <xref:System.Windows.Freezable.IsFrozen%2A> état `true` sur la contenant <xref:System.Windows.Freezable> élément. Comportement par défaut un <xref:System.Windows.Freezable> sans le `PresentationOptions:Freeze` attribut spécifié est que <xref:System.Windows.Freezable.IsFrozen%2A> est `false` au moment de la charge et selon que vous général <xref:System.Windows.Freezable> comportement lors de l’exécution.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```  
<object  
  xmlns:PresentationOptions="http://schemas.microsoft.com/winfx/2006/xaml/presentation/options"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="PresentationOptions">  
    <freezableElement PresentationOptions:Freeze="true"/>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`PresentationOptions`|Un préfixe d’espace de noms XML, qui peut être n’importe quelle chaîne de préfixe valide conformément à la spécification XML 1.0. Le préfixe `PresentationOptions` est utilisé à des fins d’identification dans cette documentation.|  
|`freezableElement`|Un élément qui instancie toute classe dérivée de <xref:System.Windows.Freezable>.|  
  
## <a name="remarks"></a>Notes  
 Le `Freeze` attribut est le seul attribut ou élément de programmation défini dans le `http://schemas.microsoft.com/winfx/2006/xaml/presentation/options` espace de noms XML. Le `Freeze` attribut existe dans cet espace de noms spécial spécifiquement afin qu’il peut être désigné comme pouvant être ignoré, à l’aide de [mc : Ignorable, attribut](mc-ignorable-attribute.md) dans le cadre des déclarations d’élément racine. La raison qui `Freeze` doit pouvoir être ignoré n’étant donné que tous les [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] implémentations de processeur sont en mesure de figer un <xref:System.Windows.Freezable> au moment du chargement ; cette fonctionnalité n’est pas dans le cadre de la [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] spécification.  
  
 La possibilité de traiter la `Freeze` attribut spécifiquement intégré à la [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur traite [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] pour les applications compilées. L’attribut n’est pas pris en charge par n’importe quelle classe, et la syntaxe d’attribut n’est pas extensible ou modifiable. Si vous implémentez votre propre [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur, vous pouvez choisir du comportement de gel en parallèle la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur lors du traitement de la `Freeze` attribut sur <xref:System.Windows.Freezable> éléments au moment du chargement.  
  
 N’importe quelle valeur pour la `Freeze` attribut autre que `true` (non sensible à la casse) génère une erreur de temps de chargement. (En spécifiant le `Freeze` sous la forme `false` n’est pas une erreur, mais qui est déjà le paramètre par défaut, par conséquent, pour `false` n’a aucun effet).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Freezable>
- [Vue d’ensemble des objets Freezable](freezable-objects-overview.md)
- [mc:Ignorable, attribut](mc-ignorable-attribute.md)
