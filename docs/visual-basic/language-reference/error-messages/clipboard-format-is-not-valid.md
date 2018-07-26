---
title: Format de Presse-papiers non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID460
ms.assetid: 71a4a045-65bb-417d-b3bd-99a9fa3c53f6
ms.openlocfilehash: f2a0ab33c1749117d5de4987e85c44602ccd29ce
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2018
ms.locfileid: "39245555"
---
# <a name="clipboard-format-is-not-valid"></a><span data-ttu-id="f7286-102">Format de Presse-papiers non valide</span><span class="sxs-lookup"><span data-stu-id="f7286-102">Clipboard format is not valid</span></span>
<span data-ttu-id="f7286-103">Le format de Presse-papiers spécifié n’est pas compatible avec la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f7286-103">The specified Clipboard format is incompatible with the method being executed.</span></span> <span data-ttu-id="f7286-104">Parmi les causes possibles de cette erreur sont :</span><span class="sxs-lookup"><span data-stu-id="f7286-104">Among the possible causes for this error are:</span></span>  
  
-   <span data-ttu-id="f7286-105">À l’aide du Presse-papiers `GetText` ou `SetText` méthode avec un format de Presse-papiers autre que `vbCFText` ou `vbCFLink`.</span><span class="sxs-lookup"><span data-stu-id="f7286-105">Using the Clipboard's `GetText` or `SetText` method with a Clipboard format other than `vbCFText` or `vbCFLink`.</span></span>  
  
-   <span data-ttu-id="f7286-106">À l’aide du Presse-papiers `GetData` ou `SetData` méthode avec un format de Presse-papiers autre que `vbCFBitmap`, `vbCFDIB`, ou `vbCFMetafile`.</span><span class="sxs-lookup"><span data-stu-id="f7286-106">Using the Clipboard's `GetData` or `SetData` method with a Clipboard format other than `vbCFBitmap`, `vbCFDIB`, or `vbCFMetafile`.</span></span>  
  
-   <span data-ttu-id="f7286-107">À l’aide de la `GetData` ou `SetData` méthodes d’un `DataObject` avec un format de Presse-papiers dans la plage réservée par Microsoft Windows pour des formats (& HC000 - & HFFFF), lorsque ce format de Presse-papiers n’a pas été inscrit avec Microsoft Windows .</span><span class="sxs-lookup"><span data-stu-id="f7286-107">Using the `GetData` or `SetData` methods of a `DataObject` with a Clipboard format in the range reserved by Microsoft Windows for registered formats (&HC000-&HFFFF), when that Clipboard format has not been registered with Microsoft Windows.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f7286-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f7286-108">To correct this error</span></span>  
  
-   <span data-ttu-id="f7286-109">Supprimer le format non valide et spécifier une valide.</span><span class="sxs-lookup"><span data-stu-id="f7286-109">Remove the invalid format and specify a valid one.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7286-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7286-110">See Also</span></span>  
 [<span data-ttu-id="f7286-111">Presse-papiers : ajout d’autres formats</span><span class="sxs-lookup"><span data-stu-id="f7286-111">Clipboard: Adding Other Formats</span></span>](/cpp/mfc/clipboard-adding-other-formats)
