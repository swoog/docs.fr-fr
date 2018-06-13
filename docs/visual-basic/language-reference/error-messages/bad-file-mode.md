---
title: Mode de fichier incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID54
ms.assetid: 74891e96-884b-4c8d-872d-cd11ae272372
ms.openlocfilehash: bccbbbeb79f38790a4664b0152ca3378fb55448d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587382"
---
# <a name="bad-file-mode"></a><span data-ttu-id="2e788-102">Mode de fichier incorrect</span><span class="sxs-lookup"><span data-stu-id="2e788-102">Bad file mode</span></span>
<span data-ttu-id="2e788-103">Les instructions utilisées pour la manipulation du contenu du fichier doivent être adaptées au mode dans lequel le fichier a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="2e788-103">Statements used in manipulating file contents must be appropriate to the mode in which the file was opened.</span></span> <span data-ttu-id="2e788-104">Plusieurs causes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="2e788-104">Possible causes include:</span></span>  
  
-   <span data-ttu-id="2e788-105">A `FilePutObject` ou `FileGetObject` instruction spécifie un fichier séquentiel.</span><span class="sxs-lookup"><span data-stu-id="2e788-105">A `FilePutObject` or `FileGetObject` statement specifies a sequential file.</span></span>  
  
-   <span data-ttu-id="2e788-106">A `Print` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Output` ou `Append`.</span><span class="sxs-lookup"><span data-stu-id="2e788-106">A `Print` statement specifies a file opened for an access mode other than `Output` or `Append`.</span></span>  
  
-   <span data-ttu-id="2e788-107">Un `Input` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Input`</span><span class="sxs-lookup"><span data-stu-id="2e788-107">An `Input` statement specifies a file opened for an access mode other than `Input`</span></span>  
  
-   <span data-ttu-id="2e788-108">Toute tentative d’écriture dans un fichier en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2e788-108">An attempt to write to a read-only file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2e788-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="2e788-109">To correct this error</span></span>  
  
-   <span data-ttu-id="2e788-110">Assurez-vous que `FilePutObject` et `FileGetObject` font uniquement référence à des fichiers ouverts pour `Random` ou `Binary` accès.</span><span class="sxs-lookup"><span data-stu-id="2e788-110">Make sure `FilePutObject` and `FileGetObject` are only referring to files open for `Random` or `Binary` access.</span></span>  
  
-   <span data-ttu-id="2e788-111">Assurez-vous que `Print` spécifie un fichier ouvert pour un `Output` ou `Append` mode d’accès.</span><span class="sxs-lookup"><span data-stu-id="2e788-111">Make sure `Print` specifies a file opened for either `Output` or `Append` access mode.</span></span> <span data-ttu-id="2e788-112">Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.</span><span class="sxs-lookup"><span data-stu-id="2e788-112">If not, use a different statement to place data in the file, or reopen the file in an appropriate mode.</span></span>  
  
-   <span data-ttu-id="2e788-113">Assurez-vous que `Input` spécifie un fichier ouvert pour `Input`.</span><span class="sxs-lookup"><span data-stu-id="2e788-113">Make sure `Input` specifies a file opened for `Input`.</span></span> <span data-ttu-id="2e788-114">Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.</span><span class="sxs-lookup"><span data-stu-id="2e788-114">If not, use a different statement to place data in the file or reopen the file in an appropriate mode.</span></span>  
  
-   <span data-ttu-id="2e788-115">Si vous écrivez dans un fichier en lecture seule, de modifier l’état de lecture/écriture du fichier ou n’essayez pas d’écrire dedans.</span><span class="sxs-lookup"><span data-stu-id="2e788-115">If you are writing to a read-only file, change the read/write status of the file or do not try to write to it.</span></span>  
  
-   <span data-ttu-id="2e788-116">Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .</span><span class="sxs-lookup"><span data-stu-id="2e788-116">Use the functionality available in the `My.Computer.FileSystem` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e788-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e788-117">See Also</span></span>  
 <xref:Microsoft.VisualBasic.FileSystem>  
 [<span data-ttu-id="2e788-118">Dépannage : lecture et écriture dans des fichiers texte</span><span class="sxs-lookup"><span data-stu-id="2e788-118">Troubleshooting: Reading from and Writing to Text Files</span></span>](../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
