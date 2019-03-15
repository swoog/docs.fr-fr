---
title: x:FieldModifier, directive
ms.date: 03/30/2017
helpviewer_keywords:
- FieldModifier attribute in XAML [XAML Services]
- x:FieldModifier attribute [XAML Services]
- XAML [XAML Services], x:FieldModifier attribute
ms.assetid: ed427cd4-2f35-4d24-bd2f-0fa7b71ec248
ms.openlocfilehash: 27ff9d027f5ff5155543097b7f0f0c2839387fe5
ms.sourcegitcommit: 5c1abeec15fbddcc7dbaa729fabc1f1f29f12045
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58042450"
---
# <a name="xfieldmodifier-directive"></a>x:FieldModifier, directive
Modifie le comportement de compilation XAML afin que les champs pour les références d’objet nommé sont définis avec <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> accéder à la place de la <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> comportement par défaut.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object x:FieldModifier="Public".../>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|*Public*|La chaîne exacte que vous passez pour spécifier <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> et <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> varie selon le langage de programmation de code-behind qui est utilisé. Consultez la section Notes.|  
  
## <a name="dependencies"></a>Dépendances  
 Si une production XAML utilise `x:FieldModifier` n’importe où, l’élément racine de cette production XAML doit déclarer un [x : Class Directive](x-class-directive.md).  
  
## <a name="remarks"></a>Notes  
 `x:FieldModifier` n’est pas pertinent pour déclarer le niveau d’accès général d’une classe ou de ses membres. Il est pertinent uniquement pour le comportement de traitement XAML lorsqu’un objet XAML particulier qui fait partie d’une production XAML est traité et devienne un objet qui est potentiellement accessible dans le graphique d’objet d’une application. Par défaut, la référence de champ pour un tel objet reste privée, ce qui empêche les consommateurs de contrôle de modifier le graphique d’objet directement. Au lieu de cela, les consommateurs de contrôle sont attendus pour modifier le graphique d’objets à l’aide de modèles standard qui sont activées par les modèles de programmation, comme en obtenant la racine de disposition, l’enfant de collections d’éléments, les propriétés publiques dédiées, et ainsi de suite.  
  
 La valeur de la `x:FieldModifier` attribut varie selon le langage de programmation et son objectif peut varier dans les infrastructures spécifiques. La chaîne à utiliser dépend de la façon dont chaque langage implémente son <xref:System.CodeDom.Compiler.CodeDomProvider> et les convertisseurs de type qu’il retourne pour définir les significations de <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> et <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType>, et si cette langue est sensible à la casse.  
  
-   Pour c#, la chaîne à passer pour désigner <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> est `public`.  
  
-   Pour Microsoft Visual Basic .NET, la chaîne à passer pour désigner <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> est `Public`.  
  
-   Pour [!INCLUDE[TLA2#tla_cppcli](../../../includes/tla2sharptla-cppcli-md.md)], n’existe actuellement aucune cible pour XAML ; par conséquent, la chaîne à passer n’est pas définie.  
  
 Vous pouvez également spécifier <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> (`internal` dans C#, `Friend` en Visual Basic), mais en spécifiant <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> est inhabituel, car `NotPublic` comme le comportement est déjà la valeur par défaut.  
  
 <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> est le comportement par défaut car il est rare que le code en dehors de l’assembly compilé le XAML a besoin d’accéder à un élément créé en XAML. Architecture de sécurité WPF avec un comportement de compilation XAML ne sera pas déclarer de champs qui stockent les instances d’élément comme public, sauf si vous définissez spécifiquement le `x:FieldModifier` pour autoriser l’accès public.  
  
 `x:FieldModifier` concerne uniquement les éléments avec un [Directive x : Name](x-name-directive.md) , car ce nom est utilisé pour référencer le champ une fois qu’il est public.  
  
 Par défaut, la classe partielle pour l’élément racine est publique ; Toutefois, vous pouvez rendre non publics à l’aide de la [x : ClassModifier, Directive](x-classmodifier-directive.md). Le [x : ClassModifier, Directive](x-classmodifier-directive.md) affecte également le niveau d’accès de l’instance de la classe d’élément racine. Vous pouvez placer les deux `x:Name` et `x:FieldModifier` sur la racine de l’élément, mais cela rend uniquement une copie du champ public de l’élément racine, avec le niveau d’accès racine true élément classe toujours contrôlée par [x : ClassModifier, Directive](x-classmodifier-directive.md).  
  
## <a name="see-also"></a>Voir aussi
- [XAML et classes personnalisées pour WPF](../wpf/advanced/xaml-and-custom-classes-for-wpf.md)
- [Code-behind et XAML dans WPF](../wpf/advanced/code-behind-and-xaml-in-wpf.md)
- [x:Name, directive](x-name-directive.md)
- [Génération d’une application WPF (WPF)](../wpf/app-development/building-a-wpf-application-wpf.md)
- [x:ClassModifier, directive](x-classmodifier-directive.md)
