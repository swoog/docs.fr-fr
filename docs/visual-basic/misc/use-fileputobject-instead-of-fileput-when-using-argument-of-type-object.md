---
title: Utilisez ’FilePutObject’ à la place de ’FilePut’ quand l’argument est de type ’Object’.
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: 3d793151905c61ee12eccdfdb5e9567a4924bb35
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62022517"
---
# <a name="use-fileputobject-instead-of-fileput-when-using-argument-of-type-object"></a><span data-ttu-id="515a2-102">Utilisez ’FilePutObject’ à la place de ’FilePut’ quand l’argument est de type ’Object’.</span><span class="sxs-lookup"><span data-stu-id="515a2-102">Use 'FilePutObject' instead of 'FilePut' when using argument of type 'Object'</span></span>
<span data-ttu-id="515a2-103">La méthode `FilePut` comprend un argument de type `Object`.</span><span class="sxs-lookup"><span data-stu-id="515a2-103">The `FilePut` method includes an argument of type `Object`.</span></span> <span data-ttu-id="515a2-104">`FilePutObject` doit être utilisé à la place de `FilePut` pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="515a2-104">`FilePutObject` should be used in place of `FilePut` to avoid ambiguities.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="515a2-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="515a2-105">To correct this error</span></span>  
  
- <span data-ttu-id="515a2-106">Remplacez `FilePut` par `FilePutObject`.</span><span class="sxs-lookup"><span data-stu-id="515a2-106">Replace `FilePut` with `FilePutObject`.</span></span>  
  
- <span data-ttu-id="515a2-107">Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="515a2-107">Cast the `Object` argument to a more specific type.</span></span>  
  
- <span data-ttu-id="515a2-108">Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .</span><span class="sxs-lookup"><span data-stu-id="515a2-108">Use the functionality available in the `My.Computer.FileSystem` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="515a2-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="515a2-109">See also</span></span>

- [<span data-ttu-id="515a2-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="515a2-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)
- [<span data-ttu-id="515a2-111">My.Computer.FileSystem.WriteAllBytes</span><span class="sxs-lookup"><span data-stu-id="515a2-111">My.Computer.FileSystem.WriteAllBytes</span></span>](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
