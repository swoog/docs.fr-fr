---
title: Erreur de chargement de la DLL (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID48
ms.assetid: 4226cd1f-028c-477d-88a5-cb57f7e0cdc8
ms.openlocfilehash: 5a26443a49b0b853f2f2188fb58d7ed907d671b4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64659617"
---
# <a name="error-in-loading-dll-visual-basic"></a><span data-ttu-id="e190e-102">Erreur de chargement de la DLL (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e190e-102">Error in loading DLL (Visual Basic)</span></span>
<span data-ttu-id="e190e-103">Une bibliothèque de liens dynamiques (DLL) est une bibliothèque spécifiée dans le `Lib` clause d’une `Declare` instruction.</span><span class="sxs-lookup"><span data-stu-id="e190e-103">A dynamic-link library (DLL) is a library specified in the `Lib` clause of a `Declare` statement.</span></span> <span data-ttu-id="e190e-104">Les causes possibles de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="e190e-104">Possible causes for this error include:</span></span>  
  
- <span data-ttu-id="e190e-105">Le fichier n’est pas exécutable DLL.</span><span class="sxs-lookup"><span data-stu-id="e190e-105">The file is not DLL executable.</span></span>  
  
- <span data-ttu-id="e190e-106">Le fichier n’est pas une DLL de Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e190e-106">The file is not a Microsoft Windows DLL.</span></span>  
  
- <span data-ttu-id="e190e-107">La DLL fait référence à une autre DLL qui n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="e190e-107">The DLL references another DLL that is not present.</span></span>  
  
- <span data-ttu-id="e190e-108">La DLL ou la DLL référencée n’est pas un répertoire spécifié dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e190e-108">The DLL or referenced DLL is not in a directory specified in the path.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e190e-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="e190e-109">To correct this error</span></span>  
  
- <span data-ttu-id="e190e-110">Si le fichier est un fichier texte source et par conséquent pas un exécutable DLL, il doit être compilé et lié à un formulaire exécutable DLL.</span><span class="sxs-lookup"><span data-stu-id="e190e-110">If the file is a source-text file and therefore not DLL executable, it must be compiled and linked to a DLL-executable form.</span></span>  
  
- <span data-ttu-id="e190e-111">Si le fichier n’est pas une DLL de Windows de Microsoft, obtenir l’équivalent Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e190e-111">If the file is not a Microsoft Windows DLL, obtain the Microsoft Windows equivalent.</span></span>  
  
- <span data-ttu-id="e190e-112">Si la DLL fait référence à une autre DLL qui n’est pas présente, obtenir la DLL référencée et le rendre disponible.</span><span class="sxs-lookup"><span data-stu-id="e190e-112">If the DLL references another DLL that is not present, obtain the referenced DLL and make it available.</span></span>  
  
- <span data-ttu-id="e190e-113">Si la DLL ou la DLL référencée n’est pas un répertoire spécifié par le chemin d’accès, déplacez la DLL vers un répertoire référencé.</span><span class="sxs-lookup"><span data-stu-id="e190e-113">If the DLL or referenced DLL is not in a directory specified by the path, move the DLL to a referenced directory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e190e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e190e-114">See also</span></span>

- [<span data-ttu-id="e190e-115">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="e190e-115">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
