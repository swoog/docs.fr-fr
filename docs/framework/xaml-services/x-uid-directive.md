---
title: x:Uid, directive
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], localizable content attribute
- XAML [XAML Services], x:Uid attribute
- x:Uid attribute [XAML Services]
- Uid attribute [XAML Services]
ms.assetid: 81defade-483b-4a89-b76d-9b25bba34010
ms.openlocfilehash: 361240c2d2c140c7bf521ece423df4aaed075ba4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745413"
---
# <a name="xuid-directive"></a>x:Uid, directive
Fournit un identificateur unique pour les éléments de balisage. Dans de nombreux scénarios, cet identificateur unique est utilisé par les outils et processus de localisation de XAML.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object x:Uid="identifier"... />  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`identifier`|Créée manuellement ou chaîne générée automatiquement qui doit être unique dans un fichier lorsqu’il est interprété par une `x:Uid` consommateur.|  
  
## <a name="remarks"></a>Notes  
 Dans [MS-XAML], `x:Uid` est défini comme une directive. Pour plus d’informations, consultez [ \[MS-XAML\] Section 5.3.6](https://go.microsoft.com/fwlink/?LinkId=114525).  
  
 `x:Uid` est différent de `x:Name` à la fois en raison du scénario de localisation XAML déclaré et afin que les identificateurs qui sont utilisés pour la localisation n’ont aucune dépendance sur les conséquences de modèle de programmation de `x:Name`. En outre, `x:Name` est régie par la portée de nom XAML ; Toutefois, `x:Uid` n’est pas régi par n’importe quel concept de langage défini XAML de l’application l’unicité. Les processeurs XAML au sens large (processeurs qui ne font pas partie du processus de localisation) ne sont pas censés l’unicité des `x:Uid` valeurs. Cette responsabilité est conceptuellement sur le donneur d’ordre des valeurs. L’attente d’unicité de `x:Uid` valeurs dans une source XAML unique est justifiée pour les consommateurs des valeurs, telles que le processus de globalisation dédié ou d’outils. Le modèle d’unicité typique est que `x:Uid` sont uniques au sein d’un fichier XML qui représente le XAML.  
  
 Outils qui ont une connaissance significative d’un schéma XAML particulier peuvent choisir d’appliquer `x:Uid` uniquement pour les chaînes localisables true, au lieu de tous les cas où une valeur de chaîne de texte est rencontrée dans le balisage.  
  
 Frameworks peuvent spécifier une propriété particulière dans leur modèle d’objet comme étant un alias pour `x:Uid` en appliquant l’attribut <xref:System.Windows.Markup.UidPropertyAttribute> pour le type de définition. Si une infrastructure spécifie une propriété particulière, il n’est pas valide pour spécifier à la fois `x:Uid` et le membre ajouté en alias sur le même objet. Si les deux `x:Uid` et le membre ajouté en alias sont spécifiés, l’API de Services XAML .NET Framework lève généralement <xref:System.Xaml.XamlDuplicateMemberException> pour ce cas.  
  
## <a name="wpf-usage-notes"></a>Remarques sur l’utilisation WPF  
 Pour plus d’informations sur le rôle de `x:Uid` dans le processus de localisation WPF et dans le formulaire BAML de XAML, consultez [globalisation pour WPF](../../../docs/framework/wpf/advanced/globalization-for-wpf.md) ou <xref:System.Windows.Markup.Localizer.BamlLocalizableResourceKey.Uid%2A>  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Markup.Localizer.BamlLocalizableResourceKey.Uid%2A>
- <xref:Microsoft.Build.Tasks.Windows.UidManager>
- [Globalisation pour WPF](../../../docs/framework/wpf/advanced/globalization-for-wpf.md)
