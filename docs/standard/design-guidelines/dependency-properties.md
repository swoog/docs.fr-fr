---
title: Propriétés de dépendance
ms.date: 10/22/2008
ms.technology: dotnet-standard
ms.assetid: 212cfb1e-cec4-4047-94a6-47209b387f6f
author: KrzysztofCwalina
ms.openlocfilehash: 52d7a69a3f52c67ebff3f3db1daf0790e995913a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721957"
---
# <a name="dependency-properties"></a>Propriétés de dépendance
Une propriété de dépendance (DP) est une propriété normale qui stocke sa valeur dans une banque de propriétés au lieu de stockage dans une variable de type (champ), par exemple.  
  
 Une propriété de dépendance attachée est un type de propriété de dépendance modélisée comme des méthodes Get et Set statiques qui représente « propriétés », description des relations entre les objets et leurs conteneurs (par exemple, la position d’un `Button` de l’objet sur un `Panel` conteneur).  
  
 **✓ DO** fournissent les propriétés de dépendance, si vous avez besoin des propriétés pour prendre en charge des fonctionnalités WPF telles que les styles, les déclencheurs, liaison de données, des animations, ressources dynamiques et d’héritage.  
  
## <a name="dependency-property-design"></a>Conception des propriétés de dépendance  
 **✓ DO** hériter <xref:System.Windows.DependencyObject>, ou l’un de ses sous-types, lors de l’implémentation des propriétés de dépendance. Le type fournit une implémentation très efficace d’une banque de propriétés et prend automatiquement en charge la liaison de données WPF.  
  
 **✓ DO** fournir une propriété CLR normale et un champ statique public en lecture seule le stockage d’une instance de <xref:System.Windows.DependencyProperty?displayProperty=nameWithType> pour chaque propriété de dépendance.  
  
 **✓ DO** implémenter des propriétés de dépendance en appelant des méthodes d’instance <xref:System.Windows.DependencyObject.GetValue%2A?displayProperty=nameWithType> et <xref:System.Windows.DependencyObject.SetValue%2A?displayProperty=nameWithType>.  
  
 **✓ DO** nom du champ de propriété de dépendance statique par suffixant le nom de la propriété « Property ».  
  
 **X DO NOT** définir explicitement les valeurs par défaut des propriétés de dépendance dans le code ; les définir dans les métadonnées.  
  
 Si vous définissez explicitement une valeur par défaut de la propriété, vous pouvez empêcher cette propriété d’être définie par certains moyens implicites, par exemple, un style.  
  
 **X DO NOT** placez le code dans les accesseurs de propriété autre que le code standard pour accéder au champ statique.  
  
 Que code ne sont pas s’exécuter si la propriété est définie par des moyens implicites, par exemple, un style, étant donné que les styles d’utilise directement le champ statique.  
  
 **X DO NOT** utilise les propriétés de dépendance pour stocker des données sécurisées. Propriétés de dépendance même privés sont accessibles publiquement.  
  
## <a name="attached-dependency-property-design"></a>Conception des propriétés de dépendance attachée  
 Les propriétés de dépendance décrites dans la section précédente représentent les propriétés intrinsèques du type déclarant ; par exemple, le `Text` propriété est une propriété de `TextButton`, qui le déclare. Un type spécial de propriété de dépendance est la propriété de dépendance attachée.  
  
 Un exemple classique d’une propriété jointe est le <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> propriété. La propriété représente la position de colonne (pas de la grille) du bouton, mais cela s’applique uniquement si le bouton est contenu dans une grille, et donc il est « attaché » aux boutons par grilles.  
  
```xaml
<Grid>  
    <Grid.ColumnDefinitions>  
        <ColumnDefinition />  
        <ColumnDefinition />  
    </Grid.ColumnDefinitions>  
  
    <Button Grid.Column="0">Click</Button>  
    <Button Grid.Column="1">Clack</Button>  
</Grid>  
```  
  
 La définition d’une propriété jointe ressemble principalement que d’une propriété de dépendance standard, à ceci près que les accesseurs sont représentés par les méthodes Get et Set statiques :  
  
```csharp
public class Grid {  
  
    public static int GetColumn(DependencyObject obj) {  
        return (int)obj.GetValue(ColumnProperty);  
    }  
  
    public static void SetColumn(DependencyObject obj, int value) {  
        obj.SetValue(ColumnProperty,value);  
    }  
  
    public static readonly DependencyProperty ColumnProperty =  
        DependencyProperty.RegisterAttached(  
            "Column",  
            typeof(int),  
            typeof(Grid)  
    );  
}  
```  
  
## <a name="dependency-property-validation"></a>Validation de propriété de dépendance  
 Propriétés implémentent souvent ce que l'on appelle la validation. La logique de validation s’exécute lorsqu’une tentative est effectuée pour modifier la valeur d’une propriété.  
  
 Malheureusement les accesseurs de propriété de dépendance ne peut pas contenir de code de validation arbitraire. Au lieu de cela, logique de validation de propriété de dépendance doit être spécifié lors de l’inscription de propriété.  
  
 **X DO NOT** placer la logique de validation de propriété de dépendance dans les accesseurs de la propriété. Au lieu de cela, passez un rappel de validation à `DependencyProperty.Register` (méthode).  
  
## <a name="dependency-property-change-notifications"></a>Notifications de modification de propriété de dépendance  
 **X DO NOT** implémenter la logique de notification de modification dans les accesseurs de propriété de dépendance. Propriétés de dépendance ont une fonctionnalité de notifications de modifications intégré qui doit être utilisée en fournissant un rappel de notification de modification pour le <xref:System.Windows.PropertyMetadata>.  
  
## <a name="dependency-property-value-coercion"></a>Forçage de valeur de propriété de dépendance  
 Contrainte de propriété a lieu lorsque la valeur donnée à un accesseur Set de propriété est modifiée par la méthode setter avant que la banque de propriétés est en fait modifiée.  
  
 **X DO NOT** implémenter la logique de la contrainte dans les accesseurs de propriété de dépendance.  
  
 Propriétés de dépendance ont une fonctionnalité de forçage intégré, et il peut être utilisé en fournissant un rappel de forçage de type pour le `PropertyMetadata`.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Modèles de design courants](../../../docs/standard/design-guidelines/common-design-patterns.md)
