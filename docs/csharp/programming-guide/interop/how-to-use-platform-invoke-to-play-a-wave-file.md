---
title: "Procédure : Utiliser l'appel de code non managé pour lire un fichier audio - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- platform invoke, sound files
- interoperability [C#], playing WAV files using pinvoke
- wav files
- .wav files
ms.assetid: f7f62f53-e026-4c40-b221-3a26adb0c2c5
ms.openlocfilehash: 29c36bd0494879b66674cf3a3c404fdaf3908f59
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59323809"
---
# <a name="how-to-use-platform-invoke-to-play-a-wave-file-c-programming-guide"></a>Procédure : Utiliser l'appel de code non managé pour lire un fichier audio (Guide de programmation C#)
L’exemple de code C# suivant explique comment utiliser des services d’appel de code non managé pour lire un fichier audio sur le système d’exploitation Windows.  
  
## <a name="example"></a>Exemple  
 Cet exemple de code utilise `DllImport` pour importer le point d’entrée de la méthode `PlaySound` de `winmm.dll` sous la forme `Form1 PlaySound()`. L’exemple utilise un formulaire Windows Form simple avec un bouton. En cliquant sur le bouton, vous ouvrez une boîte de dialogue <xref:System.Windows.Forms.OpenFileDialog> Windows standard qui permet d’ouvrir un fichier à lire. Quand un fichier audio est sélectionné, il est lu à l’aide de la méthode `PlaySound()` de la bibliothèque `winmm.dll`. Pour plus d’informations sur cette méthode, consultez [Utilisation de la fonction PlaySound avec des fichiers audio Waveform](https://docs.microsoft.com/windows/desktop/multimedia/using-playsound-to-play-waveform-audio-files). Recherchez et sélectionnez un fichier avec une extension .wav, puis cliquez sur **Ouvrir** pour lire le fichier audio à l’aide de l’appel de code non managé. Une zone de texte affiche le chemin complet du fichier sélectionné.  
  
 La boîte de dialogue **Ouvrir les fichiers** est filtrée pour afficher uniquement les fichiers avec une extension .wav au moyen des paramètres de filtre :  
  
 [!code-csharp[csProgGuideInterop#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInterop/CS/WinSound.cs#5)]  
  
 [!code-csharp[csProgGuideInterop#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInterop/CS/WinSound.cs#3)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
  
### <a name="to-compile-the-code"></a>Pour compiler le code  
  
1. Créez un projet d’application Windows C# dans Visual Studio et nommez-le **WinSound**.  
  
2. Copiez le code ci-dessus et collez-le sur le contenu du fichier `Form1.cs`.  
  
3. Copiez le code suivant et collez-le dans le fichier `Form1.Designer.cs`, dans la méthode `InitializeComponent()`, après tout le code existant.  
  
     [!code-csharp[csProgGuideInterop#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInterop/CS/WinSound.cs#4)]  
  
4. Compilez, puis exécutez le code.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Pour plus d’informations, consultez [Sécurité dans .NET](../../../standard/security/index.md).  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Vue d’ensemble de l’interopérabilité](../../../csharp/programming-guide/interop/interoperability-overview.md)
- [Présentation détaillée de l’appel de code non managé](../../../framework/interop/consuming-unmanaged-dll-functions.md#a-closer-look-at-platform-invoke)
- [Marshaling de données à l’aide de l’appel de code managé](../../../framework/interop/marshaling-data-with-platform-invoke.md)
