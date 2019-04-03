---
title: 'Procédure : Valider les noms de fichiers et chemins d’accès dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- file names [Visual Basic], validating
- strings [Visual Basic], validating
- Boolean values [Visual Basic]
- paths [Visual Basic], validating
ms.assetid: f673462d-57b7-4120-b13a-6a7592f7ab2c
ms.openlocfilehash: c8e01a0f5a3f99fdbc424d6cd7d224367c7bad08
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58835802"
---
# <a name="how-to-validate-file-names-and-paths-in-visual-basic"></a><span data-ttu-id="da9a9-102">Procédure : Valider les noms de fichiers et chemins d’accès dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="da9a9-102">How to: Validate File Names and Paths in Visual Basic</span></span>
<span data-ttu-id="da9a9-103">Cet exemple retourne un `Boolean` valeur qui indique si une chaîne représente un nom de fichier ou le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="da9a9-103">This example returns a `Boolean` value that indicates whether a string represents a file name or path.</span></span> <span data-ttu-id="da9a9-104">La validation vérifie si le nom contient des caractères qui ne sont pas autorisés par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="da9a9-104">The validation checks if the name contains characters that are not allowed by the file system.</span></span>  
  
## <a name="example"></a><span data-ttu-id="da9a9-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="da9a9-105">Example</span></span>  
 [!code-vb[VbVbcnRegEx#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#4)]  
  
 <span data-ttu-id="da9a9-106">Cet exemple ne vérifie pas si le nom a placé incorrectement deux-points ou répertoires sans nom, ou si la longueur du nom dépasse la longueur maximale définie par le système.</span><span class="sxs-lookup"><span data-stu-id="da9a9-106">This example does not check if the name has incorrectly placed colons, or directories with no name, or if the length of the name exceeds the system-defined maximum length.</span></span> <span data-ttu-id="da9a9-107">Elle également ne vérifie pas si l’application est autorisé à accéder à la ressource de système de fichiers avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="da9a9-107">It also does not check if the application has permission to access the file-system resource with the specified name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da9a9-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da9a9-108">See also</span></span>

- <xref:System.IO.Path.GetInvalidPathChars%2A>
- [<span data-ttu-id="da9a9-109">Validation de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="da9a9-109">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
