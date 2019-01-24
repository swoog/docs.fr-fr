---
title: 'Procédure : Extraire l’icône associée à un fichier dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a file name and its file type icon in a ListView control [Windows Forms]
- file name extension icons [Windows Forms], displaying in a ListView
- extracting icons associated with a file type [Windows Forms]
ms.assetid: 88e2ad8b-c34f-415a-84f2-dad756b5c928
ms.openlocfilehash: f961345c4b9be43e73a8c7a11914cf82833a822f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559019"
---
# <a name="how-to-extract-the-icon-associated-with-a-file-in-windows-forms"></a><span data-ttu-id="8cf1b-102">Procédure : Extraire l’icône associée à un fichier dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8cf1b-102">How to: Extract the Icon Associated with a File in Windows Forms</span></span>
<span data-ttu-id="8cf1b-103">Grand nombre de fichiers ont des icônes incorporées qui fournissent une représentation visuelle du type de fichier associé.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-103">Many files have embedded icons that provide a visual representation of the associated file type.</span></span> <span data-ttu-id="8cf1b-104">Par exemple, documents Microsoft Word contiennent une icône qui les identifie comme documents Word.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-104">For example, Microsoft Word documents contain an icon that identifies them as Word documents.</span></span> <span data-ttu-id="8cf1b-105">Lors de l’affichage des fichiers dans un contrôle de table ou un contrôle de liste, vous souhaiterez afficher l’icône représentant le type de fichier en regard de chaque nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-105">When displaying files in a list control or table control, you may want to display the icon representing the file type next to each file name.</span></span> <span data-ttu-id="8cf1b-106">Faire cela facilement à l’aide de la <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="8cf1b-106">You can do this easily by using the <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8cf1b-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="8cf1b-107">Example</span></span>  
 <span data-ttu-id="8cf1b-108">L’exemple de code suivant montre comment extraire l’icône associée à un fichier et afficher le nom de fichier et son icône associée dans un <xref:System.Windows.Forms.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-108">The following code example demonstrates how to extract the icon associated with a file and display the file name and its associated icon in a <xref:System.Windows.Forms.ListView> control.</span></span>  
  
 [!code-csharp[System.Drawing.Icon.ExtractAssociatedIconEx#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Icon.ExtractAssociatedIconEx#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8cf1b-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="8cf1b-109">Compiling the Code</span></span>  
 <span data-ttu-id="8cf1b-110">Pour compiler l’exemple :</span><span class="sxs-lookup"><span data-stu-id="8cf1b-110">To compile the example:</span></span>  
  
-   <span data-ttu-id="8cf1b-111">Collez le code précédent dans un Windows Form et appelez le `ExtractAssociatedIconExample` méthode à partir du constructeur du formulaire ou <xref:System.Windows.Forms.Form.Load> méthode de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-111">Paste the preceding code into a Windows Form, and call the `ExtractAssociatedIconExample` method from the form's constructor or <xref:System.Windows.Forms.Form.Load> event-handling method.</span></span>  
  
     <span data-ttu-id="8cf1b-112">Vous devez vous assurer que votre formulaire importe le <xref:System.IO> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="8cf1b-112">You will need to make sure that your form imports the <xref:System.IO> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cf1b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cf1b-113">See also</span></span>
- [<span data-ttu-id="8cf1b-114">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="8cf1b-114">Images, Bitmaps, and Metafiles</span></span>](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="8cf1b-115">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="8cf1b-115">ListView Control</span></span>](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)
