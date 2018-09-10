---
title: 'Comment : effectuer une conversion entre les flux .NET Framework et les flux Windows Runtime'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: 23a763ea-8348-4244-9f8c-a4280b870b47
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b3cfaf4cf22bba445d774c653ff7797d535bcde2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398963"
---
# <a name="how-to-convert-between-net-framework-streams-and-windows-runtime-streams"></a>Comment : effectuer une conversion entre les flux .NET Framework et les flux Windows Runtime

Le .Net Framework pour les applications Windows Store est un sous-ensemble du .NET Framework complet. En raison de la sécurité et d'autres spécifications des applications Windows Store, vous ne pouvez pas utiliser l'ensemble d'API .NET Framework pour ouvrir et lire des fichiers. Pour plus d’informations, consultez [Vue d’ensemble de .NET pour les applications du Windows Store](https://docs.microsoft.com/previous-versions/windows/apps/br230302(v=vs.140)). Toutefois, vous pouvez utiliser des API .NET Framework pour les autres opérations de manipulation des flux. Pour manipuler ces flux, il peut s’avérer nécessaire d’effectuer une conversion entre un type de flux .NET Framework tel que <xref:System.IO.MemoryStream> ou <xref:System.IO.FileStream>, et un flux Windows Runtime tel que <xref:Windows.Storage.Streams.IInputStream>, <xref:Windows.Storage.Streams.IOutputStream> ou <xref:Windows.Storage.Streams.IRandomAccessStream>.

La classe [System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) contient des méthodes qui facilitent ces conversions. Toutefois, il existe des différences sous-jacentes entre les flux .NET Framework et Windows Runtime qui affecteront les résultats obtenus lors de l'utilisation ces méthodes. Ces différentes sont décrites en détail dans les sections suivantes.

## <a name="converting-from-a-windows-runtime-stream-to-a-net-framework-stream"></a>Conversion d'un flux Windows Runtime en un flux .NET Framework

Convertissez un flux Windows Runtime en un flux .NET Framework à l’aide de l’une des méthodes [System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) suivantes :

[System.IO.WindowsRuntimeStreamExtensions.AsStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstream.aspx)  
Convertit un flux d'accès aléatoire Windows Runtime en un flux managé du sous-ensemble .NET pour les applications du Windows Store.

[System.IO.WindowsRuntimeStreamExtensions.AsStreamForWrite](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforwrite.aspx)  
Convertit un flux de sortie Windows Runtime en un flux managé du sous-ensemble .NET pour les applications du Windows Store.

[System.IO.WindowsRuntimeStreamExtensions.AsStreamForRead](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforread.aspx)  
Convertit un flux d'entrée Windows Runtime en un flux managé du sous-ensemble .NET pour les applications du Windows Store.

Le Windows Runtime offre des types de flux qui prennent en charge la lecture seule, l'écriture seule ou la lecture et l'écriture. Ces capacités sont conservées lorsque vous convertissez un flux Windows Runtime en un flux .NET Framework. En outre, si vous convertissez un flux Windows Runtime en un flux .NET Framework et inversement, vous obtenez l'instance du Windows Runtime en retour. Il est recommandé d'utiliser la méthode de conversion correspondant aux capacités du flux Windows Runtime que vous souhaitez convertir. Toutefois, comme <xref:Windows.Storage.Streams.IRandomAccessStream> est accessible en lecture et en écriture (il implémente <xref:Windows.Storage.Streams.IOutputStream> et <xref:Windows.Storage.Streams.IInputStream>), vous pouvez utiliser n’importe quelle méthode de conversion. Par ailleurs, les capacités du flux d’origine sont conservées. Par exemple, l’utilisation de [System.IO.WindowsRuntimeStreamExtensions.AsStreamForRead](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforread.aspx) pour convertir <xref:Windows.Storage.Streams.IRandomAccessStream> n’empêche pas le flux .NET Framework converti d’être accessible en lecture seule. Il est également accessible en écriture.

### <a name="to-convert-from-a-windows-runtime-random-access-stream-to-a-net-framework-stream"></a>Pour convertir un flux d'accès aléatoire Windows Runtime en un flux .NET Framework

