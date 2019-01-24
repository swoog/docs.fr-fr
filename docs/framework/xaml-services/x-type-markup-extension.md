---
title: x:Type, extension de balisage
ms.date: 03/30/2017
f1_keywords:
- x:TypeExtension
- Type
- x:Type
- xType
- TypeExtension
helpviewer_keywords:
- x:Type markup extension [XAML Services]
- XAML [XAML Services], x:Type markup extension
- XAML [XAML Services], TargetType attribute
- TargetType attribute [XAML Services]
- Type markup extension in XAML [XAML Services]
ms.assetid: e0e0ce6f-e873-49c7-8ad7-8b840eb353ec
ms.openlocfilehash: 2fc44163db99be5a0f2ddb2820053a5bdda3ccbe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668988"
---
# <a name="xtype-markup-extension"></a>x:Type, extension de balisage
Fournit le CLR <xref:System.Type> objet qui est le type sous-jacent pour un type XAML spécifié.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object property="{x:Type prefix:typeNameValue}" .../>  
```  
  
## <a name="xaml-object-element-usage"></a>Utilisation d'éléments objet XAML  
  
```xaml  
<x:Type TypeName="prefix:typeNameValue"/>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`prefix`|Facultatif. Un préfixe qui mappe un espace de noms XAML par défaut. En spécifiant un préfixe n’est généralement pas nécessaire. Consultez la section Notes.|  
|`typeNameValue`|Obligatoire. Un nom de type peut être résolu à l’espace de noms XAML par défaut actuel ; ou spécifié préfixe mappé si `prefix` est fourni.|  
  
## <a name="remarks"></a>Notes  
 Le `x:Type` extension de balisage possède une fonction similaire à la `typeof()` opérateur en c# ou le `GetType` opérateur dans Microsoft Visual Basic.  
  
 Le `x:Type` extension de balisage fournisse un comportement de conversion de chaîne pour les propriétés qui prennent le type <xref:System.Type>. L’entrée est un type XAML. La relation entre le type XAML d’entrée et la sortie CLR <xref:System.Type> est que la sortie <xref:System.Type> est la <xref:System.Xaml.XamlType.UnderlyingType%2A> de l’entrée <xref:System.Xaml.XamlType>, après avoir recherché le nécessaire <xref:System.Xaml.XamlType> selon le contexte de schéma XAML et le <xref:System.Windows.Markup.IXamlTypeResolver>fournit le contexte de service.  
  
 Dans les Services XAML .NET Framework, la gestion de cette extension de balisage est définie par le <xref:System.Windows.Markup.TypeExtension> classe.  
  
 Dans les implémentations d’infrastructure spécifiques, certaines propriétés qui acceptent <xref:System.Type> comme une valeur peut accepter le nom du type directement (la valeur de chaîne du type `Name`). Toutefois, l’implémentation de ce comportement est un scénario complexe. Pour obtenir des exemples, consultez la section « Notes d’utilisation WPF » qui suit.  
  
 La syntaxe d’attribut est la syntaxe la plus couramment utilisée avec cette extension de balisage. Le jeton de chaîne fourni après la chaîne d’identificateur `x:Type` est assigné en tant que valeur <xref:System.Windows.Markup.TypeExtension.TypeName%2A> de la classe d’extension <xref:System.Windows.Markup.TypeExtension> sous-jacente. Dans le contexte de schéma XAML par défaut pour les Services XAML .NET Framework, qui est basée sur les types CLR, la valeur de cet attribut est soit le <xref:System.Reflection.MemberInfo.Name%2A> du type souhaité, ou qui contient <xref:System.Reflection.MemberInfo.Name%2A> précédé par un préfixe pour un espace de noms XAML par défaut mappage.  
  
 Le `x:Type` extension de balisage peut être utilisée dans la syntaxe d’élément objet. Dans ce cas, en spécifiant la valeur de la <xref:System.Windows.Markup.TypeExtension.TypeName%2A> propriété est requise pour initialiser correctement l’extension.  
  
 Le `x:Type` extension de balisage peut également être utilisée comme un attribut verbose ; toutefois cette utilisation n’est pas classique : `<object property="{x:Type TypeName=typeNameValue}" .../>`  
  
