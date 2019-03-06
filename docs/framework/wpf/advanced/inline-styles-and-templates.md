---
title: Modèles et styles intralignes
ms.date: 03/30/2017
helpviewer_keywords:
- inline templates [WPF]
- styles [WPF], inline
- templates [WPF], inline
- inline styles [WPF]
ms.assetid: 69a1a3f9-acb5-4e2c-9c43-2e376c055ac4
ms.openlocfilehash: 6225e1abd2b6bb8c3598b08bb2a717340c435e77
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373385"
---
# <a name="inline-styles-and-templates"></a>Modèles et styles intralignes
[!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] Fournit des <xref:System.Windows.Style> objets et les objets de modèle (<xref:System.Windows.FrameworkTemplate> sous-classes) comme un moyen de définir l’apparence visuelle d’un élément dans les ressources, afin qu’ils peuvent être utilisés plusieurs fois. Pour cette raison, les attributs dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] qui prennent les types <xref:System.Windows.Style> et <xref:System.Windows.FrameworkTemplate> presque toujours font référence aux styles et modèles existant des ressources plutôt que définir de nouveaux inline.  
  
## <a name="limitations-of-inline-styles-and-templates"></a>Limitations des modèles et Styles intralignes  
 Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], pouvant techniquement définir les propriétés de style et de modèle de deux façons. Vous pouvez utiliser la syntaxe d’attribut pour référencer un style qui a été défini dans une ressource, par exemple `<` *objet*`Style="{StaticResource`*myResourceKey*`}" .../>`. Ou vous pouvez utiliser la syntaxe d’élément de propriété pour définir un style intraligne, par exemple :  
  
 `<` *object* `>`  
  
 `<` *object* `.Style>`  
  
 `<` `Style`  `.../>`  
  
 `</` *object* `.Style>`  
  
 `</` *object* `>`  
  
 L’utilisation de l’attribut est beaucoup plus courante. Un style qui est défini en ligne et les ressources non définis dans est nécessairement limité à l’élément conteneur uniquement et ne peut pas être réutilisé aussi facilement, car il n’a aucune clé de ressource. En général un style défini par la ressource est plus souple et utile et est plus conforme générales [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] principe de séparer la logique de programme dans le code de conception dans le balisage modèle de programmation.  
  
 En général il n’existe aucune raison pour définir un style ou un modèle en ligne, même si vous comptez utiliser uniquement ce style ou modèle à cet emplacement. La plupart des éléments qui peuvent prendre un style ou un modèle prennent également en charge une propriété de contenu et un modèle de contenu. Si vous utilisez uniquement l’arborescence logique vous créez dans un style ou de la création de modèles, il serait encore plus facile de renseigner simplement cette propriété de contenu avec les éléments enfants équivalents dans le balisage direct. Cela permettrait de contourner les mécanismes de style et de modèle complètement.  
  
 Autres syntaxes activées par les extensions de balisage qui retournent un objet sont également possibles pour les styles et modèles. Deux extensions des scénarios possibles incluent [TemplateBinding](templatebinding-markup-extension.md) et <xref:System.Windows.Data.Binding>.  
  
## <a name="see-also"></a>Voir aussi
- [Application d’un style et création de modèles](../controls/styling-and-templating.md)
