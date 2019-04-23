---
title: x:Arguments, directive
ms.date: 03/30/2017
helpviewer_keywords:
- x:Arguments directive [XAML Services]
- Arguments directive in XAML [XAML Services]
- XAML [XAML Services], x:Arguments directive
ms.assetid: 87cc10b0-b610-4025-b6b0-ab27ca27c92e
ms.openlocfilehash: a87542513ffeeec7efc526d4218f921d1b7579a1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59184845"
---
# <a name="xarguments-directive"></a>x:Arguments, directive
Arguments de construction de packages pour une déclaration d’élément objet constructeur non-par défaut dans XAML, ou pour une déclaration d’objet de fabrique (méthode).  
  
## <a name="xaml-element-usage-nondefault-constructor"></a>Utilisation de l’élément XAML (constructeur non défini par défaut)  
  
```  
<object ...>  
  <x:Arguments>  
    oneOrMoreObjectElements  
  </x:Arguments>  
</object>  
```  
  
## <a name="xaml-element-usage-factory-method"></a>Utilisation de l’élément XAML (méthode de fabrique)  
  
```  
<object x:FactoryMethod="methodName"...>  
  <x:Arguments>  
    oneOrMoreObjectElements  
  </x:Arguments>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`oneOrMoreObjectElements`|Un ou plusieurs éléments objet qui spécifient les arguments à passer à la méthode de constructeur ou de fabrique par défaut de stockage.<br /><br /> Utilisation typique consiste à utiliser le texte d’initialisation dans les éléments objet pour spécifier les valeurs d’argument réel. Consultez la section Exemples.<br /><br /> L’ordre des éléments est significatif. Les types XAML dans l’ordre doivent correspondre les types et ordre de type de la surcharge de méthode de constructeur ou de la fabrique de sauvegarde.|  
|`methodName`|Le nom de la méthode de fabrique qui doit traiter tous `x:Arguments` arguments.|  
  
## <a name="dependencies"></a>Dépendances  
 `x:FactoryMethod` peut modifier l’étendue et le comportement où `x:Arguments` s’applique.  
  
 Si aucun `x:FactoryMethod` est spécifié, `x:Arguments` s’applique pour alterner des signatures (non définis par défaut) des constructeurs de stockage.  
  
 Si `x:FactoryMethod` est spécifié, `x:Arguments` s’applique à une surcharge de la méthode nommée.  
  
## <a name="remarks"></a>Notes  
 XAML 2006 peut prendre en charge l’initialisation non définis par défaut dans le texte de l’initialisation. Toutefois, l’application pratique d’une technique de construction de texte d’initialisation est limitée. Texte d’initialisation est traité comme une chaîne de texte unique ; Par conséquent, il ajoute uniquement la capacité pour une initialisation de paramètre, sauf si un convertisseur de type est défini pour le comportement de construction qui peut analyser des éléments d’informations personnalisées et les délimiteurs personnalisés à partir de la chaîne. En outre, la chaîne de texte à la logique de l’objet est potentiellement convertisseur de type natif par défaut d’un analyseur XAML donnée pour la gestion des primitives de chaîne true.  
  
 Le `x:Arguments` l’utilisation XAML n’est pas utilisation d’élément de propriété dans le sens classique, étant donné que le balisage de directive ne référence pas de type de l’élément objet contenant. Cela correspond davantage à autres directives telles que `x:Code` où l’élément dénote une plage dans laquelle la balise doit être interprétée comme autre que la valeur par défaut pour le contenu enfant. Dans ce cas, le type XAML de chaque élément d’objet communique des informations sur les types d’arguments, qui sont utilisées par les analyseurs XAML pour déterminer quelle signature de méthode de fabrique constructeur spécifique un `x:Arguments` utilisation tentative de référencement.  
  
 `x:Arguments` pour un élément de l’objet en cours de construction doit précéder les autres éléments de propriété, du contenu, texte interne ou chaînes d’initialisation de l’élément objet. Les éléments objet dans `x:Arguments` peut inclure des attributs et des chaînes d’initialisation, comme autorisé par ce type XAML et sa méthode de constructeur ou de la fabrique de sauvegarde. Pour l’objet ou les arguments, vous pouvez spécifier les types XAML personnalisés ou les types XAML qui sont sinon en dehors de l’espace de noms XAML par défaut en référençant les mappages de préfixe établis.  
  
 Les processeurs XAML utilisent les instructions suivantes pour déterminer la façon dont les arguments spécifiés dans `x:Arguments` doit être utilisé pour construire un objet. Si `x:FactoryMethod` est spécifié, les informations sont comparées spécifié `x:FactoryMethod` (Notez que la valeur de `x:FactoryMethod` est le nom de méthode et la méthode nommée peut avoir des surcharges. Si `x:FactoryMethod` n’est pas spécifié, les informations sont comparées à l’ensemble de toutes les surcharges de constructeur public de l’objet. Logique de traitement XAML puis compare le nombre de paramètres et sélectionne la surcharge avec l’arité correspondante. S’il existe plus d’une correspondance, le processeur XAML doit comparer les types des paramètres basés sur les types XAML des éléments objet fourni. S’il existe plus d’une correspondance, le comportement du processeur XAML est indéfini. Si un `x:FactoryMethod` est spécifié, mais la méthode ne peut pas être résolue, un processeur XAML doit lever une exception.  
  
 L’utilisation d’un attribut XAML `<x:Arguments>string</x:Arguments>` est techniquement possible. Toutefois, cela ne fournit aucune des fonctionnalités au-delà de ce qui peut être fait sinon via les convertisseurs de texte et le type d’initialisation, et à l’aide de cette syntaxe n’est pas l’intention de conception des fonctionnalités de méthode de fabrique XAML 2009.  
  
## <a name="examples"></a>Exemples  
 L’exemple suivant montre un constructeur non défini par défaut de signature, puis l’utilisation XAML de `x:Arguments` qui accède à cette signature.  
  
```csharp  
public class Food {  
    private string _name;  
    private Int32 _calories;  
    public Food(string name, Int32 calories) {  
        _name=name;  
        _calories=calories;  
    }  
}  
```  
  
```xaml  
<my:Food>  
    <x:Arguments>  
        <x:String>Apple</x:String>  
        <x:Int32>150</x:Int32>  
    </x:Arguments>  
</my:Food>  
```  
  
 L’exemple suivant montre une signature de méthode de fabrique cible, puis l’utilisation XAML de `x:Arguments` qui accède à cette signature.  
  
```csharp  
public Food TryLookupFood(string name)  
{  
  switch (name) {  
    case "Apple": return new Food("Apple",150);  
    case "Chocolate": return new Food("Chocolate",200);  
    case "Cheese": return new Food("Cheese", 450);  
    default: {return new Food(name,0);  
  }  
}  
```  
  
```xaml  
<my:Food x:FactoryMethod="TryLookupFood">  
    <x:Arguments>  
        <x:String>Apple</x:String>  
    </x:Arguments>  
</my:Food>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Définition de types personnalisés pour une utilisation avec les services XAML .NET Framework](defining-custom-types-for-use-with-net-framework-xaml-services.md)
- [Vue d’ensemble du langage XAML (WPF)](../wpf/advanced/xaml-overview-wpf.md)
