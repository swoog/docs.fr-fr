---
title: "Procédure : Remplacer l'arborescence logique"
ms.date: 03/30/2017
helpviewer_keywords:
- overriding the logical tree [WPF]
- logical tree [WPF], overriding
ms.assetid: 0ae4d074-8113-4b06-b4fa-e0f39d4967a6
ms.openlocfilehash: bf3459fff1a90326794d6713dd39c73596b0e960
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57375212"
---
# <a name="how-to-override-the-logical-tree"></a>Procédure : Remplacer l'arborescence logique
Bien que cela ne soit pas nécessaire dans la plupart des cas, les auteurs de contrôles avancés ont la possibilité de remplacer l’arborescence logique.  
  
## <a name="example"></a>Exemple  
 Cet exemple décrit comment créer une sous-classe <xref:System.Windows.Controls.StackPanel> pour remplacer l’arborescence logique, dans ce cas pour appliquer un comportement que le panneau peut avoir et effectue le rendu uniquement un seul élément enfant. Ce n’est pas nécessairement un comportement souhaitable, mais il est indiqué ici afin d’illustrer le scénario permettant de remplacer l’arborescence logique normale d’un élément.  
  
 [!code-csharp[LogicalOverride#SingletonPanel](~/samples/snippets/csharp/VS_Snippets_Wpf/LogicalOverride/CSharp/SDKSampleLibrary/class1.cs#singletonpanel)]  
  
 Pour plus d’informations sur l’arborescence logique, consultez [Arborescences dans WPF](trees-in-wpf.md).
