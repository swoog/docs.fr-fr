---
title: 'Procédure : effectuer une conversion entre les flux .NET Framework et les flux Windows Runtime (Windows uniquement)'
ms.date: 01/14/2019
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: 23a763ea-8348-4244-9f8c-a4280b870b47
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dc38e69a79af7c7220b8e3b55d4cb1f4ca3695f6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255196"
---
# <a name="how-to-convert-between-net-framework-and-windows-runtime-streams-windows-only"></a>Procédure : effectuer une conversion entre les flux .NET Framework et les flux Windows Runtime (Windows uniquement)

Le .NET Framework pour les applications UWP est un sous-ensemble du .NET Framework complet. En raison de la sécurité et d’autres spécifications des applications UWP, vous ne pouvez pas utiliser l’ensemble d’API .NET Framework pour ouvrir et lire des fichiers. Pour plus d’informations, consultez [Vue d’ensemble de .NET pour les applications UWP](https://docs.microsoft.com/previous-versions/windows/apps/br230302(v=vs.140)). Toutefois, vous pouvez utiliser des API .NET Framework pour les autres opérations de manipulation des flux. Pour manipuler ces flux, vous pouvez convertir un flux .NET Framework, tel que <xref:System.IO.MemoryStream> ou <xref:System.IO.FileStream>, en flux Windows Runtime tel que <xref:Windows.Storage.Streams.IInputStream>, <xref:Windows.Storage.Streams.IOutputStream> ou <xref:Windows.Storage.Streams.IRandomAccessStream>.

La classe [System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) contient des méthodes qui facilitent ces conversions. Toutefois, il existe des différences sous-jacentes entre les flux .NET Framework et Windows Runtime qui affecteront les résultats obtenus lors de l’utilisation de ces méthodes, comme l’expliquent les sections suivantes :

## <a name="convert-from-a-windows-runtime-to-a-net-framework-stream"></a>Convertir un flux Windows Runtime en flux .NET Framework
Pour convertir un flux Windows Runtime en flux .NET Framework, utilisez l’une des méthodes [System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) suivantes :

- [System.IO.WindowsRuntimeStreamExtensions.AsStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstream.aspx) convertit un flux d’accès aléatoire Windows Runtime en flux managé .NET pour applications UWP.
  
- [System.IO.WindowsRuntimeStreamExtensions.AsStreamForWrite](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforwrite.aspx) convertit un flux de sortie Windows Runtime en flux managé .NET pour applications UWP.
  
- [System.IO.WindowsRuntimeStreamExtensions.AsStreamForRead](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforread.aspx) convertit un flux d’entrée Windows Runtime en flux managé .NET pour applications UWP.

Windows Runtime propose des types de flux qui prennent en charge la lecture seule, l’écriture seule et la lecture-écriture. Ces fonctionnalités sont conservées lorsque vous convertissez un flux Windows Runtime en flux .NET Framework. En outre, si vous convertissez un flux Windows Runtime en un flux .NET Framework et inversement, vous obtenez l'instance du Windows Runtime en retour. 

Il est recommandé d’utiliser la méthode de conversion qui correspond aux fonctionnalités du flux Windows Runtime que vous souhaitez convertir. Toutefois, comme <xref:Windows.Storage.Streams.IRandomAccessStream> est accessible en lecture et en écriture (il implémente <xref:Windows.Storage.Streams.IOutputStream> et <xref:Windows.Storage.Streams.IInputStream>), les méthodes de conversion conservent les fonctionnalités du flux d’origine. Par exemple, l’utilisation de [System.IO.WindowsRuntimeStreamExtensions.AsStreamForRead](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforread.aspx) pour convertir <xref:Windows.Storage.Streams.IRandomAccessStream> n’empêche pas le flux .NET Framework converti d’être accessible en lecture. Il est également accessible en écriture.

## <a name="example-convert-windows-runtime-random-access-to-net-framework-stream"></a>Exemple : Convertir un flux d’accès aléatoire Windows Runtime en flux .NET Framework
Pour convertir un flux d’accès aléatoire Windows Runtime en flux .NET Framework, utilisez une méthode [System.IO.WindowsRuntimeStreamExtensions.AsStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstream.aspx).

L’exemple de code suivant vous invite à sélectionner un fichier, l’ouvre à l’aide des API Windows Runtime, puis le convertit en flux .NET Framework. Il lit le flux et l’exporte vers un bloc de texte. En général, vous devez manipuler le flux à l’aide des API .NET Framework avant de sortir les résultats.

Pour exécuter cet exemple, créez une application XAML UWP, contenant un bloc de texte nommé `TextBlock1` et un bouton nommé `Button1`. Associez l’événement de clic de bouton à la méthode `button1_Click` qui est illustrée dans l’exemple.

  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage1.xaml.cs)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage1.xaml.vb)]

