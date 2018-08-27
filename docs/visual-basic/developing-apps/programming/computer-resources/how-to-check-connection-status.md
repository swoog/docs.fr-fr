---
title: Guide pratique pour vérifier l'état de la connexion en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- Web connections [Visual Basic]
- IsAvailable property [Visual Basic], about IsAvailable
- connections [Visual Basic], checking status
- connection status [Visual Basic]
ms.assetid: 4d9ee8ab-9a6f-4279-ace4-b75afc976a74
ms.openlocfilehash: 4a6cb67474d03ada5e0a73d94f65da7a381c44a8
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2018
ms.locfileid: "42911939"
---
# <a name="how-to-check-connection-status-in-visual-basic"></a><span data-ttu-id="96eea-102">Guide pratique pour vérifier l'état de la connexion en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="96eea-102">How to: Check Connection Status in Visual Basic</span></span>
<span data-ttu-id="96eea-103">Vous pouvez utiliser la propriété <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable> pour déterminer si l’ordinateur dispose d’une connexion Internet ou réseau active.</span><span class="sxs-lookup"><span data-stu-id="96eea-103">The <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable> property can be used to determine whether the computer has a working network or Internet connection.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-check-whether-a-computer-has-a-working-connection"></a><span data-ttu-id="96eea-104">Pour vérifier si un ordinateur dispose d’une connexion active</span><span class="sxs-lookup"><span data-stu-id="96eea-104">To check whether a computer has a working connection</span></span>  
  
-   <span data-ttu-id="96eea-105">Vérifiez si la propriété `IsAvailable` est `True` ou `False`.</span><span class="sxs-lookup"><span data-stu-id="96eea-105">Determine whether the `IsAvailable` property is `True` or `False`.</span></span> <span data-ttu-id="96eea-106">Le code suivant vérifie l’état de la propriété et le signale :</span><span class="sxs-lookup"><span data-stu-id="96eea-106">The following code checks the property's status and reports it:</span></span>  
  
     [!code-vb[VbResourceTasks#3](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-check-connection-status_1.vb)]  
  
     <span data-ttu-id="96eea-107">Cet exemple de code est également disponible sous la forme d’un extrait de code IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="96eea-107">This code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="96eea-108">Dans le sélecteur d’extraits de code, il se trouve sous **Connectivité et réseau**.</span><span class="sxs-lookup"><span data-stu-id="96eea-108">In the code snippet picker, it is located in **Connectivity and Networking**.</span></span> <span data-ttu-id="96eea-109">Pour plus d’informations, consultez [Extraits de code](/visualstudio/ide/code-snippets).</span><span class="sxs-lookup"><span data-stu-id="96eea-109">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96eea-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96eea-110">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Devices.Network?displayProperty=nameWithType>  
 <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable>
