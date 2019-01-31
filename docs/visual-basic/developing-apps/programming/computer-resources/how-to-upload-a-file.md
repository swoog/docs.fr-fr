---
title: 'Procédure : charger un fichier dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- networks, uploading files
- files [Visual Basic], uploading
- uploading files [Visual Basic]
- UploadFile method [Visual Basic]
- My.Computer.Network.UploadFile method
ms.assetid: a8b37924-c523-4fd3-b5ca-cb0074df29cd
ms.openlocfilehash: 0d0aaca06a72b9bd2631a652a0b4756f4681df7d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704405"
---
# <a name="how-to-upload-a-file-in-visual-basic"></a>Procédure : charger un fichier dans Visual Basic
Vous pouvez utiliser la méthode <xref:Microsoft.VisualBasic.Devices.Network.UploadFile%2A> pour charger un fichier et le stocker dans un emplacement distant. Si le paramètre `ShowUI` a la valeur `True`, une boîte de dialogue s’affiche pour indiquer la progression du chargement et permettre aux utilisateurs d’annuler l’opération.  
  
### <a name="to-upload-a-file"></a>Pour charger un fichier  
  
-   Utilisez la méthode `UploadFile` pour charger un fichier, en spécifiant l’emplacement du fichier source et l’emplacement du répertoire cible sous forme de chaîne ou d’URI (Uniform Resource Identifier). Cet exemple charge le fichier `Order.txt` sur `http://www.cohowinery.com/uploads.aspx`.  
  
     [!code-vb[VbResourceTasks#6](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-upload-a-file_1.vb)]  
  
### <a name="to-upload-a-file-and-show-the-progress-of-the-operation"></a>Pour charger un fichier et afficher la progression de l’opération  
  
-   Utilisez la méthode `UploadFile` pour charger un fichier, en spécifiant l’emplacement du fichier source et l’emplacement du répertoire cible sous forme de chaîne ou d’URI. Cet exemple charge le fichier `Order.txt` sur `http://www.cohowinery.com/uploads.aspx` sans fournir de nom d’utilisateur ou de mot de passe, affiche la progression du chargement, et présente un délai d’attente de 500 millisecondes.  
  
     [!code-vb[VbResourceTasks#7](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-upload-a-file_2.vb)]  
  
### <a name="to-upload-a-file-supplying-a-user-name-and-password"></a>Pour charger un fichier en fournissant un nom d’utilisateur et un mot de passe  
  
-   Utilisez la méthode `UploadFile` pour charger un fichier, en spécifiant l’emplacement du fichier source et l’emplacement du répertoire cible sous forme de chaîne ou d’URI, et en spécifiant le nom d’utilisateur et le mot de passe. Cet exemple charge le fichier `Order.txt` sur `http://www.cohowinery.com/uploads.aspx`, en fournissant le nom d’utilisateur `anonymous` et un mot de passe vide.  
  
     [!code-vb[VbResourceTasks#8](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-upload-a-file_3.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Les conditions suivantes peuvent lever une exception :  
  
-   Le chemin local n’est pas valide (<xref:System.ArgumentException>).  
  
-   L’authentification a échoué (<xref:System.Security.SecurityException>).  
  
-   La connexion a expiré (<xref:System.TimeoutException>).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Devices.Network?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Devices.Network.UploadFile%2A>
- [Guide pratique pour télécharger un fichier](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-download-a-file.md)
- [Guide pratique pour analyser des chemins](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
