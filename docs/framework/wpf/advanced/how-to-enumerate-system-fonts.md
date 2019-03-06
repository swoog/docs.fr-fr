---
title: 'Procédure : Énumérer des polices système'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], enumerating system fonts
- fonts [WPF], enumerating
- system fonts [WPF], enumerating
- enumerating [WPF], system fonts
ms.assetid: 36e37791-55b9-4f01-a496-5cc10335e6a6
ms.openlocfilehash: c7e81b5d1b70ba911a0b505219f7977e019038cf
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352436"
---
# <a name="how-to-enumerate-system-fonts"></a>Procédure : Énumérer des polices système
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment énumérer les polices dans la collection de polices système. Le nom de famille de polices de chaque <xref:System.Windows.Media.FontFamily> dans <xref:System.Windows.Media.Fonts.SystemFontFamilies%2A> est ajouté en tant qu’élément à une zone de liste déroulante.  
  
 [!code-csharp[TextOverview#100](~/samples/snippets/csharp/VS_Snippets_Wpf/TextOverview/CSharp/Window1.xaml.cs#100)]
 [!code-vb[TextOverview#100](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextOverview/visualbasic/window1.xaml.vb#100)]  
  
 Si plusieurs versions de la même famille de polices résident dans le même répertoire, le [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] énumération de police retourne la version la plus récente de la police. Si les informations de version ne fournissent pas de résolution, la police avec l’horodateur le plus récent est retournée. Si les informations d’horodatage sont équivalentes, le fichier de police qui apparaît en premier dans l’ordre alphabétique est retourné.
