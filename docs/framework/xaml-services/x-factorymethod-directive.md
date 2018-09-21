---
title: x:FactoryMethod, directive
ms.date: 03/30/2017
helpviewer_keywords:
- XAML. x:FactoryMethod directive [XAML Services]
- FactoryMethod directive in XAML [XAML Services]
- x:FactoryMethod directive [XAML Services]
ms.assetid: 829bcbdf-5318-4afb-9a03-c310e0d2f23d
ms.openlocfilehash: 436caa9b93467dcf2a0763bcc0962a2beb722315
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46532373"
---
# <a name="xfactorymethod-directive"></a>x:FactoryMethod, directive
Spécifie une méthode autre qu’un constructeur qu’un processeur XAML doit utiliser pour initialiser un objet après avoir résolu son type de stockage.  
  
## <a name="xaml-attribute-usage-no-xarguments"></a>Utilisation d’attribut XAML, aucune x : Arguments  
  
```  
<object x:FactoryMethod="methodname"...>  
  ...  
</object>  
```  
  
## <a name="xaml-attribute-usage-xarguments-as-elements"></a>Utilisation d’attribut XAML, x : Arguments comme élément (s)  
  
```  
<object x:FactoryMethod="methodname"...>  
  <x:Arguments>  
    oneOrMoreObjectElements  
  </x:Arguments>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`methodname`|Le nom de méthode de chaîne d’une méthode que les processeurs XAML appellent pour initialiser l’instance spécifiée en tant que `object`. Consultez la section Notes.|  
|`oneOrMoreObjectElements`|Un ou plusieurs éléments objet pour les objets qui spécifient les paramètres de méthode de fabrique. Ordre est significatif ; Il désigne l’ordre dans lequel les arguments doivent être passés à la méthode de fabrique.|  
  
## <a name="remarks"></a>Notes  
 Si `methodname` est une méthode d’instance, il ne peut pas être qualifié.  
  
 Les méthodes statiques en tant que méthodes de fabrique sont prises en charge. Si `methodname` est une méthode statique, `methodname` est fourni comme un *typeName*. *methodName* combinaison, où *typeName* nomme la classe qui définit la méthode de fabrique statique. *typeName* peut être qualifié par un préfixe s’il fait référence à un type dans un fichier xmlns mappé. *typeName* peut être un type différent de `typeof(object)`.  
  
 La méthode de fabrique doit être une méthode déclarée publique du type qui stocke l’élément objet appropriée.  
  
 La méthode de fabrique doit retourner une instance qui ne peut être assignée à l’objet correspondant. Méthodes de fabrique ne doivent jamais retourner null.  
  
 `x:Arguments` fonctionne sur un principe de meilleure correspondance pour les signatures de méthodes de fabrique. Mise en correspondance évalue d’abord le nombre de paramètres. S’il existe plusieurs correspondances possibles pour un nombre de paramètres, type de paramètre est évaluée et la meilleure correspondance est déterminée. S’il reste une ambiguïté après cette phase d’évaluation, le comportement du processeur XAML est indéfini.  
  
 Le `x:FactoryMethod` utilisation de l’élément n’est pas utilisation d’élément de propriété dans le sens classique, étant donné que le balisage de directive ne référence pas de type de l’élément objet contenant. Il est probable que l’utilisation d’élément est moins fréquentes que l’utilisation d’attribut. `x:Arguments` (utilisation d’attribut ou élément) peut être utilisée avec `x:FactoryMethod` utilisation de l’élément, mais cela n’est pas spécifiquement indiqué dans les sections de l’utilisation.  
  
 `x:FactoryMethod` comme un élément doit précéder tous les autres éléments de propriété, il doit précéder tout `x:Arguments` également fourni en tant qu’éléments et doit précéder n’importe quel contenu/interne texte/texte d’initialisation.  
  
## <a name="see-also"></a>Voir aussi  
 [x:Arguments (directive)](../../../docs/framework/xaml-services/x-arguments-directive.md)
