---
title: x:Key, directive
ms.date: 03/30/2017
f1_keywords:
- xKey
- Key
- x:Key
helpviewer_keywords:
- x:Key attribute [XAML Services]
- Key attribute in XAML [XAML Services]
- XAML [XAML Services], x:Key attribute
ms.assetid: 1985cd45-f197-42d5-b75e-886add64b248
ms.openlocfilehash: f77f0a952224f79ee95a755cb848a4f8b68c9602
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47112768"
---
# <a name="xkey-directive"></a>x:Key, directive
Identifie les éléments qui sont créés et référencés dans un dictionnaire défini en XAML. Ajout d’un `x:Key` valeur à un élément d’objet XAML est la méthode la plus courante pour identifier une ressource dans un dictionnaire de ressources, par exemple dans un WPF <xref:System.Windows.ResourceDictionary>.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```  
<object x:Key="stringKeyValue".../>  
-or-  
<object x:Key="{markupExtensionUsage}".../>  
```  
  
## <a name="xaml-attribute-usage-wpf-specific"></a>Utilisation d’attributs XAML (spécifique à WPF)  
  
```  
<object.Resources>  
  <object x:Key="stringKeyValue".../>  
</object.Resources>  
-or-  
<object.Resources>  
  <object x:Key="{markupExtensionUsage}".../>  
</object.Resources>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`stringKeyValue`|Une chaîne de texte à utiliser en tant que clé. La chaîne de texte doit être conforme à la [XamlName, grammaire](../../../docs/framework/xaml-services/xamlname-grammar.md).|  
|`markupExtensionUsage`|Dans les délimiteurs d’extension de balisage {}, une extension de balisage qui fournit un objet à utiliser en tant que clé. Consultez la section Notes.|  
  
## <a name="remarks"></a>Notes  
 `x:Key` prend en charge le concept de dictionnaire de ressources XAML. XAML en tant que langage ne définit pas une implémentation de dictionnaire de ressources, qui est laissée aux infrastructures d’interface utilisateur spécifiques. Pour en savoir plus sur la façon dont les dictionnaires de ressources XAML sont implémentés dans WPF, consultez [XAML ressources](../../../docs/framework/wpf/advanced/xaml-resources.md).  
  
 Dans XAML 2006 et WPF, `x:Key` doit être fourni en tant qu’attribut. Vous pouvez toujours utiliser des clés, mais cela requiert une extension de balisage afin de fournir la valeur de chaîne sous forme d’attribut. Si vous utilisez XAML 2009, `x:Key` peut être spécifié en tant qu’élément, pour prendre en charge explicitement des dictionnaires indexés par les types d’objets autres que des chaînes sans exiger une extension de balisage intermédiaire. Consultez la section « XAML 2009 » dans cette rubrique. Le reste de la section Notes s’applique spécifiquement à l’implémentation XAML 2006.  
  
 La valeur d’attribut `x:Key` peut être n’importe quelle chaîne définie dans le [XamlName, grammaire](../../../docs/framework/xaml-services/xamlname-grammar.md) ou à un objet évalué via une extension de balisage. Pour obtenir un exemple de WPF, consultez « Remarques sur l’utilisation WPF ».  
  
 Les éléments enfants d’un élément parent qui est une <xref:System.Collections.IDictionary> implémentation doit généralement inclure un `x:Key` attribut qui spécifie une valeur de clé unique dans ce dictionnaire. Frameworks peuvent implémenter des propriétés de clé d’un alias pour remplacer les `x:Key` sur des types particuliers ; les types qui définissent de telles propriétés doivent être attribués avec <xref:System.Windows.Markup.DictionaryKeyPropertyAttribute>.  
  
 Le code équivalent de la spécification `x:Key` est la clé qui est utilisée pour sous-jacent <xref:System.Collections.IDictionary>. Par exemple, un `x:Key` qui est appliqué dans le balisage pour une ressource dans WPF équivaut à la valeur de la `key` paramètre de <xref:System.Windows.ResourceDictionary.Add%2A?displayProperty=nameWithType> lorsque vous ajoutez la ressource à un WPF <xref:System.Windows.ResourceDictionary> dans le code.  
  
## <a name="wpf-usage-notes"></a>Remarques sur l’utilisation WPF  
 Les objets enfants d’un parent de l’objet qui est un <xref:System.Collections.IDictionary> implémentation, telles que le WPF <xref:System.Windows.ResourceDictionary>, doivent généralement inclure un `x:Key` attribut et la valeur de clé doivent être unique dans ce dictionnaire. Il existe deux exceptions notables :  
  
-   Certains types WPF déclarent une clé implicite pour l’utilisation de dictionnaire. Par exemple, un <xref:System.Windows.Style> avec un <xref:System.Windows.Style.TargetType%2A>, ou un <xref:System.Windows.DataTemplate> avec un <xref:System.Windows.DataTemplate.DataType%2A>, peuvent se trouver dans un <xref:System.Windows.ResourceDictionary> et utilisez la clé implicite.  
  
-   WPF prend en charge un concept de dictionnaire de ressources fusionné. Les clés peuvent être partagées entre les dictionnaires fusionnés, et le comportement de la clé partagée est accessible à l’aide de <xref:System.Windows.FrameworkContentElement.FindResource%2A>. Pour plus d’informations, consultez [Dictionnaires de ressources fusionnés](../../../docs/framework/wpf/advanced/merged-resource-dictionaries.md).  
  
 Dans le WPF XAML implémentation et l’application modèle global, l’unicité clé n’est pas vérifiée par le compilateur de balisage XAML. Au lieu de cela, manquantes ou non uniques `x:Key` valeurs provoquent des erreurs au moment du chargement de l’analyseur XAML. Toutefois, la gestion de Visual Studio de dictionnaires pour WPF peuvent souvent noter ces erreurs dans la phase de conception.  
  
 Notez que dans la syntaxe affichée, le <xref:System.Windows.ResourceDictionary> objet est implicite dans la façon dont le processeur WPF XAML produit une collection pour remplir une <xref:System.Windows.FrameworkElement.Resources%2A> collection. Un <xref:System.Windows.ResourceDictionary> est généralement pas fourni explicitement en tant qu’élément dans le balisage, bien qu’il peut être dans certains cas, si vous souhaitiez par souci de clarté (il serait un élément objet de collection entre le <xref:System.Windows.FrameworkElement.Resources%2A> élément de propriété et les éléments qui remplissent la dictionnaire). Pour plus d’informations sur la raison pour laquelle un objet de collection est presque toujours un élément implicite dans le balisage, consultez [syntaxe de XAML en détail](../../../docs/framework/wpf/advanced/xaml-syntax-in-detail.md).  
  
 Dans l’implémentation WPF XAML, la gestion de clés de dictionnaire de ressources est définie par le <xref:System.Windows.ResourceKey> classe abstraite. Toutefois, le processeur WPF XAML produit différents types d’extension sous-jacents pour les clés en fonction de leur utilisation. Par exemple, la clé pour un <xref:System.Windows.DataTemplate> ou n’importe quelle classe dérivée est gérée séparément et produit distinct <xref:System.Windows.DataTemplateKey> objet.  
  
 Clés et les noms utilisent des directives et des différents éléments de langage (`x:Key` et `x:Name`) dans la définition XAML de base. Clés et les noms sont également utilisés dans des situations différentes par la définition WPF et l’application de ces concepts. Pour plus d’informations, consultez [portées de nom XAML WPF](../../../docs/framework/wpf/advanced/wpf-xaml-namescopes.md).  
  
 Comme indiqué précédemment, la valeur d’une clé peut être fournie via une extension de balisage et peut être différente d’une valeur de chaîne. Un exemple de scénario WPF est que la valeur de `x:Key` peut être un [ComponentResourceKey](../../../docs/framework/wpf/advanced/componentresourcekey-markup-extension.md). Certains contrôles exposent une clé de style de ce type pour une ressource de style personnalisée qui influence une partie de l’apparence et le comportement de ce contrôle sans remplacer le style totalement. Est un exemple d’une telle clé <xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>.  
  
 La fonctionnalité de dictionnaire fusionné WPF ajoute des considérations supplémentaires pour l’unicité clé et le comportement de recherche de clé. Pour plus d’informations, consultez [Dictionnaires de ressources fusionnés](../../../docs/framework/wpf/advanced/merged-resource-dictionaries.md).  
  
## <a name="xaml-2009"></a>XAML 2009  
 XAML 2009 assouplit la restriction qui `x:Key` toujours être fourni sous forme d’attribut.  
  
 Dans WPF, vous pouvez utiliser les fonctionnalités XAML 2009, mais uniquement pour le XAML non compilé par balisage. Le code XAML compilé par balisage pour WPF et la forme BAML du code XAML ne prennent actuellement pas en charge les mots clés et les fonctionnalités XAML 2009.  
  
 En XAML 2009, vous pouvez spécifier `x:Key` éléments via l’utilisation suivante :  
  
### <a name="xaml-element-usage-xaml-2009-only"></a>Utilisation de l’élément XAML (XAML 2009 uniquement)  
  
```  
<object>  
  <x:Key>  
