---
title: x:Subclass, directive
ms.date: 03/30/2017
f1_keywords:
- Subclass
- xSubclass
- x:Subclass
helpviewer_keywords:
- x:Subclass attribute [XAML Services]
- XAML [XAML Services], x:Subclass attribute
- Subclass attribute in XAML [XAML Services]
ms.assetid: 99f66072-8107-4362-ab99-8171dc83b469
ms.openlocfilehash: 67d699782cd2ce2b13e159d2b7218b4868a8794c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670925"
---
# <a name="xsubclass-directive"></a>x:Subclass, directive
Modifie le comportement de compilation du balisage XAML lorsque `x:Class` est également fourni. Au lieu de créer une classe partielle qui est basée sur `x:Class`, fourni `x:Class` est créée comme une classe intermédiaire, et ensuite votre classe dérivée fournie est censée être basée sur `x:Class`.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```  
<object x:Class="namespace.classname" x:Subclass="subclassNamespace.subclassName">  
   ...  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`namespace`|Facultatif. Spécifie un espace de noms CLR contenant `classname`. Si `namespace` est spécifié, un point (.) sépare `namespace` et `classname`.|  
|`classname`|Obligatoire. Spécifie le nom CLR de la classe partielle qui connecte le XAML chargé et votre code-behind pour ce XAML. Consultez la section Notes.|  
|`subclassNamespace`|Facultatif. Peut être différent de `namespace` si chaque espace de noms peut résoudre l’autre. Spécifie un espace de noms CLR contenant `subclassName`. Si `subclassName` est spécifié, un point (.) sépare `subclassNamespace` et `subclassName`.|  
|`subclassName`|Obligatoire. Spécifie le nom CLR de la sous-classe.|  
  
## <a name="dependencies"></a>Dépendances  
 [x : Class Directive](../../../docs/framework/xaml-services/x-class-directive.md) doit également être fourni dans le même objet, et cet objet doit être l’élément racine de la production XAML.  
  
## <a name="remarks"></a>Notes  
 `x:Subclass` l’utilisation est destiné aux langages qui ne prennent pas en charge les déclarations de classe partielle.  
  
 La classe utilisée comme le `x:Subclass` ne peut pas être une classe imbriquée, et `x:Subclass` doit faire référence à l’objet racine, comme expliqué dans la section « Dépendances ».  
  
 Sinon, la signification conceptuelle de `x:Subclass` n’est pas définie par une implémentation de Services XAML du .NET Framework. Il s’agit, car le comportement des Services XAML du .NET Framework ne spécifie pas le modèle de programmation global par quels XAML balisage et code de stockage sont connectés. Les implémentations de concepts supplémentaires liées à `x:Class` et `x:Subclass` sont effectuées par les infrastructures spécifiques qui utilisent des modèles de programmation ou des modèles d’application pour définir comment connecter le balisage XAML, compilée de balisage et code-behind basé sur CLR. Chaque framework peut avoir ses propres actions de génération qui activent une partie du comportement, ou des composants spécifiques qui doivent être inclus dans l’environnement de génération. Dans une infrastructure, les actions de génération peuvent également varier selon le langage CLR spécifique qui est utilisé pour le code-behind.  
  
## <a name="wpf-usage-notes"></a>Remarques sur l’utilisation WPF  
 `x:Subclass` peut être sur une racine de la page ou le <xref:System.Windows.Application> racine dans la définition d’application, ce qui a déjà `x:Class`. Déclaration `x:Subclass` sur tout élément autre qu’une racine de page ou une application, ou sa spécification lorsqu’aucun `x:Class` existe, provoque une erreur de compilation.  
  
 Création de classes dérivées qui fonctionnent correctement pour le `x:Subclass` scénario est assez complexe. Vous devrez peut-être examiner les fichiers intermédiaires (les fichiers .g produits dans le dossier obj de votre projet par la compilation du balisage, avec des noms qui incorporent les noms de fichier .xaml). Ces fichiers intermédiaires peuvent vous aider à déterminer l’origine de certaines constructions de programmation dans les classes partielles jointes dans l’application compilée.  
  
 Gestionnaires d’événements dans la classe dérivée doivent être `internal override` (`Friend Overrides` dans Microsoft Visual Basic) afin de substituer les stubs pour les gestionnaires créés dans la classe intermédiaire pendant la compilation. Sinon, les implémentations de classe dérivée masqueront l’implémentation de la classe intermédiaire et les gestionnaires de classe intermédiaire ne sont pas appelés.  
  
 Lorsque vous définissez les deux `x:Class` et `x:Subclass`, vous n’avez pas besoin de fournir une implémentation de la classe qui est référencée par `x:Class`. Vous devez uniquement lui donner un nom via le `x:Class` attribut afin que le compilateur présente quelques conseils pour la classe qu’il crée dans les fichiers intermédiaires (dans ce cas, le compilateur ne sélectionne pas de nom par défaut). Vous pouvez donner le `x:Class` une implémentation de la classe ; Toutefois, ce n’est pas le scénario classique d’utilisation à la fois `x:Class` et `x:Subclass`.  
  
## <a name="see-also"></a>Voir aussi
- [x:Class, directive](../../../docs/framework/xaml-services/x-class-directive.md)
- [XAML et classes personnalisées pour WPF](../../../docs/framework/wpf/advanced/xaml-and-custom-classes-for-wpf.md)
