---
title: ComponentResourceKey, extension de balisage
ms.date: 03/30/2017
f1_keywords:
- ComponentResourceKey
- ComponentResourceKeyExtension
helpviewer_keywords:
- ComponentResourceKey markup extension [WPF]
- XAML [WPF], ComponentResourceKey markup extension
ms.assetid: d6bcdbe6-61b3-40a7-b381-4e02185b5a85
ms.openlocfilehash: 5f72d6c3273cfda4276383cfe72f90196e5d4340
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59169752"
---
# <a name="componentresourcekey-markup-extension"></a>ComponentResourceKey, extension de balisage
Définit et référence des clés pour les ressources qui sont chargés à partir des assemblys externes. Cela permet une recherche de ressource spécifier un type de cible dans un assembly, plutôt qu’un dictionnaire de ressources explicite dans un assembly ou une classe.  
  
## <a name="xaml-attribute-usage-setting-key-compact"></a>Utilisation d’attributs XAML (définition de la clé, compacte)  
  
```xml  
<object x:Key="{ComponentResourceKey {x:Type targetTypeName}, targetID}" .../>  
```  
  
## <a name="xaml-attribute-usage-setting-key-verbose"></a>Utilisation d’attributs XAML (définition de clé, détaillé)  
  
```xml  
<object x:Key="{ComponentResourceKey TypeInTargetAssembly={x:Type targetTypeName}, ResourceID=targetID}" .../>  
```  
  
## <a name="xaml-attribute-usage-requesting-resource-compact"></a>Utilisation d’attributs XAML (demande de ressource, compact)  
  
```xml  
<object property="{DynamicResource {ComponentResourceKey {x:Type targetTypeName}, targetID}}" .../>  
```  
  
## <a name="xaml-attribute-usage-requesting-resource-verbose"></a>Utilisation d’attributs XAML (demande de ressource, détaillé)  
  
```xml  
<object property="{DynamicResource {ComponentResourceKey TypeInTargetAssembly={x:Type targetTypeName}, ResourceID=targetID}}" .../>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`targetTypeName`|Le nom du public [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] type qui est défini dans l’assembly de ressource.|  
|`targetID`|La clé pour la ressource. Lors de la recherche de ressources, `targetID` sera analogue à la [Directive x : Key](../../xaml-services/x-key-directive.md) de la ressource.|  
  
## <a name="remarks"></a>Notes  
 Comme indiqué dans les utilisations ci-dessus, un {`ComponentResourceKey`} extension de balisage est trouvée dans deux emplacements :  
  
-   La définition d’une clé dans un dictionnaire de ressources de thème, tel que fourni par un auteur de contrôle.  
  
-   L’accès à une ressource de thème à partir de l’assembly, lorsque vous êtes recréation d’un modèle du contrôle, mais pour utiliser les valeurs de propriété provenant de ressources fournies par les thèmes du contrôle.  
  
 Pour faire référence à des ressources de composant qui proviennent de thèmes, il est généralement recommandé d’utiliser `{DynamicResource}` plutôt que `{StaticResource}`. Cela est illustré dans les utilisations. `{DynamicResource}` est recommandée car le thème lui-même peut être modifié par l’utilisateur. Si vous souhaitez que la ressource de composant qui correspond le mieux à intention de l’auteur du contrôle pour prendre en charge un thème, vous devez activer votre référence de ressource de composant d’être également dynamique.  
  
 Le <xref:System.Windows.ComponentResourceKey.TypeInTargetAssembly%2A> identifie un type qui existe dans l’assembly cible où la ressource est réellement définie. Un `ComponentResourceKey` peut être définie et utilisée indépendamment de savoir exactement où le <xref:System.Windows.ComponentResourceKey.TypeInTargetAssembly%2A> est défini, mais finalement doit résoudre le type via les assemblys référencés.  
  
 Une utilisation courante pour <xref:System.Windows.ComponentResourceKey> consiste à définir des clés qui sont ensuite exposées en tant que membres d’une classe. Pour cela, vous utilisez le <xref:System.Windows.ComponentResourceKey> constructeur de classe, pas l’extension de balisage. Pour plus d’informations, consultez <xref:System.Windows.ComponentResourceKey>, ou la section « Définition et référencement de clés pour les ressources de thème » de la rubrique [vue d’ensemble de la création de contrôles](../controls/control-authoring-overview.md).  
  
 Pour établir des clés et faisant référence à des ressources de clé, syntaxe d’attribut est généralement utilisée pour le `ComponentResourceKey` extension de balisage.  
  
 La syntaxe compacte indiquée s’appuie sur le <xref:System.Windows.ComponentResourceKey.%23ctor%2A?displayProperty=nameWithType> signature de constructeur et l’utilisation des paramètres positionnels d’une extension de balisage. L’ordre dans lequel le `targetTypeName` et `targetID` sont donné est important. La syntaxe détaillée s’appuie sur le <xref:System.Windows.ComponentResourceKey.%23ctor%2A?displayProperty=nameWithType> constructeur par défaut, puis définit la <xref:System.Windows.ComponentResourceKey.TypeInTargetAssembly%2A> et <xref:System.Windows.ComponentResourceKey.ResourceId%2A> d’une manière qui est analogue à la syntaxe d’attribut réelle sur un élément objet. Dans la syntaxe détaillée, l’ordre dans lequel les propriétés sont définies n’est pas important. La relation et les mécanismes de ces deux alternatives (compacte et détaillés) est décrite plus en détail dans la rubrique [Extensions de balisage et WPF XAML](markup-extensions-and-wpf-xaml.md).  
  
 Techniquement, la valeur de `targetID` peut être n’importe quel objet, il ne devra pas être une chaîne. Toutefois, l’utilisation la plus courante dans WPF est d’aligner la `targetID` valeur avec des formulaires qui sont des chaînes, et où ces chaînes sont valides dans le [XamlName, grammaire](../../xaml-services/xamlname-grammar.md).  
  
 `ComponentResourceKey` peut être utilisé dans la syntaxe d’élément objet. Dans ce cas, en spécifiant la valeur des deux le <xref:System.Windows.ComponentResourceKey.TypeInTargetAssembly%2A> et <xref:System.Windows.ComponentResourceKey.ResourceId%2A> propriétés est requis pour initialiser correctement l’extension.  
  
 Dans le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] implémentation de lecteur, la gestion de cette extension de balisage est définie par le <xref:System.Windows.ComponentResourceKey> classe.  
  
 `ComponentResourceKey` est une extension de balisage. Les extensions de balisage sont généralement implémentées pour éviter que les valeurs d’attribut ne soient autre chose que des valeurs littérales ou des noms de gestionnaire et lorsque l’exigence dépasse le cadre de la définition de convertisseurs de type sur certains types ou propriétés. Toutes les extensions de balisage [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] utilisent les caractères { et } dans leur syntaxe d’attribut, convention selon laquelle un processeur [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] reconnaît qu’une extension de balisage doit traiter l’attribut. Pour plus d’informations, consultez [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.ComponentResourceKey>
- <xref:System.Windows.Controls.ControlTemplate>
- [Vue d’ensemble de la création de contrôles](../controls/control-authoring-overview.md)
- [Vue d’ensemble du langage XAML (WPF)](xaml-overview-wpf.md)
- [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md)