## <a name="wpf-usage-notes"></a>Remarques sur l’utilisation WPF  
  
### <a name="default-xaml-namespace-and-type-mapping"></a>Namespace XAML et mappage de Type par défaut  
 L’espace de noms XAML par défaut pour la programmation WPF contient la plupart des types XAML que vous avez besoin pour les scénarios XAML standard ; Par conséquent, vous pouvez souvent éviter les préfixes lors du référencement de valeurs de type XAML. Vous devrez peut-être mapper un préfixe si vous référencez un type à partir d’un assembly personnalisé ou pour les types qui existent dans un assembly WPF mais qui sont dans un espace de noms CLR qui n’a pas été mappé à l’espace de noms XAML par défaut. Pour plus d’informations sur les préfixes, les espaces de noms XAML et mappage CLR, consultez [espaces de noms XAML et mappage Namespace pour WPF XAML](../../../docs/framework/wpf/advanced/xaml-namespaces-and-namespace-mapping-for-wpf-xaml.md).  
  
### <a name="type-properties-that-support-typename-as-string"></a>Cette prise en charge Typename en tant que chaîne de propriétés de type  
 WPF prend en charge les techniques qui permettent de spécifier la valeur de certaines propriétés de type <xref:System.Type> sans nécessiter une `x:Type` extension de balisage. Au lieu de cela, vous pouvez spécifier la valeur sous forme de chaîne qui désigne le type. Des exemples sont <xref:System.Windows.Controls.ControlTemplate.TargetType%2A?displayProperty=nameWithType> et <xref:System.Windows.Style.TargetType%2A?displayProperty=nameWithType>. Prise en charge de ce comportement n’est pas fourni par le biais des convertisseurs de type ou les extensions de balisage. Au lieu de cela, il s’agit d’un comportement de report implémenté via <xref:System.Windows.FrameworkElementFactory>.  
  
 Silverlight prend en charge une convention similaire. En fait, Silverlight ne prend pas actuellement en charge `{x:Type}` dans sa prise en charge du langage XAML et n’accepte pas `{x:Type}` utilisations en dehors de certaines circonstances sont destinées à prendre en charge la migration de WPF-Silverlight XAML. Par conséquent, le comportement typename as string est intégré à toutes les évaluation de propriété native de Silverlight où un <xref:System.Type> est la valeur.  
  
## <a name="xaml-2009"></a>XAML 2009  
 XAML 2009 prend également en charge pour les types génériques et modifie le comportement de la fonctionnalité de `x:TypeArguments` et `x:Type` pour fournir cette prise en charge.  
  
-   `x:TypeArguments` et l’élément objet associé pour une instanciation d’objet générique peut se trouver sur des éléments autres que la racine. Pour plus d’informations, consultez la section « XAML 2009 » de [x : TypeArguments Directive](../../../docs/framework/xaml-services/x-typearguments-directive.md).  
  
-   XAML 2009 prend en charge une syntaxe permettant de spécifier la contrainte d’un type générique dans le balisage. Cela peut être utilisé par `x:TypeArguments`, par `x:Type`, ou par les deux fonctionnalités conjointement.  
  
-   Implémentation WPF XAML lors du traitement de XAML 2009 pour le chargement ajoute également cette fonctionnalité pour le comportement de conversion de type implicite pour certaines propriétés de l’infrastructure qui utilisent le type <xref:System.Type>.  
  
 Dans WPF, vous pouvez utiliser les fonctionnalités XAML 2009, mais uniquement pour XAML libre (XAML non compilé par balisage). Le code XAML compilé par balisage pour WPF et la forme BAML du code XAML ne prennent actuellement pas en charge les mots clés et les fonctionnalités XAML 2009.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Style>
- [Application d’un style et création de modèles](../../../docs/framework/wpf/controls/styling-and-templating.md)
- [Vue d’ensemble du langage XAML (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
- [Extensions de balisage et XAML WPF](../../../docs/framework/wpf/advanced/markup-extensions-and-wpf-xaml.md)
