---
title: mc:Ignorable, attribut
ms.date: 03/30/2017
helpviewer_keywords:
- mc XML namespace prefix [WPF]
- mc:Ignorable attribute
- XML [WPF], mc namespace prefix
- XAML [WPF], mc:Ignorable attribute
- mc:ProcessContent attribute
- XAML [WPF], mc:ProcessContent attribute
ms.assetid: acd9a6ef-b7ca-4146-abb6-60f3b366e9ec
ms.openlocfilehash: 03439a2c4a1a4de375e90d0e5121e690541e2f0f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59219328"
---
# <a name="mcignorable-attribute"></a>mc:Ignorable, attribut
Spécifie les [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] préfixes d’espace de noms rencontrés dans un fichier de balisage peuvent être ignorés par un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur. Le `mc:Ignorable` attribut prend en charge la compatibilité du balisage à la fois pour le mappage d’espace de noms personnalisé et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] le contrôle de version.  
  
## <a name="xaml-attribute-usage-single-prefix"></a>Utilisation d’attributs XAML (un seul préfixe)  
  
```  
<object  
  xmlns:ignorablePrefix="ignorableUri"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix"...>  
    <ignorablePrefix1:ThisElementCanBeIgnored/>  
</object>  
```  
  
## <a name="xaml-attribute-usage-two-prefixes"></a>Utilisation d’attributs XAML (deux préfixes)  
  
```  
<object  
  xmlns:ignorablePrefix1="ignorableUri"  
  xmlns:ignorablePrefix2="ignorableUri2"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix1 ignorablePrefix2"...>  
    <ignorablePrefix1:ThisElementCanBeIgnored/>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|*ignorablePrefix, ignorablePrefix1, etc.*|N’importe quelle chaîne de préfixe valide, conformément à la spécification XML 1.0.|  
|*ignorableUri*|N’importe quel URI valide pour la désignation d’un espace de noms, conformément à la spécification XML 1.0.|  
|*ThisElementCanBeIgnored*|Un élément qui peut être ignoré par [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] implémentations de processeur, si le type sous-jacent ne peut pas être résolu.|  
  
## <a name="remarks"></a>Notes  
 Le `mc` [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] préfixe d’espace de noms est la convention de préfixe recommandé à utiliser lors du mappage le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] espace de noms de compatibilité [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)].  
  
 Éléments ou attributs où la partie préfixe de nom de l’élément sont identifiés comme `mc:Ignorable` ne déclenchent pas d’erreurs lors du traitement par un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur. Si cet attribut n’a pas pu être résolu en un type sous-jacent ou la construction de programmation, cet élément est ignoré. Notez toutefois que les éléments ignorés peuvent générer des erreurs d’analyse supplémentaires pour les spécifications d’éléments supplémentaires qui sont les effets de cet élément n’est pas traitée. Par exemple, un modèle de contenu d’élément particulier peut nécessiter un seul élément enfant, mais si l’élément enfant spécifié était dans un `mc:Ignorable` préfixe et l’élément enfant spécifié n’a pas pu être résolue en un type, puis le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur peut génère une erreur.  
  
 `mc:Ignorable` s’applique uniquement aux mappages d’espace de noms pour les chaînes d’identificateur. `mc:Ignorable` ne s’applique pas aux mappages d’espace de noms dans des assemblys, qui spécifient un [!INCLUDE[TLA2#tla_clr](../../../../includes/tla2sharptla-clr-md.md)] espace de noms et un assembly (ou par défaut le fichier exécutable actuel en tant que l’assembly).  
  
 Si vous implémentez un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur, votre implémentation de processeur ne doit pas déclencher l’analyse ou de traitement des erreurs sur la résolution de type pour tout élément ou attribut est qualifié par un préfixe qui est identifié comme `mc:Ignorable`. Mais votre implémentation de processeur peut toujours déclencher des exceptions qui sont le résultat d’un élément ne parvient pas à charger ou être traitées, comme l’exemple d’élément enfant de celui donné précédemment secondaire.  
  
 Par défaut, un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur ignore le contenu d’un élément ignoré. Toutefois, vous pouvez spécifier un attribut supplémentaire, [MC : ProcessContent attribut](mc-processcontent-attribute.md), afin de demander la poursuite du traitement du contenu d’un élément ignoré par l’élément parent disponible suivant.  
  
 Plusieurs préfixes peuvent être spécifiés dans l’attribut, à l’aide d’un ou plusieurs caractères d’espace blanc comme séparateur, par exemple : `mc:Ignorable="ignore1 ignore2"`.  

 Le [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] espace de noms définit les autres éléments et attributs qui ne sont pas documentés dans cette zone de la [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)]. Pour plus d’informations, consultez [spécification de compatibilité du balisage XML](/office/open-xml/introduction-to-markup-compatibility#markup-compatibility-in-the-open-xml-file-formats-specification).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Markup.XamlReader>
- [PresentationOptions:Freeze, attribut](presentationoptions-freeze-attribute.md)
- [Vue d’ensemble du langage XAML (WPF)](xaml-overview-wpf.md)
- [Documents dans WPF](documents-in-wpf.md)
