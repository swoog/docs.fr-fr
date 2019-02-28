---
title: Exécution de tâches avec My.Application, My.Computer et My.User (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My.Application object [Visual Basic], developing applications
- rapid application development (RAD), My.Application
- rapid application development (RAD), My.Computer
- rapid application development (RAD), My.User
- My.Computer object [Visual Basic], developing applications
- My.User object [Visual Basic], developing applications
ms.assetid: c8af61bd-4dd3-4a0f-9af5-795b594b240b
ms.openlocfilehash: 56d79691a216f87c847474ce4340b454850b9b11
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56969698"
---
# <a name="performing-tasks-with-myapplication-mycomputer-and-myuser-visual-basic"></a><span data-ttu-id="d2315-102">Exécution de tâches avec My.Application, My.Computer et My.User (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d2315-102">Performing Tasks with My.Application, My.Computer, and My.User (Visual Basic)</span></span>
<span data-ttu-id="d2315-103">Les trois central `My` sont des objets qui fournissent l’accès aux informations et couramment utilisé la fonctionnalité `My.Application` (<xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>), `My.Computer` (<xref:Microsoft.VisualBasic.Devices.Computer>), et `My.User` (<xref:Microsoft.VisualBasic.ApplicationServices.User>).</span><span class="sxs-lookup"><span data-stu-id="d2315-103">The three central `My` objects that provide access to information and commonly used functionality are `My.Application` (<xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>), `My.Computer` (<xref:Microsoft.VisualBasic.Devices.Computer>), and `My.User` (<xref:Microsoft.VisualBasic.ApplicationServices.User>).</span></span> <span data-ttu-id="d2315-104">Vous pouvez utiliser ces objets pour accéder aux informations relatives à l’application actuelle, l’application est installée sur l’ordinateur ou l’utilisateur actuel de l’application, respectivement.</span><span class="sxs-lookup"><span data-stu-id="d2315-104">You can use these objects to access information that is related to the current application, the computer that the application is installed on, or the current user of the application, respectively.</span></span>  
  
## <a name="myapplication-mycomputer-and-myuser"></a><span data-ttu-id="d2315-105">My.Application, My.Computer et My.User</span><span class="sxs-lookup"><span data-stu-id="d2315-105">My.Application, My.Computer, and My.User</span></span>  
 <span data-ttu-id="d2315-106">Les exemples suivants montrent comment les informations peuvent être récupérées à l’aide `My`.</span><span class="sxs-lookup"><span data-stu-id="d2315-106">The following examples demonstrate how information can be retrieved using `My`.</span></span>  
  
 [!code-vb[VbVbcnMy#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#1)]  
  
 [!code-vb[VbVbcnMy#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#2)]  
  
 <span data-ttu-id="d2315-107">En plus de la récupération des informations, les membres exposés via ces trois objets vous permettent également d’exécuter des méthodes associées à cet objet.</span><span class="sxs-lookup"><span data-stu-id="d2315-107">In addition to retrieving information, the members exposed through these three objects also allow you to execute methods related to that object.</span></span> <span data-ttu-id="d2315-108">Par exemple, vous pouvez accéder à diverses méthodes pour manipuler des fichiers ou mettre à jour le Registre via `My.Computer`.</span><span class="sxs-lookup"><span data-stu-id="d2315-108">For instance, you can access a variety of methods to manipulate files or update the registry through `My.Computer`.</span></span>  
  
 <span data-ttu-id="d2315-109">Fichier d’e/s est considérablement plus facile et plus rapide avec `My`, qui inclut une variété de méthodes et propriétés pour la manipulation de fichiers, répertoires et lecteurs.</span><span class="sxs-lookup"><span data-stu-id="d2315-109">File I/O is significantly easier and faster with `My`, which includes a variety of methods and properties for manipulating files, directories, and drives.</span></span> <span data-ttu-id="d2315-110">Le <xref:Microsoft.VisualBasic.FileIO.TextFieldParser> objet vous permet de lire à partir des fichiers volumineux structurés qui ont délimitées ou les champs de largeur fixe.</span><span class="sxs-lookup"><span data-stu-id="d2315-110">The <xref:Microsoft.VisualBasic.FileIO.TextFieldParser> object allows you to read from large structured files that have delimited or fixed-width fields.</span></span> <span data-ttu-id="d2315-111">Cet exemple ouvre le `TextFieldParser` `reader` et l’utilise pour lire à partir de `C:\TestFolder1\test1.txt`.</span><span class="sxs-lookup"><span data-stu-id="d2315-111">This example opens the `TextFieldParser` `reader` and uses it to read from `C:\TestFolder1\test1.txt`.</span></span>  
  
 [!code-vb[VbVbalrTextFieldParser#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrTextFieldParser/VB/Class1.vb#23)]  
  
 <span data-ttu-id="d2315-112">`My.Application` vous permet de modifier la culture de votre application.</span><span class="sxs-lookup"><span data-stu-id="d2315-112">`My.Application` allows you to change the culture for your application.</span></span> <span data-ttu-id="d2315-113">L’exemple suivant montre comment cette méthode peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="d2315-113">The following example demonstrates how this method can be called.</span></span>  
  
 [!code-vb[VbVbcnMy#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMy/VB/Class1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="d2315-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2315-114">See also</span></span>
- <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>
- <xref:Microsoft.VisualBasic.Devices.Computer>
- <xref:Microsoft.VisualBasic.ApplicationServices.User>
- [<span data-ttu-id="d2315-115">Comment My dépend du type de projet</span><span class="sxs-lookup"><span data-stu-id="d2315-115">How My Depends on Project Type</span></span>](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
