---
title: 'Procédure : Valider les noms de fichiers et chemins d’accès dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- file names [Visual Basic], validating
- strings [Visual Basic], validating
- Boolean values [Visual Basic]
- paths [Visual Basic], validating
ms.assetid: f673462d-57b7-4120-b13a-6a7592f7ab2c
ms.openlocfilehash: d29553071d68319d754406b3104da6e096f908fd
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56975522"
---
# <a name="how-to-validate-file-names-and-paths-in-visual-basic"></a><span data-ttu-id="b84aa-102">Procédure : Valider les noms de fichiers et chemins d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b84aa-102">How to: Validate File Names and Paths in Visual Basic</span></span>
<span data-ttu-id="b84aa-103">Cet exemple retourne un `Boolean` valeur qui indique si une chaîne représente un nom de fichier ou le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b84aa-103">This example returns a `Boolean` value that indicates whether a string represents a file name or path.</span></span> <span data-ttu-id="b84aa-104">La validation vérifie si le nom contient des caractères qui ne sont pas autorisés par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b84aa-104">The validation checks if the name contains characters that are not allowed by the file system.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b84aa-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="b84aa-105">Example</span></span>  
 [!code-vb[VbVbcnRegEx#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#4)]  
  
 <span data-ttu-id="b84aa-106">Cet exemple ne vérifie pas si le nom a placé incorrectement deux-points ou répertoires sans nom, ou si la longueur du nom dépasse la longueur maximale définie par le système.</span><span class="sxs-lookup"><span data-stu-id="b84aa-106">This example does not check if the name has incorrectly placed colons, or directories with no name, or if the length of the name exceeds the system-defined maximum length.</span></span> <span data-ttu-id="b84aa-107">Elle également ne vérifie pas si l’application est autorisé à accéder à la ressource de système de fichiers avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="b84aa-107">It also does not check if the application has permission to access the file-system resource with the specified name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b84aa-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b84aa-108">See also</span></span>
- <xref:System.IO.Path.GetInvalidPathChars%2A>
- [<span data-ttu-id="b84aa-109">Validation de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b84aa-109">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
