---
title: mc:ProcessContent, attribut
ms.date: 03/30/2017
helpviewer_keywords:
- mc:ProcessContent attribute
- XAML [WPF], mc:ProcessContent attribute
ms.assetid: 2689b2c8-b4dc-4b71-b9bd-f95e619122d7
ms.openlocfilehash: a9af18d1fac9101a75ac16918adf8e86ef7d2ba4
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357376"
---
# <a name="mcprocesscontent-attribute"></a>mc:ProcessContent, attribut
Spécifie les [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] éléments doivent toujours avoir contenu traité par les éléments parents pertinents, même si l’élément parent immédiat peut être ignoré par un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur en raison de la spécification [mc : Ignorable, attribut](mc-ignorable-attribute.md) . Le `mc:ProcessContent` attribut prend en charge la compatibilité du balisage à la fois pour le mappage d’espace de noms personnalisé et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] le contrôle de version.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```  
<object  
  xmlns:ignorablePrefix="ignorableUri"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix"...  
  mc:ProcessContent="ignorablePrefix:ThisElementCanBeIgnored"  
>  
    <ignorablePrefix:ThisElementCanBeIgnored>  
        [content]  
    </ignorablePrefix:ThisElementCanBeIgnored>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|*ignorablePrefix*|N’importe quelle chaîne de préfixe valide, conformément à la spécification XML 1.0.|  
|*ignorableUri*|N’importe quel URI valide pour la désignation d’un espace de noms, conformément à la spécification XML 1.0.|  
|*ThisElementCanBeIgnored*|Un élément qui peut être ignoré par [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] implémentations de processeur, si le type sous-jacent ne peut pas être résolu.|  
|*[content]*|*ThisElementCanBeIgnored* est marqué comme pouvant être ignoré. Si le processeur ignore cet élément, *[content]* est traité par *objet*.|  
  
## <a name="remarks"></a>Notes  
 Par défaut, un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur ignore le contenu d’un élément ignoré. Vous pouvez spécifier un élément spécifique par `mc:ProcessContent`et un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] processeur continue à traiter le contenu dans l’élément ignoré. Cela doit généralement être utilisé si le contenu est imbriqué dans plusieurs balises, au moins un d'entre eux peut être ignoré et au moins un d'entre eux n’est pas peut être ignoré.  
  
 Plusieurs préfixes peuvent être spécifiés dans l’attribut, à l’aide d’un espace de séparation, par exemple : `mc:ProcessContent="ignore:Element1 ignore:Element2"`.  
  
 Le [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] espace de noms définit les autres éléments et attributs qui ne sont pas documentés dans cette zone de la [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)]. Pour plus d’informations, consultez [spécification de compatibilité du balisage XML](https://go.microsoft.com/fwlink/?LinkId=73824).  
  
## <a name="see-also"></a>Voir aussi
- [mc:Ignorable, attribut](mc-ignorable-attribute.md)
- [Vue d’ensemble du langage XAML (WPF)](xaml-overview-wpf.md)
