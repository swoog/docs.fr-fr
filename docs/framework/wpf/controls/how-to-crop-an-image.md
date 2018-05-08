---
title: 'Comment : rogner une image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], cropping
- cropping images [WPF]
ms.assetid: c6bba109-c6e7-4cf8-bfe6-9cf8d01bb4fc
ms.openlocfilehash: 46c559356447688e52508b823cc260c13128208f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-crop-an-image"></a>Comment : rogner une image
Cet exemple montre comment rogner une image à l’aide de <xref:System.Windows.Media.Imaging.CroppedBitmap>.  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap> est principalement utilisé lors de l’encodage de version d’une image rognée à enregistrer dans un fichier. Pour rogner une image à des fins d’affichage, consultez la [créer une zone de découpage](http://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376) rubrique.  
  
## <a name="example"></a>Exemple  
 Les éléments suivants [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] définit les ressources utilisées dans les exemples ci-dessous.  
  
 [!code-xaml[imageelementexample#CroppedXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 L’exemple suivant crée une image en utilisant un <xref:System.Windows.Media.Imaging.CroppedBitmap> comme source.  
  
 [!code-xaml[imageelementexample#CroppedXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 Le <xref:System.Windows.Media.Imaging.CroppedBitmap> peut également être utilisé comme source d’un autre <xref:System.Windows.Media.Imaging.CroppedBitmap>, chaînage le rognage. Notez que le <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> utilise les valeurs par rapport à la bitmap source rogné et non pas l’image initiale.  
  
 [!code-xaml[imageelementexample#CroppedXAML3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a>Voir aussi  
 [Créer une zone de découpage](http://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376)
