---
title: 'Procédure : Charger un son de façon asynchrone dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SoundPlayer class [Windows Forms], loading sounds asynchronously
- sounds [Windows Forms], loading on separate threads
- threading [Windows Forms], sounds
ms.assetid: 3b6a9296-1d5e-4d52-a4ba-94366d6fe302
ms.openlocfilehash: 8240e26ea0133aa091354d29f52d0692499d7765
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718296"
---
# <a name="how-to-load-a-sound-asynchronously-within-a-windows-form"></a>Procédure : Charger un son de façon asynchrone dans un formulaire Windows
L'exemple de code suivant charge un son de façon asynchrone à partir d'une URL et le lit sur un nouveau thread.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Media.SoundPlayer.LoadAsync#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.LoadAsync#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   des références aux assemblys System et System.Windows.Forms ;  
  
-   que vous remplaciez le nom de fichier `"http://www.tailspintoys.com/sounds/stop.wav"` par un nom de fichier valide.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les opérations de fichiers doivent être placées dans des blocs de gestion des exceptions appropriés.  
  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Le chemin d'accès est mal formé. Par exemple, il contient des caractères qui ne sont pas valides ou est constitué uniquement d'espaces blancs (classe <xref:System.ArgumentException>).  
  
-   Le chemin d'accès est en lecture seule (classe <xref:System.IO.IOException>).  
  
-   Le nom du chemin d'accès est `Nothing` (classe <xref:System.ArgumentNullException>).  
  
-   Le nom de chemin d'accès est trop long (classe <xref:System.IO.PathTooLongException>).  
  
-   Le chemin d'accès n'est pas valide (classe <xref:System.IO.DirectoryNotFoundException>).  
  
-   Le chemin d’accès n’est constitué que d’un signe deux-points « : » (classe <xref:System.NotSupportedException>).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Ne vous basez pas sur le nom d'un fichier pour en déterminer le contenu. Par exemple, le fichier `Form1.vb` peut ne pas être un fichier source Visual Basic. Vérifiez toutes les entrées avant d'utiliser les données dans votre application.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Media.SoundPlayer.LoadAsync%2A>
- <xref:System.Media.SoundPlayer.LoadCompleted>
- <xref:System.Media.SoundPlayer.Play%2A>
- [Guide pratique pour Un signal sonore à partir d’un formulaire Windows](how-to-play-a-sound-from-a-windows-form.md)
