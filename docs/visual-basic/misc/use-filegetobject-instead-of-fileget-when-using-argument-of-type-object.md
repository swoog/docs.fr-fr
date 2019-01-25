---
title: Utilisez ’FileGetObject’ à la place de ’FileGet’ quand l’argument est de type ’Object’.
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: 60eaabc686070aced908116728f06d4e82b5cecb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723392"
---
# <a name="use-filegetobject-instead-of-fileget-when-using-argument-of-type-object"></a><span data-ttu-id="83cb6-102">Utilisez ’FileGetObject’ à la place de ’FileGet’ quand l’argument est de type ’Object’.</span><span class="sxs-lookup"><span data-stu-id="83cb6-102">Use 'FileGetObject' instead of 'FileGet' when using argument of type 'Object'</span></span>
<span data-ttu-id="83cb6-103">La méthode `FileGet` comprend un argument de type `Object`.</span><span class="sxs-lookup"><span data-stu-id="83cb6-103">The `FileGet` method includes an argument of type `Object`.</span></span> <span data-ttu-id="83cb6-104">`FileGetObject` doit être utilisé à la place de `FileGet` pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="83cb6-104">`FileGetObject` should be used in place of `FileGet` to avoid ambiguities.</span></span>  
  
 <span data-ttu-id="83cb6-105">Notez que les fonctionnalités offertes par `My.Computer.Filesystem` proposent une plus grande facilité d’utilisation et des performances accrues par rapport à `FileGet` ou `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="83cb6-105">Notice that the functionality offered by `My.Computer.Filesystem` offers greater ease of use and performance than either `FileGet` or `FileGetObject`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="83cb6-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="83cb6-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="83cb6-107">Remplacez `FileGet` par `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="83cb6-107">Replace `FileGet` with `FileGetObject`.</span></span>  
  
2.  <span data-ttu-id="83cb6-108">Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="83cb6-108">Cast the `Object` argument to a more specific type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83cb6-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83cb6-109">See also</span></span>

- [<span data-ttu-id="83cb6-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="83cb6-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)
