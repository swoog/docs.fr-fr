---
title: 'Procédure : choisir des dossiers avec le composant FolderBrowserDialog Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- directories [Windows Forms], choosing
- FolderBrowserDialog component [Windows Forms], choosing directories
- folders [Windows Forms], selecting
- folders [Windows Forms], choosing
- directories [Windows Forms], selecting
ms.assetid: 4593670e-7c7d-4661-b46b-4ffb63258adb
ms.openlocfilehash: 2bff105d5c97a8b98d094a1ce3a4f033aa5971be
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59116075"
---
# <a name="how-to-choose-folders-with-the-windows-forms-folderbrowserdialog-component"></a>Procédure : choisir des dossiers avec le composant FolderBrowserDialog Windows Forms
Souvent, dans les applications Windows que vous créez, vous devez demander aux utilisateurs de sélectionner un dossier, le plus souvent pour enregistrer un ensemble de fichiers. Les formulaires Windows <xref:System.Windows.Forms.FolderBrowserDialog> composant vous permet d’effectuer rapidement cette tâche.  
  
### <a name="to-choose-folders-with-the-folderbrowserdialog-component"></a>Pour sélectionner des dossiers avec le composant FolderBrowserDialog  
  
1.  Dans une procédure, vérifiez le <xref:System.Windows.Forms.FolderBrowserDialog> du composant <xref:System.Windows.Forms.Form.DialogResult%2A> propriété pour déterminer comment la boîte de dialogue a été fermée et obtenir la valeur de la <xref:System.Windows.Forms.FolderBrowserDialog> du composant <xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> propriété.  
  
2.  Si vous avez besoin au dossier de l’ensemble le plus élevé qui s’affichent dans l’arborescence de la boîte de dialogue, définissez la <xref:System.Windows.Forms.FolderBrowserDialog.RootFolder%2A> propriété, qui utilise un membre de la <xref:System.Environment.SpecialFolder> énumération.  
  
3.  En outre, vous pouvez définir le <xref:System.Windows.Forms.FolderBrowserDialog.Description%2A> propriété qui spécifie la chaîne de texte qui apparaît en haut de l’arborescence de l’Explorateur de dossiers.  
  
     Dans l’exemple ci-dessous, le <xref:System.Windows.Forms.FolderBrowserDialog> composant est utilisé pour sélectionner un dossier, similaire à lorsque vous créez un projet dans Visual Studio et que vous êtes invité à sélectionner un dossier pour l’enregistrer. Dans cet exemple, le nom du dossier est ensuite affiché dans un <xref:System.Windows.Forms.TextBox> contrôle sur le formulaire. Il est judicieux de placer l’emplacement dans une zone modifiable, comme un <xref:System.Windows.Forms.TextBox> contrôler, afin que les utilisateurs puissent modifier leur sélection en cas d’erreur ou d’autres problèmes. Cet exemple suppose un formulaire avec un <xref:System.Windows.Forms.FolderBrowserDialog> composant et un <xref:System.Windows.Forms.TextBox> contrôle.  
  
    ```vb  
    Public Sub ChooseFolder()  
        If FolderBrowserDialog1.ShowDialog() = DialogResult.OK Then  
            TextBox1.Text = FolderBrowserDialog1.SelectedPath  
        End If  
    End Sub  
    ```  
  
    ```csharp  
    public void ChooseFolder()  
    {  
        if (folderBrowserDialog1.ShowDialog() == DialogResult.OK)   
        {  
            textBox1.Text = folderBrowserDialog1.SelectedPath;  
        }  
    }  
    ```  
  
    ```cpp  
    public:  
       void ChooseFolder()  
       {  
          if (folderBrowserDialog1->ShowDialog() == DialogResult::OK)  
          {  
             textBox1->Text = folderBrowserDialog1->SelectedPath;  
          }  
       }  
    ```  
  
    > [!IMPORTANT]
    >  Pour utiliser cette classe, votre assembly nécessite un niveau de privilège accordé par la <xref:System.Security.Permissions.FileIOPermissionAttribute.PathDiscovery%2A> propriété, qui fait partie de la <xref:System.Security.Permissions.FileIOPermissionAccess> énumération. Si vous l’exécutez dans un contexte de confiance partielle, le processus peut lever une exception en raison de privilèges insuffisants. Pour plus d’informations, consultez [Notions fondamentales de la sécurité d’accès du code](../../misc/code-access-security-basics.md).  
  
 Pour plus d’informations sur la façon d’enregistrer des fichiers, consultez [Comment : Enregistrer des fichiers à l’aide du composant SaveFileDialog](how-to-save-files-using-the-savefiledialog-component.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.FolderBrowserDialog>
- [Vue d’ensemble du composant FolderBrowserDialog (Windows Forms)](folderbrowserdialog-component-overview-windows-forms.md)
- [FolderBrowserDialog, composant](folderbrowserdialog-component-windows-forms.md)
