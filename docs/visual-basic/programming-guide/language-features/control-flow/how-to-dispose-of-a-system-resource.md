---
title: 'Procédure : Supprimer une ressource système (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Using statement [Visual Basic], disposing of system resources
- Visual Basic code, control flow
- system resources, disposing of
- resources [Visual Basic], disposing of system
- system resources
- Using statement [Visual Basic], Using...End Using
- Using block
ms.assetid: 8be2b239-8090-419b-8e7e-bcaa75b0ecc8
ms.openlocfilehash: 2a399b92c66c8a88d10d661ff41aef58a82bbc2a
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58829913"
---
# <a name="how-to-dispose-of-a-system-resource-visual-basic"></a><span data-ttu-id="3e6e5-102">Procédure : Supprimer une ressource système (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3e6e5-102">How to: Dispose of a System Resource (Visual Basic)</span></span>
<span data-ttu-id="3e6e5-103">Vous pouvez utiliser un `Using` bloc pour garantir que le système supprime une ressource lorsque votre code quitte le bloc.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-103">You can use a `Using` block to guarantee that the system disposes of a resource when your code exits the block.</span></span> <span data-ttu-id="3e6e5-104">Cela est utile si vous utilisez une ressource système qui consomme une grande quantité de mémoire ou d’autres composants également vouloir utiliser.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-104">This is useful if you are using a system resource that consumes a large amount of memory, or that other components also want to use.</span></span>  
  
### <a name="to-dispose-of-a-database-connection-when-your-code-is-finished-with-it"></a><span data-ttu-id="3e6e5-105">Pour supprimer une connexion de base de données lorsque votre code est terminé avec lui</span><span class="sxs-lookup"><span data-stu-id="3e6e5-105">To dispose of a database connection when your code is finished with it</span></span>  
  
1.  <span data-ttu-id="3e6e5-106">Veillez à inclure le texte approprié [instruction Imports (.NET Namespace et Type)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) pour la connexion de base de données au début de votre fichier source (dans ce cas, <xref:System.Data.SqlClient>).</span><span class="sxs-lookup"><span data-stu-id="3e6e5-106">Make sure you include the appropriate [Imports Statement (.NET Namespace and Type)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) for the database connection at the beginning of your source file (in this case, <xref:System.Data.SqlClient>).</span></span>  
  
2.  <span data-ttu-id="3e6e5-107">Créer un `Using` bloc avec le `Using` et `End Using` instructions.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-107">Create a `Using` block with the `Using` and `End Using` statements.</span></span> <span data-ttu-id="3e6e5-108">Dans le bloc, placez le code qui traite de la connexion de base de données.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-108">Inside the block, put the code that deals with the database connection.</span></span>  
  
3.  <span data-ttu-id="3e6e5-109">Déclarez la connexion et de créer une instance de celui-ci dans le cadre de la `Using` instruction.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-109">Declare the connection and create an instance of it as part of the `Using` statement.</span></span>  
  
    ```  
    ' Insert the following line at the beginning of your source file.  
    Imports System.Data.SqlClient  
    Public Sub AccessSql(ByVal s As String)  
        Using sqc As New System.Data.SqlClient.SqlConnection(s)  
            MsgBox("Connected with string """ & sqc.ConnectionString & """")  
        End Using  
    End Sub  
    ```  
  
     <span data-ttu-id="3e6e5-110">Le système supprime la ressource, quel que soit la manière dont vous quittez le bloc, y compris le cas d’une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-110">The system disposes of the resource no matter how you exit the block, including the case of an unhandled exception.</span></span>  
  
     <span data-ttu-id="3e6e5-111">Notez que vous ne pouvez pas accéder à `sqc` à partir d’en dehors de la `Using` bloquer, car sa portée est limitée au bloc.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-111">Note that you cannot access `sqc` from outside the `Using` block, because its scope is limited to the block.</span></span>  
  
     <span data-ttu-id="3e6e5-112">Vous pouvez utiliser cette même technique sur une ressource système comme un descripteur de fichier ou un wrapper COM.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-112">You can use this same technique on a system resource such as a file handle or a COM wrapper.</span></span> <span data-ttu-id="3e6e5-113">Vous utilisez un `Using` bloquer quand vous voulez être certain de laisser la ressource est disponible pour d’autres composants après avoir quitté le `Using` bloc.</span><span class="sxs-lookup"><span data-stu-id="3e6e5-113">You use a `Using` block when you want to be sure to leave the resource available for other components after you have exited the `Using` block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e6e5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e6e5-114">See also</span></span>

- <xref:System.Data.SqlClient.SqlConnection>
- [<span data-ttu-id="3e6e5-115">Flux de contrôle</span><span class="sxs-lookup"><span data-stu-id="3e6e5-115">Control Flow</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)
- [<span data-ttu-id="3e6e5-116">Structures de décision</span><span class="sxs-lookup"><span data-stu-id="3e6e5-116">Decision Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [<span data-ttu-id="3e6e5-117">Structures de boucle</span><span class="sxs-lookup"><span data-stu-id="3e6e5-117">Loop Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [<span data-ttu-id="3e6e5-118">Autres structures de contrôle</span><span class="sxs-lookup"><span data-stu-id="3e6e5-118">Other Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/other-control-structures.md)
- [<span data-ttu-id="3e6e5-119">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="3e6e5-119">Nested Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="3e6e5-120">Using (instruction)</span><span class="sxs-lookup"><span data-stu-id="3e6e5-120">Using Statement</span></span>](../../../../visual-basic/language-reference/statements/using-statement.md)
