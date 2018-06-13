---
title: Longueur d'enregistrement incorrecte
ms.date: 07/20/2015
f1_keywords:
- vbrID59
ms.assetid: 0926a3a4-177b-4452-9b33-d8a01e24cc21
ms.openlocfilehash: b4b311e2eb504c485772091ed126b3beb71729cb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33585968"
---
# <a name="bad-record-length"></a><span data-ttu-id="09a08-102">Longueur d'enregistrement incorrecte</span><span class="sxs-lookup"><span data-stu-id="09a08-102">Bad record length</span></span>
<span data-ttu-id="09a08-103">Cette erreur peut avoir plusieurs causes, dont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="09a08-103">Among the possible causes of this error are:</span></span>  
  
-   <span data-ttu-id="09a08-104">La longueur d’une variable d’enregistrement spécifiée dans un `FileGet`, `FileGetObject`, `FilePut` ou `FilePutObject` instruction diffère de la longueur spécifiée dans correspondant `FileOpen` instruction.</span><span class="sxs-lookup"><span data-stu-id="09a08-104">The length of a record variable specified in a `FileGet`, `FileGetObject`, `FilePut` or `FilePutObject` statement differs from the length specified in the corresponding `FileOpen` statement.</span></span>  
  
-   <span data-ttu-id="09a08-105">La variable dans un `FilePut` ou `FilePutObject` instruction est ou inclut une chaîne de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="09a08-105">The variable in a `FilePut` or `FilePutObject` statement is or includes a variable-length string.</span></span>  
  
-   <span data-ttu-id="09a08-106">La variable dans un `FilePut` ou `FilePutObject` est ou inclut un `Variant` type.</span><span class="sxs-lookup"><span data-stu-id="09a08-106">The variable in a `FilePut` or `FilePutObject` is or includes a `Variant` type.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="09a08-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="09a08-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="09a08-108">Assurez-vous que la somme des tailles des variables à longueur fixe dans le type défini par l’utilisateur de définition de type de la variable d’enregistrement est identique à la valeur indiquée dans le `FileOpen` l’instruction `Len` clause.</span><span class="sxs-lookup"><span data-stu-id="09a08-108">Make sure the sum of the sizes of fixed-length variables in the user-defined type defining the record variable's type is the same as the value stated in the `FileOpen` statement's `Len` clause.</span></span>  
  
2.  <span data-ttu-id="09a08-109">Si la variable dans un `FilePut` ou `FilePutObject` instruction est ou inclut une chaîne de longueur variable, vérifiez que la chaîne de longueur variable est au moins 2 caractères plus courtes que la longueur d’enregistrement spécifiée dans le `Len` clause de la `FileOpen` instruction.</span><span class="sxs-lookup"><span data-stu-id="09a08-109">If the variable in a `FilePut` or `FilePutObject` statement is or includes a variable-length string, make sure the variable-length string is at least 2 characters shorter than the record length specified in the `Len` clause of the `FileOpen` statement.</span></span>  
  
3.  <span data-ttu-id="09a08-110">Si la variable dans un `FilePut` ou `FilePutObject` est ou inclut un `Variant` Assurez-vous que la chaîne de longueur variable est au moins de 4 octets plus court que la longueur d’enregistrement spécifiée dans le `Len` clause de la `FileOpen` instruction.</span><span class="sxs-lookup"><span data-stu-id="09a08-110">If the variable in a `FilePut` or `FilePutObject` is or includes a `Variant` make sure the variable-length string is at least 4 bytes shorter than the record length specified in the `Len` clause of the `FileOpen` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09a08-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09a08-111">See Also</span></span>  
 <xref:Microsoft.VisualBasic.FileSystem.FileGet%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.FileGetObject%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.FilePut%2A>  
 <xref:Microsoft.VisualBasic.FileSystem.FilePutObject%2A>
