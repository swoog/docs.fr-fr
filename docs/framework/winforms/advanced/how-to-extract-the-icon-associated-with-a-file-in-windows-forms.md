---
title: 'Procédure : extraire l’icône associée à un fichier dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a file name and its file type icon in a ListView control [Windows Forms]
- file name extension icons [Windows Forms], displaying in a ListView
- extracting icons associated with a file type [Windows Forms]
ms.assetid: 88e2ad8b-c34f-415a-84f2-dad756b5c928
ms.openlocfilehash: d754dc5e8a57b3c4e2e5439bb2524a22d44813c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59112552"
---
# <a name="how-to-extract-the-icon-associated-with-a-file-in-windows-forms"></a>Procédure : extraire l’icône associée à un fichier dans Windows Forms
Grand nombre de fichiers ont des icônes incorporées qui fournissent une représentation visuelle du type de fichier associé. Par exemple, documents Microsoft Word contiennent une icône qui les identifie comme documents Word. Lors de l’affichage des fichiers dans un contrôle de table ou un contrôle de liste, vous souhaiterez afficher l’icône représentant le type de fichier en regard de chaque nom de fichier. Faire cela facilement à l’aide de la <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> (méthode).  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment extraire l’icône associée à un fichier et afficher le nom de fichier et son icône associée dans un <xref:System.Windows.Forms.ListView> contrôle.  
  
 [!code-csharp[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Pour compiler l’exemple :  
  
-   Collez le code précédent dans un Windows Form et appelez le `ExtractAssociatedIconExample` méthode à partir du constructeur du formulaire ou <xref:System.Windows.Forms.Form.Load> méthode de gestion des événements.  
  
     Vous devez vous assurer que votre formulaire importe le <xref:System.IO> espace de noms.  
  
## <a name="see-also"></a>Voir aussi

- [Images, bitmaps et métafichiers](images-bitmaps-and-metafiles.md)
- [Contrôle ListView](../controls/listview-control-windows-forms.md)