- Utilisez la méthode [System.IO.WindowsRuntimeStreamExtensions.AsStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstream.aspx).

  L'exemple de code suivant montre comment inviter l'utilisateur à sélectionner un fichier, l'ouvrir avec les API Windows Runtime, puis le convertir en un flux .NET Framework, qui est lu et envoyé vers un bloc de texte. Dans ce scénario, vous manipulez généralement le flux avec les API .NET Framework avant de sortir les résultats.

  Pour exécuter cet exemple, vous devez créer une application XAML Windows Store, contenant un bloc de texte nommé `TextBlock1` et un bouton nommé  `Button1`. L'événement Click du bouton doit être associé à la méthode `button1_Click` illustrée dans l'exemple.

  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#imports)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#imports)]
  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#1](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#1)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#1](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#1)]

## <a name="converting-from-a-net-framework-stream-to-a-windows-runtime-stream"></a>Conversion d'un flux .NET Framework en un flux Windows Runtime

Convertissez un flux .NET Framework en un flux Windows Runtime à l’aide de l’une des méthodes [System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) suivantes :

[System.IO.WindowsRuntimeStreamExtensions.AsInputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asinputstream.aspx) Convertit un flux managé du sous-ensemble .NET pour les applications du Windows Store en un flux d’entrée Windows Runtime.

[System.IO.WindowsRuntimeStreamExtensions.AsOutputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asoutputstream.aspx) Convertit un flux managé du sous-ensemble .NET pour les applications du Windows Store en un flux de sortie Windows Runtime.

[AsRandomAccessStream](../../../docs/standard/cross-platform/windowsruntimestreamextensions-asrandomaccessstream-method.md) Convertit un flux managé du sous-ensemble .NET pour les applications du Windows Store en un flux d’accès aléatoire qui peut être utilisé pour lire ou écrire dans Windows Runtime.

Lorsque vous convertissez un flux .NET Framework en un flux Windows Runtime, les capacités du flux converti dépendent du flux d'origine. Par exemple, si le flux d’origine prend en charge la lecture et l’écriture, et que vous appelez [System.IO.WindowsRuntimeStreamExtensions.AsInputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asinputstream.aspx) pour convertir le flux, le type retourné est un `IRandomAccessStream`qui implémente `IInputStream` et `IOutputStream`, et prend en charge la lecture et l’écriture.

Les flux .NET Framework ne prennent pas en charge le clonage, même après la conversion. Cela signifie que si vous convertissez un flux .NET Framework en flux Windows Runtime, et si vous appelez <xref:Windows.Storage.Streams.InMemoryRandomAccessStream.GetInputStreamAt%2A> ou <xref:Windows.Storage.Streams.IRandomAccessStream.GetOutputStreamAt%2A>, qui appelle <xref:Windows.Storage.Streams.RandomAccessStreamOverStream.CloneStream%2A> ou <xref:Windows.Storage.Streams.RandomAccessStreamOverStream.CloneStream%2A> directement, une exception est levée.

### <a name="to-convert-from-a-net-framework-stream-to-a-windows-runtime-random-access-stream"></a>Pour convertir un flux .NET Framework en un flux d'accès aléatoire Windows Runtime

- Utilisez la méthode [AsRandomAccessStream](../../../docs/standard/cross-platform/windowsruntimestreamextensions-asrandomaccessstream-method.md), comme illustré dans l’exemple suivant :

  > [!IMPORTANT]
  > Assurez-vous que le flux du .NET Framework que vous utilisez prend en charge la recherche, ou copiez-le dans un flux qui la prend en charge. Vous pouvez utiliser la propriété <xref:System.IO.Stream.CanSeek%2A?displayProperty=nameWithType> pour le déterminer.

  Pour exécuter cet exemple, vous devez créer une application XAML Windows Store qui cible le .NET Framework 4.5.1 et contient un bloc de texte nommé `TextBlock2` et un bouton nommé `Button2`. L'événement Click du bouton doit être associé à la méthode `button2_Click` illustrée dans cet exemple.

  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#imports)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#imports)]
  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#2](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#2)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#2](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#2)]

## <a name="see-also"></a>Voir aussi

[Démarrage rapide : lecture et écriture dans un fichier (Windows)](https://msdn.microsoft.com/library/windows/apps/hh464978.aspx)  
[Vue d’ensemble de .NET pour les applications Windows Store](https://msdn.microsoft.com/library/windows/apps/br230302.aspx)  
[.NET pour les applications du Windows Store : API prises en charge](https://msdn.microsoft.com/library/windows/apps/br230232.aspx)  