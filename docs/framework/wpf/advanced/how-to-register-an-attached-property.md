---
title: 'Procédure : Enregistrer une propriété jointe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- attached properties [WPF], registering
- registering attached properties [WPF]
ms.assetid: eb47bd94-0451-4f8d-8fb6-95f7812ac05b
ms.openlocfilehash: 4c678a64b62b8f4db24cf39ffbafac52e56c9982
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768678"
---
# <a name="how-to-register-an-attached-property"></a>Procédure : Enregistrer une propriété jointe
Cet exemple montre comment inscrire une propriété jointe et fournir des accesseurs publics pour pouvoir utiliser la propriété en [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] et dans le code. Les propriétés jointes sont un concept de syntaxe défini par [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]. La plupart des propriétés jointes pour les types [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont également implémentées en tant que propriétés de dépendance. Vous pouvez utiliser les propriétés de dépendance sur n’importe quel <xref:System.Windows.DependencyObject> types.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment inscrire une propriété jointe comme une propriété de dépendance à l’aide de la <xref:System.Windows.DependencyProperty.RegisterAttached%2A> (méthode). La classe de fournisseur a la possibilité de fournir des métadonnées par défaut pour la propriété qui s’appliquent quand celle-ci est utilisée sur une autre classe, à moins que cette classe ne substitue les métadonnées. Dans cet exemple, la valeur par défaut de la propriété `IsBubbleSource` est définie sur `false`.  
  
 La classe de fournisseur pour une propriété jointe (même si elle n’est pas inscrite en tant que propriété de dépendance) doit fournir des accesseurs get et set statiques qui respectent la convention d’affectation de noms `Set`*[NomPropriétéJointe]* et `Get`*[NomPropriétéJointe]*. Ces accesseurs sont nécessaires pour que le lecteur [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] puisse reconnaître la propriété en tant qu’attribut en [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] et résoudre les types appropriés.  
  
 [!code-csharp[WPFAquariumSln#RegisterAttachedBubbler](~/samples/snippets/csharp/VS_Snippets_Wpf/WPFAquariumSln/CSharp/WPFAquariumObjects/Class1.cs#registerattachedbubbler)]
 [!code-vb[WPFAquariumSln#RegisterAttachedBubbler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WPFAquariumSln/visualbasic/wpfaquariumobjects/class1.vb#registerattachedbubbler)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.DependencyProperty>
- [Vue d’ensemble des propriétés de dépendance](dependency-properties-overview.md)
- [Propriétés de dépendance personnalisées](custom-dependency-properties.md)
- [Rubriques de guide pratique](properties-how-to-topics.md)
