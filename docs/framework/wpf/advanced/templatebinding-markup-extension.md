---
title: TemplateBinding, extension de balisage
ms.date: 03/30/2017
f1_keywords:
- TemplateBinding
- TemplateBindingExtension
helpviewer_keywords:
- XAML [WPF], TemplateBinding markup extension
- TemplateBinding markup extensions [WPF]
ms.assetid: 1d25bbfc-dbc2-499d-9f12-419d23d4ac6a
ms.openlocfilehash: c004560a0b7ab367fbf4fbb48b0e8d8b63f3d8f4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59155998"
---
# <a name="templatebinding-markup-extension"></a>TemplateBinding, extension de balisage
Cette extension lie la valeur d'une propriété dans un modèle de contrôle afin de la définir comme valeur d'une autre propriété exposée dans le contrôle basé sur un modèle.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xml  
<object property="{TemplateBinding sourceProperty}" .../>  
```  
  
## <a name="xaml-attribute-usage-for-setter-property-in-template-or-style"></a>Utilisation d'attributs XAML (pour la propriété de méthode setter dans le modèle ou le style)  
  
```xml  
<Setter Property="propertyName" Value="{TemplateBinding sourceProperty}" .../>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`propertyName`|<xref:System.Windows.DependencyProperty.Name%2A?displayProperty=nameWithType> de la propriété définie dans la syntaxe de méthode setter.|  
|`sourceProperty`|Autre propriété de dépendance qui existe sur le type basé sur un modèle, spécifiée par <xref:System.Windows.DependencyProperty.Name%2A?displayProperty=nameWithType>.<br /><br /> ou<br /><br /> Nom de propriété « dotted-down » défini par un autre type que le type de cible basé sur un modèle. Il s'agit en réalité d'un <xref:System.Windows.PropertyPath>. Consultez [PropertyPath XAML syntaxe](propertypath-xaml-syntax.md).|  
  
## <a name="remarks"></a>Notes  
 Un `TemplateBinding` est une version optimisée d’un [liaison](binding-markup-extension.md) pour les scénarios de modèle, analogues à un `Binding` construit avec `{Binding RelativeSource={RelativeSource TemplatedParent}}`. `TemplateBinding` est toujours une liaison unidirectionnelle, même si les propriétés ont comme valeur par défaut des liaisons bidirectionnelles. Les deux propriétés doivent toutes être des propriétés de dépendance. Pour atteindre une liaison bidirectionnelle à un parent basé sur un modèle utilisez l’instruction suivante de la liaison à la place `{Binding RelativeSource={RelativeSource TemplatedParent}, Mode=TwoWay, Path=MyDependencyProperty}`. 
  
 [RelativeSource](relativesource-markupextension.md) est une autre extension de balisage parfois utilisée avec ou au lieu de `TemplateBinding` afin d’effectuer la liaison de propriété relative dans un modèle.  
  
 Décrire les modèles de contrôle comme un concept n’est pas couverte ici ; Pour plus d’informations, consultez [Styles et modèles Control](../controls/control-styles-and-templates.md).  
  
 La syntaxe d’attribut est la syntaxe la plus couramment utilisée avec cette extension de balisage. Le jeton de chaîne fourni après la chaîne d’identificateur `TemplateBinding` est assigné en tant que valeur <xref:System.Windows.TemplateBindingExtension.Property%2A> de la classe d’extension <xref:System.Windows.TemplateBindingExtension> sous-jacente.  
  
 La syntaxe d'élément objet est possible, mais elle n'est pas indiquée car elle ne possède aucune application réaliste. `TemplateBinding` est utilisé pour remplir les expressions de valeurs dans des méthodes setter, à l’aide d’évaluées et à l’aide de la syntaxe d’élément objet `TemplateBinding` pour remplir `<Setter.Property>` syntaxe d’élément de propriété est inutilement détaillé.  
  
 `TemplateBinding` peut également être utilisé dans une utilisation d’attributs en clair qui spécifie la <xref:System.Windows.TemplateBindingExtension.Property%2A> propriété en tant que propriété = paire valeur :  
  
```xml  
<object property="{TemplateBinding Property=sourceProperty}" .../>  
```  
  
 L'utilisation en clair est souvent utile pour les extensions qui comportent plusieurs propriétés définissables ou si certaines propriétés sont facultatives. `TemplateBinding` ne comportant qu'une seule propriété définissable (obligatoire), cette utilisation en clair n'est pas classique.  
  
 Dans le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] implémentation du processeur XAML, la gestion de cette extension de balisage est définie par le <xref:System.Windows.TemplateBindingExtension> classe.  
  
 `TemplateBinding` est une extension de balisage. Les extensions de balisage sont généralement implémentées pour éviter que les valeurs d’attribut ne soient autre chose que des valeurs littérales ou des noms de gestionnaire et lorsque l’exigence dépasse le cadre de la définition de convertisseurs de type sur certains types ou propriétés. Toutes les extensions de balisage en cours d’utilisation XAML le `{` et `}` caractères dans leur syntaxe d’attribut, qui est la convention selon laquelle un processeur XAML reconnaît qu’une extension de balisage doit traiter l’attribut. Pour plus d’informations, consultez [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Style>
- <xref:System.Windows.Controls.ControlTemplate>
- [Application d'un style et création de modèles](../controls/styling-and-templating.md)
- [Vue d’ensemble du langage XAML (WPF)](xaml-overview-wpf.md)
- [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md)
- [RelativeSource, extension de balisage](relativesource-markupextension.md)
- [Binding, extension de balisage](binding-markup-extension.md)
