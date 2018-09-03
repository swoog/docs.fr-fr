---
title: "Comment : faire en sorte qu'une variable objet ne fasse pas référence à une instance (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- Nothing keyword [Visual Basic], variable assignment
- object variables [Visual Basic], null reference
ms.assetid: e6d30578-bdae-4142-a3ac-a10697bf696a
ms.openlocfilehash: 8f85ba0adea522851e45b20ef5024491874c9a29
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482946"
---
# <a name="how-to-make-an-object-variable-not-refer-to-any-instance-visual-basic"></a><span data-ttu-id="c1aa3-102">Comment : faire en sorte qu'une variable objet ne fasse pas référence à une instance (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c1aa3-102">How to: Make an Object Variable Not Refer to Any Instance (Visual Basic)</span></span>
<span data-ttu-id="c1aa3-103">Vous pouvez dissocier une variable objet à partir de n’importe quelle instance d’objet en lui affectant [rien](../../../../visual-basic/language-reference/nothing.md).</span><span class="sxs-lookup"><span data-stu-id="c1aa3-103">You can disassociate an object variable from any object instance by setting it to [Nothing](../../../../visual-basic/language-reference/nothing.md).</span></span>  
  
### <a name="to-disassociate-an-object-variable-from-any-object-instance"></a><span data-ttu-id="c1aa3-104">Pour dissocier une variable objet à partir de n’importe quelle instance d’objet</span><span class="sxs-lookup"><span data-stu-id="c1aa3-104">To disassociate an object variable from any object instance</span></span>  
  
-   <span data-ttu-id="c1aa3-105">Affectez à la variable `Nothing` dans une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="c1aa3-105">Set the variable to `Nothing` in an assignment statement.</span></span>  
  
    ```  
    ' Assume account is a defined class  
    Dim currentAccount As account  
    currentAccount = Nothing  
    ```  
  
## <a name="robust-programming"></a><span data-ttu-id="c1aa3-106">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="c1aa3-106">Robust Programming</span></span>  
 <span data-ttu-id="c1aa3-107">Si votre code tente d’accéder à un membre d’une variable objet qui a été défini sur `Nothing`, un <xref:System.NullReferenceException> se produit.</span><span class="sxs-lookup"><span data-stu-id="c1aa3-107">If your code tries to access a member of an object variable that has been set to `Nothing`, a <xref:System.NullReferenceException> occurs.</span></span> <span data-ttu-id="c1aa3-108">Si vous définissez une variable objet `Nothing` fréquemment, ou s’il est possible de la variable n’est pas initialisée, il est judicieux de placer les accès aux membres dans un `Try...Catch...Finally` bloc.</span><span class="sxs-lookup"><span data-stu-id="c1aa3-108">If you set an object variable to `Nothing` frequently, or if it is possible the variable is not initialized, it is a good idea to enclose member accesses in a `Try...Catch...Finally` block.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="c1aa3-109">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="c1aa3-109">.NET Framework Security</span></span>  
 <span data-ttu-id="c1aa3-110">Si vous utilisez une variable d’objet pour les objets qui contiennent des données confidentielles ou sensibles, vous pouvez définir la variable `Nothing` lorsque vous N'utilisez pas activement un de ces objets.</span><span class="sxs-lookup"><span data-stu-id="c1aa3-110">If you use an object variable for objects that contain confidential or sensitive data, you can set the variable to `Nothing` when you are not actively dealing with one of those objects.</span></span> <span data-ttu-id="c1aa3-111">Cela réduit le risque de code malveillant accède aux données.</span><span class="sxs-lookup"><span data-stu-id="c1aa3-111">This reduces the chance of malicious code gaining access to the data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1aa3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1aa3-112">See Also</span></span>  
 <xref:System.NullReferenceException>  
 [<span data-ttu-id="c1aa3-113">Variables objets</span><span class="sxs-lookup"><span data-stu-id="c1aa3-113">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [<span data-ttu-id="c1aa3-114">Assignation des variables objets</span><span class="sxs-lookup"><span data-stu-id="c1aa3-114">Object Variable Assignment</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)  
 [<span data-ttu-id="c1aa3-115">Nothing</span><span class="sxs-lookup"><span data-stu-id="c1aa3-115">Nothing</span></span>](../../../../visual-basic/language-reference/nothing.md)  
 [<span data-ttu-id="c1aa3-116">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="c1aa3-116">Try...Catch...Finally Statement</span></span>](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [<span data-ttu-id="c1aa3-117">Dépannage des exceptions : System.NullReferenceException</span><span class="sxs-lookup"><span data-stu-id="c1aa3-117">Troubleshooting Exceptions: System.NullReferenceException</span></span>](https://msdn.microsoft.com/library/4822b0b4-8105-43fb-887a-3cc51ff02899)
