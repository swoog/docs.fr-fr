---
title: Métafichiers dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], metafiles
- GDI+, metafiles
- metafiles
ms.assetid: 51da872c-c783-440f-8bf6-1e580a966c31
ms.openlocfilehash: 25ce3fdd98560aba0918431bb77d6f3f23a04784
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57722462"
---
# <a name="metafiles-in-gdi"></a><span data-ttu-id="424b4-102">Métafichiers dans GDI+</span><span class="sxs-lookup"><span data-stu-id="424b4-102">Metafiles in GDI+</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="424b4-103">Fournit la <xref:System.Drawing.Imaging.Metafile> classe afin que vous pouvez enregistrer et afficher des métafichiers.</span><span class="sxs-lookup"><span data-stu-id="424b4-103">provides the <xref:System.Drawing.Imaging.Metafile> class so that you can record and display metafiles.</span></span> <span data-ttu-id="424b4-104">Un métafichier, également appelé image vectorielle, est une image qui est stockée comme une séquence de commandes et les paramètres de dessin.</span><span class="sxs-lookup"><span data-stu-id="424b4-104">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="424b4-105">Les commandes et les paramètres enregistrement dans un <xref:System.Drawing.Imaging.Metafile> objet peut être stocké en mémoire ou enregistré dans un fichier ou le flux.</span><span class="sxs-lookup"><span data-stu-id="424b4-105">The commands and settings recorded in a <xref:System.Drawing.Imaging.Metafile> object can be stored in memory or saved to a file or stream.</span></span>  
  
## <a name="metafile-formats"></a><span data-ttu-id="424b4-106">Formats de métafichier</span><span class="sxs-lookup"><span data-stu-id="424b4-106">Metafile Formats</span></span>  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="424b4-107">peut afficher des métafichiers qui ont été stockés dans les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="424b4-107">can display metafiles that have been stored in the following formats:</span></span>  
  
-   <span data-ttu-id="424b4-108">Métafichier Windows (WMF)</span><span class="sxs-lookup"><span data-stu-id="424b4-108">Windows Metafile (WMF)</span></span>  
  
-   <span data-ttu-id="424b4-109">métafichier amélioré (EMF)</span><span class="sxs-lookup"><span data-stu-id="424b4-109">Enhanced Metafile (EMF)</span></span>  
  
-   <span data-ttu-id="424b4-110">EMF+</span><span class="sxs-lookup"><span data-stu-id="424b4-110">EMF+</span></span>  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="424b4-111">peut enregistrer des métafichiers aux formats EMF et EMF +, mais pas dans le format WMF.</span><span class="sxs-lookup"><span data-stu-id="424b4-111">can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>  
  
 <span data-ttu-id="424b4-112">EMF + est une extension d’EMF qui permet [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] enregistrements doivent être stockés.</span><span class="sxs-lookup"><span data-stu-id="424b4-112">EMF+ is an extension to EMF that allows [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] records to be stored.</span></span> <span data-ttu-id="424b4-113">Il existe deux variantes du format EMF + : EMF + uniquement et double EMF +.</span><span class="sxs-lookup"><span data-stu-id="424b4-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="424b4-114">Métafichiers EMF + Only contiennent uniquement [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] enregistrements.</span><span class="sxs-lookup"><span data-stu-id="424b4-114">EMF+ Only metafiles contain only [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] records.</span></span> <span data-ttu-id="424b4-115">Ces métafichiers peuvent être affichés par [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] mais pas par [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)].</span><span class="sxs-lookup"><span data-stu-id="424b4-115">Such metafiles can be displayed by [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] but not by [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)].</span></span> <span data-ttu-id="424b4-116">Les métafichiers EMF + Dual contiennent [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] et [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] enregistrements.</span><span class="sxs-lookup"><span data-stu-id="424b4-116">EMF+ Dual metafiles contain [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] and [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] records.</span></span> <span data-ttu-id="424b4-117">Chaque [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] enregistrements dans une double EMF + métafichier est associée à un autre [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] enregistrement.</span><span class="sxs-lookup"><span data-stu-id="424b4-117">Each [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] record in an EMF+ Dual metafile is paired with an alternate [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] record.</span></span> <span data-ttu-id="424b4-118">Ces métafichiers peuvent être affichés par [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] ou par [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)].</span><span class="sxs-lookup"><span data-stu-id="424b4-118">Such metafiles can be displayed by [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] or by [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)].</span></span>  
  
 <span data-ttu-id="424b4-119">L’exemple suivant affiche un métafichier précédemment enregistré en tant que fichier.</span><span class="sxs-lookup"><span data-stu-id="424b4-119">The following example displays a metafile that was previously saved as a file.</span></span> <span data-ttu-id="424b4-120">Le métafichier est affiché avec son coin supérieur gauche à (100, 100).</span><span class="sxs-lookup"><span data-stu-id="424b4-120">The metafile is displayed with its upper-left corner at (100, 100).</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#21)]  
  
## <a name="see-also"></a><span data-ttu-id="424b4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="424b4-121">See also</span></span>
- [<span data-ttu-id="424b4-122">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="424b4-122">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
