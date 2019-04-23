---
title: 'Procédure : enregistrer des fichiers avec le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- saving files
- RTF files [Windows Forms], saving in RichTextBox control
- examples [Windows Forms], text boxes
- saving files [Windows Forms], RichTextBox control
- files [Windows Forms], saving with RichTextBox control
- RichTextBox control [Windows Forms], saving files
- .rtf files [Windows Forms], saving in RichTextBox control
- text files [Windows Forms], saving from RichTextBox control
ms.assetid: 4a58ec19-84d1-4383-9110-298c06adcfca
ms.openlocfilehash: 4784ddd563ccec0f7e6271700781ee1b5d3ac105
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59318414"
---
# <a name="how-to-save-files-with-the-windows-forms-richtextbox-control"></a>Procédure : enregistrer des fichiers avec le contrôle RichTextBox Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle peut écrire les informations affichées dans un des formats suivants :  
  
-   Texte brut  
  
-   Texte brut Unicode  
  
-   Format de texte enrichi (RTF)  
  
-   RTF avec des espaces à la place des objets OLE  
  
-   Texte brut avec une représentation textuelle des objets OLE  
  
 Pour enregistrer un fichier, appelez le <xref:System.Windows.Forms.RichTextBox.SaveFile%2A> (méthode). Vous pouvez également utiliser le **SaveFile** méthode pour enregistrer les données dans un flux. Pour plus d'informations, consultez <xref:System.Windows.Forms.RichTextBox.SaveFile%28System.IO.Stream%2CSystem.Windows.Forms.RichTextBoxStreamType%29>.  
  
### <a name="to-save-the-contents-of-the-control-to-a-file"></a>Pour enregistrer le contenu du contrôle dans un fichier  
  
1. Déterminer le chemin d’accès du fichier à enregistrer.  
  
     Pour ce faire, dans une application réelle, vous utiliseriez généralement le <xref:System.Windows.Forms.SaveFileDialog> composant. Pour une vue d’ensemble, consultez [vue d’ensemble du composant SaveFileDialog](savefiledialog-component-overview-windows-forms.md).  
  
2. Appelez le <xref:System.Windows.Forms.RichTextBox.SaveFile%2A> méthode de la <xref:System.Windows.Forms.RichTextBox> contrôle, en spécifiant le fichier à enregistrer et éventuellement un type de fichier. Si vous appelez la méthode avec un nom de fichier comme seul argument, le fichier sera enregistré au format RTF. Pour spécifier un autre type de fichier, appelez la méthode en spécifiant une valeur pour l’énumération <xref:System.Windows.Forms.RichTextBoxStreamType> comme deuxième argument.  
  
     Dans l’exemple ci-dessous, le chemin d’accès défini pour l’emplacement du fichier de texte enrichi est la **Mes Documents** dossier. Cet emplacement est utilisé, car vous pouvez supposer que la plupart des ordinateurs exécutant le système d’exploitation Windows incluent ce dossier. Choix de cet emplacement permet également aux utilisateurs avec des niveaux d’accès système minimal exécuter en toute sécurité de l’application. L’exemple suivant suppose un formulaire avec un <xref:System.Windows.Forms.RichTextBox> contrôle déjà ajouté.  
  
    ```vb  
    Public Sub SaveFile()  
       ' You should replace the bold file name in the   
       ' sample below with a file name of your own choosing.  
       RichTextBox1.SaveFile(System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\Testdoc.rtf", _  
          RichTextBoxStreamType.RichNoOleObjs)  
    End Sub  
    ```  
  
    ```csharp  
    public void SaveFile()  
    {  
       // You should replace the bold file name in the   
       // sample below with a file name of your own choosing.  
       // Note the escape character used (@) when specifying the path.  
       richTextBox1.SaveFile(System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.Personal)  
       + @"\Testdoc.rtf",  
          RichTextBoxStreamType.RichNoOleObjs);  
    }  
    ```  
  
    ```cpp  
    public:  
       void SaveFile()  
       {  
          // You should replace the bold file name in the   
          // sample below with a file name of your own choosing.  
          richTextBox1->SaveFile(String::Concat  
             (System::Environment::GetFolderPath  
             (System::Environment::SpecialFolder::Personal),  
             "\\Testdoc.rtf"), RichTextBoxStreamType::RichNoOleObjs);  
       }  
    ```  
  
    > [!IMPORTANT]
    >  Cet exemple crée un fichier s’il n’existe pas déjà. Si une application a besoin créer un fichier, cette application a besoin d’accéder de créer pour le dossier. Les autorisations sont définies à l’aide des listes de contrôle d’accès. Si le fichier existe déjà, l’application doit uniquement un accès en écriture, un privilège inférieur. Si possible, il est plus sûr de créer le fichier pendant le déploiement et uniquement accorder l’accès en lecture à un seul fichier, au lieu de créer l’accès pour un dossier. En outre, il est plus sûr d’écrire les données dans des dossiers utilisateur que dans le dossier racine ou le dossier Program Files.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RichTextBox.SaveFile%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
