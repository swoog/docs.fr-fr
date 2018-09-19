---
title: Noms de classes, de structures et d'interfaces
ms.date: 03/30/2017
helpviewer_keywords:
- type names, guidelines
- classes [.NET Framework], names
- enumerations [.NET Framework], names
- names [.NET Framework], interfaces
- common type names
- names [.NET Framework], type names
- names [.NET Framework], classes
- interfaces [.NET Framework], names
- generic type parameters
ms.assetid: 87a4b0da-ed64-43b1-ac43-968576c444ce
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0c56f840bc5ebd5070c9b686384751acab3f0203
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45972544"
---
# <a name="names-of-classes-structs-and-interfaces"></a>Noms de classes, de structures et d'interfaces
Les instructions d’affectation de noms qui suivent s’appliquent au type général d’affectation de noms.  
  
 **✓ DO** un nom de classes et structs avec des noms ou des expressions nominales, à l’aide de la casse Pascal.  
  
 Cette particularité le distingue les noms de types à partir de méthodes, qui sont nommés avec des expressions de verbe.  
  
 **✓ DO** nom interfaces phrases adjectivales ou parfois avec des noms ou des expressions nominales.  
  
 Noms et des expressions nominales doivent être utilisées rarement et ils peuvent indiquer que le type doit être une classe abstraite et pas une interface.  
  
 **X DO NOT** donner des noms de classe un préfixe (par exemple, « C »).  
  
 **✓ CONSIDER** se terminant par le nom de classes dérivées portant le nom de la classe de base.  
  
 Cela est très lisible et explique clairement de la relation. Voici quelques exemples de ce code : `ArgumentOutOfRangeException`, qui est un type de `Exception`, et `SerializableAttribute`, qui est un type de `Attribute`. Toutefois, il est important d’utiliser Réfléchissez soigneusement en appliquant cette recommandation ; par exemple, le `Button` classe est une sorte de `Control` événement, bien que `Control` n’apparaît pas dans son nom.  
  
 **✓ DO** préfixe les noms d’interface avec la lettre I, pour indiquer que le type est une interface.  
  
 Par exemple, `IComponent` (nom descriptif), `ICustomAttributeProvider` (expression nominale), et `IPersistable` (adjectif) sont des noms de l’interface appropriée. Comme avec d’autres noms de types, évitez d’abréviations.  
  
 **✓ DO** vous assurer que les noms diffèrent uniquement par « I » du préfixe du nom de l’interface lorsque vous définissez une paire : interface de classe dans laquelle la classe est une implémentation standard de l’interface.  
  
## <a name="names-of-generic-type-parameters"></a>Noms des paramètres de Type générique  
 Les génériques ont été ajoutés à .NET Framework 2.0. La fonctionnalité introduit un nouveau type d’identificateur appelé *le paramètre de type*.  
  
 **✓ DO** nom des paramètres de type générique avec des noms descriptifs, sauf si un nom de lettre unique est complètement explicite et un nom descriptif ajouterait pas de valeur.  
  
 **✓ CONSIDER** à l’aide de `T` comme nom de paramètre de type pour les types avec un paramètre de type de lettre unique.  
  
```  
public int IComparer<T> { ... }  
public delegate bool Predicate<T>(T item);  
public struct Nullable<T> where T:struct { ... }  
```  
  
 **✓ DO** préfixe des noms de paramètre de type descriptifs avec `T`.  
  
```  
public interface ISessionChannel<TSession> where TSession : ISession {  
    TSession Session { get; }  
}  
```  
  
 **✓ CONSIDER** indiquer les contraintes placées sur un paramètre de type dans le nom du paramètre.  
  
 Par exemple, un paramètre limité à `ISession` peut être appelée `TSession`.  
  
## <a name="names-of-common-types"></a>Noms des Types courants  
 **✓ DO** suivez les instructions décrites dans le tableau suivant lorsque vous nommez des types dérivés ou implémenter certains types .NET Framework.  
  
|Base Type|Règle de Type dérivé et l’implémentation de|  
|---------------|------------------------------------------|  
|`System.Attribute`|**✓ DO** ajouter le suffixe « Attribute » aux noms des classes d’attributs personnalisés.|  
|`System.Delegate`|**✓ DO** ajouter le suffixe « EventHandler » aux noms de délégués qui sont utilisés dans les événements.<br /><br /> **✓ DO** ajouter le suffixe « Rappel » aux noms de délégués autres que ceux utilisés en tant que gestionnaires d’événements.<br /><br /> **X DO NOT** ajouter le suffixe « Délégué » à un délégué.|  
|`System.EventArgs`|**✓ DO** ajouter le suffixe « EventArgs ».|  
|`System.Enum`|**X DO NOT** dériver de cette classe ; utilisez le mot clé pris en charge par votre langage à la place ; par exemple, en c#, utilisez le `enum` (mot clé).<br /><br /> **X DO NOT** ajouter le suffixe « Enum » ou « Indicateur ».|  
|`System.Exception`|**✓ DO** ajouter le suffixe « Exception ».|  
|`IDictionary` <br /> `IDictionary<TKey,TValue>`|**✓ DO** ajouter le suffixe « Dictionnaire ». Notez que `IDictionary` est un type spécifique de collection, mais cette instruction est prioritaire sur la règle de collections plus générale qui suit.|  
|`IEnumerable` <br /> `ICollection` <br /> `IList` <br /> `IEnumerable<T>` <br /> `ICollection<T>` <br /> `IList<T>`|**✓ DO** ajouter le suffixe « Collection ».|  
|`System.IO.Stream`|**✓ DO** ajouter le suffixe « Stream ».|  
|`CodeAccessPermission IPermission`|**✓ DO** ajouter le suffixe « Autorisation ».|  
  
## <a name="naming-enumerations"></a>Énumérations d’affectation de noms  
 Noms des types énumération (également appelés enums) en général doivent respecter les règles d’affectation de noms de type standard (casse Pascal, etc.). Toutefois, il existe des recommandations supplémentaires qui s’appliquent spécifiquement aux enums.  
  
 **✓ DO** utiliser un nom de type au singulier pour une énumération, sauf si ses valeurs sont les champs de bits.  
  
 **✓ DO** utiliser un nom de type au pluriel pour une énumération avec les champs de bits sous forme de valeurs, également appelés enum d’indicateurs.  
  
 **X DO NOT** utiliser le suffixe « Enum » dans les noms de type enum.  
  
 **X DO NOT** utiliser « Indicateur » ou tapez les noms des suffixes « Indicateurs » dans l’enum.  
  
 **X DO NOT** utiliser un préfixe sur les noms de valeur d’énumération (par exemple, « ad » pour les énumérations ADO.), « rtf » pour les énumérations de texte enrichi, etc.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
