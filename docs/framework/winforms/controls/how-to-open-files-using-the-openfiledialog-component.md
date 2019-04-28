---
title: 'Procédure : Ouvrir des fichiers avec le composant OpenFileDialog'
ms.date: 02/11/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- OpenFileDialog component [Windows Forms], opening files
- OpenFile method [Windows Forms], OpenFileDialog component
- files [Windows Forms], opening with OpenFileDialog component
ms.assetid: 9d88367a-cc21-4ffd-be74-89fd63767d35
ms.openlocfilehash: 7f4e96f1714a182647665f12e29d38f2b8037478
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913456"
---
# <a name="how-to-open-files-with-the-openfiledialog"></a>Procédure : Ouvrir des fichiers du composant OpenFileDialog 

Le <xref:System.Windows.Forms.OpenFileDialog?displayProperty=nameWithType> composant ouvre la boîte de dialogue Windows pour parcourir et sélectionner des fichiers. Pour ouvrir et lire les fichiers sélectionnés, vous pouvez utiliser la <xref:System.Windows.Forms.OpenFileDialog.OpenFile%2A?displayProperty=nameWithType> (méthode), ou créez une instance de la <xref:System.IO.StreamReader?displayProperty=nameWithType> classe. Les exemples suivants illustrent les deux approches. 

Dans .NET Framework, pour obtenir ou définir le <xref:System.Windows.Forms.FileDialog.FileName%2A> propriété nécessite un niveau de privilège accordé par la <xref:System.Security.Permissions.FileIOPermission?displayProperty=nameWithType> classe. Les exemples exécutent un <xref:System.Security.Permissions.FileIOPermission> autorisation vérifier et peut lever une exception en raison de privilèges insuffisants s’exécuter dans un contexte de confiance partielle. Pour plus d’informations, consultez [notions fondamentales du Code access security](../../misc/code-access-security-basics.md).

Vous pouvez générer et exécuter ces exemples en tant qu’applications .NET Framework à partir de la C# ou ligne de commande de Visual Basic. Pour plus d’informations, consultez [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md) ou [construire à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md). 

À compter de .NET Core 3.0, vous pouvez également générer et exécuter les exemples comme des applications .NET Core de Windows à partir d’un dossier qui a un .NET Core Windows Forms  *\<nom du dossier > .csproj* fichier projet. 

## <a name="example-read-a-file-as-a-stream-with-streamreader"></a>Exemple : Lire un fichier en tant que flux avec un StreamReader  
  
L’exemple suivant utilise les formulaires Windows <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour ouvrir le <xref:System.Windows.Forms.OpenFileDialog> avec la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode). Une fois que l’utilisateur choisit un fichier et sélectionne **OK**, une instance de la <xref:System.IO.StreamReader> classe lit le fichier et affiche son contenu dans la zone de texte du formulaire. Pour plus d’informations sur la lecture à partir de flux de fichier, consultez <xref:System.IO.FileStream.BeginRead%2A?displayProperty=nameWithType> et <xref:System.IO.FileStream.Read%2A?displayProperty=nameWithType>.  

 [!code-csharp[OpenFileDialog#1](~/samples/snippets/winforms/open-files/example1/cs/Form1.cs)]
 [!code-vb[OpenFileDialog#1](~/samples/snippets/winforms/open-files/example1/vb/Form1.vb)]  

## <a name="example-open-a-file-from-a-filtered-selection-with-openfile"></a>Exemple : Ouvrir un fichier à partir d’une sélection filtrée avec OpenFile 

L’exemple suivant utilise le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour ouvrir le <xref:System.Windows.Forms.OpenFileDialog> avec un filtre qui affiche uniquement les fichiers texte. Une fois que l’utilisateur choisit un fichier texte et sélectionne **OK**, le <xref:System.Windows.Forms.OpenFileDialog.OpenFile%2A> méthode est utilisée pour ouvrir le fichier dans le bloc-notes.

 [!code-csharp[OpenFileDialog#2](~/samples/snippets/winforms/open-files/example2/cs/Form1.cs)]
 [!code-vb[OpenFileDialog#2](~/samples/snippets/winforms/open-files/example2/vb/Form1.vb)]  

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.OpenFileDialog>
- [Composant OpenFileDialog](openfiledialog-component-windows-forms.md)
