---
title: 'Procédure : Utiliser des caractères spéciaux en XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- Unicode UTF-8 file format
- UTF-8 file format
- characters [WPF], special
- typography [WPF], special characters
- special characters [WPF]
ms.assetid: a57776d1-f353-4794-afa0-bfa3c712ed1c
ms.openlocfilehash: 18934e06f45ca4b88f48bce8a310a07b460a5f53
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57377961"
---
# <a name="how-to-use-special-characters-in-xaml"></a>Procédure : Utiliser des caractères spéciaux en XAML
Les fichiers de balisage qui sont créés dans [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)] sont automatiquement enregistrés dans le [!INCLUDE[TLA#tla_unicode](../../../../includes/tlasharptla-unicode-md.md)] format de fichier UTF-8, ce qui signifie que des caractères plus spéciaux, tels que les accents sont encodés correctement. Toutefois, il existe un ensemble de caractères spéciaux couramment utilisés qui sont gérés différemment. Ces caractères spéciaux respectent la [!INCLUDE[TLA#tla_w3c](../../../../includes/tlasharptla-w3c-md.md)] [!INCLUDE[TL A#tla_xml](../../../../includes/tlasharptla-xml-md.md)] standard pour l’encodage.  
  
 Le tableau suivant montre la syntaxe pour l’encodage de ce jeu de caractères spéciaux :  
  
|Caractère|Syntaxe|Description|  
|---------------|------------|-----------------|  
|<|`&lt;`|Signe Inférieur à.|  
|>|`&gt;`|Signe Supérieur à.|  
|&|`&amp;`|Symbole de Et commercial.|  
|"|`&quot;`|Symbole de guillemet double.|  
  
> [!NOTE]
>  Si vous créez un fichier de balisage à l’aide d’un texte éditeur de, tel que [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] le bloc-notes, vous devez enregistrer le fichier dans le [!INCLUDE[TLA#tla_unicode](../../../../includes/tlasharptla-unicode-md.md)] le format de fichier UTF-8 afin de préserver un caractères spéciaux encodés.  
  
 L’exemple suivant montre comment utiliser des caractères spéciaux dans du texte lors de la création du balisage.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[SpecialCharsSnippets#SpecialCharsSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/SpecialCharsSnippets/CS/Window1.xaml#specialcharssnippet1)]
