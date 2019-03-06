---
title: 'Procédure : Définir une portée de nom'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- name scope [WPF], defining
- Storyboards [WPF], animating in procedural code
- animation [WPF], Storyboards [WPF], in procedural code
ms.assetid: 4f361925-6a08-40dc-8231-a61111c6b28b
ms.openlocfilehash: 6afb59550d774109c62c283905495c76b0834b3d
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370369"
---
# <a name="how-to-define-a-name-scope"></a>Procédure : Définir une portée de nom
Pour animer avec <xref:System.Windows.Media.Animation.Storyboard> dans le code, vous devez créer un <xref:System.Windows.NameScope> et enregistrer les noms des objets de la cible avec l’élément qui possède cette portée de nom. Dans l’exemple suivant, un <xref:System.Windows.NameScope> est créé pour `myMainPanel`. Deux boutons, `button1` et `button2`, sont ajoutées pour le panneau de configuration et leurs noms enregistrés. Plusieurs animations et un <xref:System.Windows.Media.Animation.Storyboard> sont créés. La table de montage séquentiel <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> méthode est utilisée pour démarrer les animations.  
  
 Étant donné que `button1`, `button2`, et `myMainPanel` partagent tous la même portée de nom, l’un d’eux peut être utilisé avec le <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> méthode pour démarrer les animations.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[StoryboardBeginAnimation_procedural_snip#NameScopeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/CSharp/ScopeExample.cs#namescopeexample)]
 [!code-vb[StoryboardBeginAnimation_procedural_snip#NameScopeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/visualbasic/scopeexample.vb#namescopeexample)]  
  
## <a name="see-also"></a>Voir aussi
- [Animer une propriété à l’aide d’une table de montage séquentiel](how-to-animate-a-property-by-using-a-storyboard.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