## <a name="convert-from-a-net-framework-to-a-windows-runtime-stream"></a>Convertir un flux .NET Framework en flux Windows Runtime
Pour convertir un flux .NET Framework en flux Windows Runtime, utilisez l’une des méthodes [System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) suivantes :

- [System.IO.WindowsRuntimeStreamExtensions.AsInputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asinputstream.aspx) convertit un flux managé .NET pour applications UWP en flux d’entrée Windows Runtime.
  
- [System.IO.WindowsRuntimeStreamExtensions.AsOutputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asoutputstream.aspx) convertit un flux managé .NET pour applications UWP en un flux de sortie Windows Runtime.
  
- [AsRandomAccessStream](../../../docs/standard/cross-platform/windowsruntimestreamextensions-asrandomaccessstream-method.md) convertit un flux managé .NET pour applications UWP en flux d’accès aléatoire que Windows Runtime peut utiliser pour lire ou écrire des données.

Lorsque vous convertissez un flux .NET Framework en flux Windows Runtime, les fonctionnalités du flux converti dépendent de celles du flux d’origine. Par exemple, si le flux d’origine prend en charge la lecture et l’écriture, et que vous appelez [System.IO.WindowsRuntimeStreamExtensions.AsInputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asinputstream.aspx) pour convertir le flux, le type retourné est un `IRandomAccessStream`. `IRandomAccessStream` implémente `IInputStream` et `IOutputStream`, et prend en charge la lecture et l’écriture.

Les flux .NET Framework ne prennent pas en charge le clonage, même après la conversion. Si vous convertissez un flux .NET Framework en flux Windows Runtime, et appelez <xref:Windows.Storage.Streams.InMemoryRandomAccessStream.GetInputStreamAt%2A> ou <xref:Windows.Storage.Streams.IRandomAccessStream.GetOutputStreamAt%2A>, qui appelle <xref:Windows.Storage.Streams.RandomAccessStreamOverStream.CloneStream%2A>, ou si vous appelez <xref:Windows.Storage.Streams.RandomAccessStreamOverStream.CloneStream%2A> directement, une exception est levée.

## <a name="example-convert-net-framework-to-windows-runtime-random-access-stream"></a>Exemple : Convertir un flux .NET Framework en flux d’accès aléatoire Windows Runtime

Pour convertir un flux .NET Framework en flux d’accès aléatoire Windows Runtime, utilisez une méthode [AsRandomAccessStream](../../../docs/standard/cross-platform/windowsruntimestreamextensions-asrandomaccessstream-method.md), comme indiqué dans l’exemple suivant :

> [!IMPORTANT]
> Vérifiez que le flux du .NET Framework que vous utilisez prend en charge la recherche, ou copiez-le dans un flux qui la prend en charge. Vous pouvez utiliser la propriété <xref:System.IO.Stream.CanSeek%2A?displayProperty=nameWithType> pour le déterminer.

Pour exécuter cet exemple, créez une application XAML UWP qui cible .NET Framework 4.5.1 et contient un bloc de texte nommé `TextBlock2` et un bouton nommé `Button2`. Associez l’événement de clic de bouton à la méthode `button2_Click` qui est illustrée dans l’exemple.

  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage2.xaml.cs)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage2.xaml.vb)]

## <a name="see-also"></a>Voir aussi

- [Démarrage rapide : Lire et écrire des données dans un fichier (Windows)](https://msdn.microsoft.com/library/windows/apps/hh464978.aspx)  
- [Vue d’ensemble de .NET pour les applications Windows Store](https://msdn.microsoft.com/library/windows/apps/br230302.aspx)  
- [.NET pour les applications Windows Store : API prises en charge](https://msdn.microsoft.com/library/windows/apps/br230232.aspx)  