keyObject  
  </x:Key>  
...  
</object>  
```  
  
### <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`keyObject`|Élément objet pour l’objet qui est utilisé comme clé pour une donnée `object` dans un dictionnaire spécialisé.|  
  
-   Le conteneur/parent pour ce type d’utilisation n’est pas affiché ici. `object` est censé être un enfant d’un élément objet qui représente une implémentation de dictionnaire spécialisé. `keyObject` est supposé être une instance d’objet (ou une valeur d’un type valeur) qui est appropriée comme clé pour cette implémentation de dictionnaire spécialisée particulière.  
  
-   WPF n’implémente pas les dictionnaires qui requièrent cette utilisation. Clés d’objet est plus une fonctionnalité générale du langage XAML, éventuellement utile pour certains scénarios de dictionnaire personnalisé où il est souhaitable de création du dictionnaire en XAML. Pour les fonctionnalités WPF telles que les styles implicites qui utilisent des clés de non-chaîne pour les ressources, autres techniques pour l’établissement ou la spécification des clés existent, à l’aide d’une clé d’objet n’est pas nécessaire.  
  
-   *keyObject* peut également être une extension de balisage dans le formulaire d’élément objet, plutôt que d’une instance d’objet direct.  
  
## <a name="silverlight-usage-notes"></a>Remarques sur l’utilisation de Silverlight  
 `x:Key` pour Silverlight est documenté séparément. Pour plus d’informations, consultez [XAML Namespace (x :)) Fonctionnalités de langage (Silverlight)](https://go.microsoft.com/fwlink/?LinkId=199081).  
  
## <a name="see-also"></a>Voir aussi  
 [Ressources XAML](../../../docs/framework/wpf/advanced/xaml-resources.md)  
 [Ressources et code](../../../docs/framework/wpf/advanced/resources-and-code.md)  
 [StaticResource, extension de balisage](../../../docs/framework/wpf/advanced/staticresource-markup-extension.md)
