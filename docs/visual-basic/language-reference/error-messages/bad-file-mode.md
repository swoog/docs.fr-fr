---
title: Mode de fichier incorrect
ms.date: 07/20/2015
f1_keywords:
- vbrID54
ms.assetid: 74891e96-884b-4c8d-872d-cd11ae272372
ms.openlocfilehash: d3d0ebd003f178567ec9e9b19d6baccb8bc15f60
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819981"
---
# <a name="bad-file-mode"></a><span data-ttu-id="07578-102">Mode de fichier incorrect</span><span class="sxs-lookup"><span data-stu-id="07578-102">Bad file mode</span></span>
<span data-ttu-id="07578-103">Les instructions utilisées pour la manipulation du contenu du fichier doivent être adaptées à la mode dans lequel le fichier a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="07578-103">Statements used in manipulating file contents must be appropriate to the mode in which the file was opened.</span></span> <span data-ttu-id="07578-104">Plusieurs causes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="07578-104">Possible causes include:</span></span>  
  
-   <span data-ttu-id="07578-105">Un `FilePutObject` ou `FileGetObject` instruction spécifie un fichier séquentiel.</span><span class="sxs-lookup"><span data-stu-id="07578-105">A `FilePutObject` or `FileGetObject` statement specifies a sequential file.</span></span>  
  
-   <span data-ttu-id="07578-106">Un `Print` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Output` ou `Append`.</span><span class="sxs-lookup"><span data-stu-id="07578-106">A `Print` statement specifies a file opened for an access mode other than `Output` or `Append`.</span></span>  
  
-   <span data-ttu-id="07578-107">Un `Input` instruction spécifie un fichier ouvert pour un mode d’accès autre que `Input`</span><span class="sxs-lookup"><span data-stu-id="07578-107">An `Input` statement specifies a file opened for an access mode other than `Input`</span></span>  
  
-   <span data-ttu-id="07578-108">Une tentative d’écriture dans un fichier en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="07578-108">An attempt to write to a read-only file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="07578-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="07578-109">To correct this error</span></span>  
  
-   <span data-ttu-id="07578-110">Assurez-vous que `FilePutObject` et `FileGetObject` font uniquement référence à des fichiers ouverts pour `Random` ou `Binary` accès.</span><span class="sxs-lookup"><span data-stu-id="07578-110">Make sure `FilePutObject` and `FileGetObject` are only referring to files open for `Random` or `Binary` access.</span></span>  
  
-   <span data-ttu-id="07578-111">Assurez-vous que `Print` spécifie un fichier ouvert pour un `Output` ou `Append` mode d’accès.</span><span class="sxs-lookup"><span data-stu-id="07578-111">Make sure `Print` specifies a file opened for either `Output` or `Append` access mode.</span></span> <span data-ttu-id="07578-112">Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.</span><span class="sxs-lookup"><span data-stu-id="07578-112">If not, use a different statement to place data in the file, or reopen the file in an appropriate mode.</span></span>  
  
-   <span data-ttu-id="07578-113">Assurez-vous que `Input` spécifie un fichier ouvert pour `Input`.</span><span class="sxs-lookup"><span data-stu-id="07578-113">Make sure `Input` specifies a file opened for `Input`.</span></span> <span data-ttu-id="07578-114">Si ce n’est pas le cas, utilisez une instruction différente pour placer des données dans le fichier ou rouvrez le fichier dans un mode approprié.</span><span class="sxs-lookup"><span data-stu-id="07578-114">If not, use a different statement to place data in the file or reopen the file in an appropriate mode.</span></span>  
  
-   <span data-ttu-id="07578-115">Si vous écrivez dans un fichier en lecture seule, modifier l’état de lecture/écriture du fichier ou n’essayez pas d’y écrire.</span><span class="sxs-lookup"><span data-stu-id="07578-115">If you are writing to a read-only file, change the read/write status of the file or do not try to write to it.</span></span>  
  
-   <span data-ttu-id="07578-116">Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .</span><span class="sxs-lookup"><span data-stu-id="07578-116">Use the functionality available in the `My.Computer.FileSystem` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07578-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07578-117">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem>
- [<span data-ttu-id="07578-118">Résolution des problèmes : lecture et écriture dans des fichiers texte</span><span class="sxs-lookup"><span data-stu-id="07578-118">Troubleshooting: Reading from and Writing to Text Files</span></span>](../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
