---
title: Sécurisation de la gestion des exceptions
ms.date: 03/30/2017
dev_langs:
- cpp
helpviewer_keywords:
- code security, exception handling
- security [.NET Framework], exception handling
- secure coding, exception handling
- exception handling, security
ms.assetid: 1f3da743-9742-47ff-96e6-d0dd1e9e1c19
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bc8cd20a4183ffd002f1399b6b50c8956208a21b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61868798"
---
# <a name="securing-exception-handling"></a><span data-ttu-id="199f9-102">Sécurisation de la gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="199f9-102">Securing Exception Handling</span></span>
<span data-ttu-id="199f9-103">Dans Visual C++ et Visual Basic, une expression de filtre plus haut de la pile s’exécute avant tout **enfin** instruction.</span><span class="sxs-lookup"><span data-stu-id="199f9-103">In Visual C++ and Visual Basic, a filter expression further up the stack runs before any **finally** statement.</span></span> <span data-ttu-id="199f9-104">Le **catch** bloc associé à ce filtre s’exécute après le **enfin** instruction.</span><span class="sxs-lookup"><span data-stu-id="199f9-104">The **catch** block associated with that filter runs after the **finally** statement.</span></span> <span data-ttu-id="199f9-105">Pour plus d’informations, consultez [utilisation d’Exceptions](../../../docs/standard/exceptions/using-user-filtered-exception-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="199f9-105">For more information, see [Using User-Filtered Exceptions](../../../docs/standard/exceptions/using-user-filtered-exception-handlers.md).</span></span> <span data-ttu-id="199f9-106">Cette section examine les implications de sécurité de cet ordre.</span><span class="sxs-lookup"><span data-stu-id="199f9-106">This section examines the security implications of this order.</span></span> <span data-ttu-id="199f9-107">Prenons l’exemple de pseudo-code suivant qui illustre l’ordre dans les instructions de filtre et **enfin** instructions sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="199f9-107">Consider the following pseudocode example that illustrates the order in which filter statements and **finally** statements run.</span></span>  
  
```cpp  
void Main()   
{  
    try   
    {  
        Sub();  
    }   
    except (Filter())   
    {  
        Console.WriteLine("catch");  
    }  
}  
bool Filter () {  
    Console.WriteLine("filter");  
    return true;  
}  
void Sub()   
{  
    try   
    {  
        Console.WriteLine("throw");  
        throw new Exception();  
    }   
    finally   
    {  
        Console.WriteLine("finally");  
    }  
}                        
```  
  
 <span data-ttu-id="199f9-108">Ce code imprime les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="199f9-108">This code prints the following.</span></span>  
  
```  
Throw  
Filter  
Finally  
Catch  
```  
  
 <span data-ttu-id="199f9-109">Le filtre s’exécute avant le **enfin** instruction, donc les problèmes de sécurité peuvent être introduites par tout ce qui rend à un état de modification où l’exécution d’un autre code peut tirer parti.</span><span class="sxs-lookup"><span data-stu-id="199f9-109">The filter runs before the **finally** statement, so security issues can be introduced by anything that makes a state change where execution of other code could take advantage.</span></span> <span data-ttu-id="199f9-110">Exemple :</span><span class="sxs-lookup"><span data-stu-id="199f9-110">For example:</span></span>  
  
```cpp  
try   
{  
    Alter_Security_State();  
    // This means changing anything (state variables,  
    // switching unmanaged context, impersonation, and   
    // so on) that could be exploited if malicious   
    // code ran before state is restored.  
    Do_some_work();  
}   
finally   
{  
    Restore_Security_State();  
    // This simply restores the state change above.  
}  
```  
  
 <span data-ttu-id="199f9-111">Ce pseudocode permet à un filtre plu haut dans la pile pour exécuter du code arbitraire.</span><span class="sxs-lookup"><span data-stu-id="199f9-111">This pseudocode allows a filter higher up the stack to run arbitrary code.</span></span> <span data-ttu-id="199f9-112">Autres exemples d’opérations qui auraient un effet similaire sont l’emprunt d’identité temporaire d’une autre identité, en définissant un indicateur interne qui ignore la vérification de sécurité ou de modification de la culture associée au thread.</span><span class="sxs-lookup"><span data-stu-id="199f9-112">Other examples of operations that would have a similar effect are temporary impersonation of another identity, setting an internal flag that bypasses some security check, or changing the culture associated with the thread.</span></span> <span data-ttu-id="199f9-113">La solution recommandée consiste à introduire un gestionnaire d’exceptions pour isoler les modifications du code à l’état du thread à partir de blocs de filtre aux appelants.</span><span class="sxs-lookup"><span data-stu-id="199f9-113">The recommended solution is to introduce an exception handler to isolate the code's changes to thread state from callers' filter blocks.</span></span> <span data-ttu-id="199f9-114">Toutefois, il est important que le Gestionnaire d’exceptions soit correctement introduit ou ce problème ne sera pas résolu.</span><span class="sxs-lookup"><span data-stu-id="199f9-114">However, it is important that the exception handler be properly introduced or this problem will not be fixed.</span></span> <span data-ttu-id="199f9-115">L’exemple suivant active la culture d’interface utilisateur, mais n’importe quel type de changement d’état de thread peut être exposée de la même façon.</span><span class="sxs-lookup"><span data-stu-id="199f9-115">The following example switches the UI culture, but any kind of thread state change could be similarly exposed.</span></span>  
  
```cpp  
YourObject.YourMethod()  
{  
   CultureInfo saveCulture = Thread.CurrentThread.CurrentUICulture;  
   try {  
      Thread.CurrentThread.CurrentUICulture = new CultureInfo("de-DE");  
      // Do something that throws an exception.  
}  
   finally {  
      Thread.CurrentThread.CurrentUICulture = saveCulture;  
   }  
}  
```  
  
```vb  
Public Class UserCode  
   Public Shared Sub Main()  
      Try  
         Dim obj As YourObject = new YourObject  
         obj.YourMethod()  
      Catch e As Exception When FilterFunc  
         Console.WriteLine("An error occurred: '{0}'", e)  
         Console.WriteLine("Current Culture: {0}",   
Thread.CurrentThread.CurrentUICulture)  
      End Try  
   End Sub  
  
   Public Function FilterFunc As Boolean  
      Console.WriteLine("Current Culture: {0}", Thread.CurrentThread.CurrentUICulture)  
      Return True  
   End Sub  
  
End Class  
```  
  
 <span data-ttu-id="199f9-116">La correction appropriée est dans ce cas consiste à encapsuler existant **essayez**/**enfin** bloquer un **essayez**/**catch** bloc.</span><span class="sxs-lookup"><span data-stu-id="199f9-116">The correct fix in this case is to wrap the existing **try**/**finally** block in a **try**/**catch** block.</span></span> <span data-ttu-id="199f9-117">Présentation de simplement un **catch-throw** clause dans existant **essayez**/**enfin** bloc ne résout pas le problème, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="199f9-117">Simply introducing a **catch-throw** clause into the existing **try**/**finally** block does not fix the problem, as shown in the following example.</span></span>  
  
```cpp  
YourObject.YourMethod()  
{  
    CultureInfo saveCulture = Thread.CurrentThread.CurrentUICulture;  
  
    try   
    {  
        Thread.CurrentThread.CurrentUICulture = new CultureInfo("de-DE");  
        // Do something that throws an exception.  
    }  
    catch { throw; }  
    finally   
    {  
        Thread.CurrentThread.CurrentUICulture = saveCulture;  
    }  
}  
```  
  
 <span data-ttu-id="199f9-118">Cela ne résout pas le problème, car le **enfin** instruction n’a pas été exécuté auparavant le `FilterFunc` Obtient le contrôle.</span><span class="sxs-lookup"><span data-stu-id="199f9-118">This does not fix the problem because the **finally** statement has not run before the `FilterFunc` gets control.</span></span>  
  
 <span data-ttu-id="199f9-119">L’exemple suivant résout le problème en s’assurant que le **enfin** clause a exécutée avant de proposer une exception des blocs de filtre d’exceptions aux appelants.</span><span class="sxs-lookup"><span data-stu-id="199f9-119">The following example fixes the problem by ensuring that the **finally** clause has executed before offering an exception up the callers' exception filter blocks.</span></span>  
  
```cpp  
YourObject.YourMethod()  
{  
    CultureInfo saveCulture = Thread.CurrentThread.CurrentUICulture;  
    try    
    {  
        try   
        {  
            Thread.CurrentThread.CurrentUICulture = new CultureInfo("de-DE");  
            // Do something that throws an exception.  
        }  
        finally   
        {  
            Thread.CurrentThread.CurrentUICulture = saveCulture;  
        }  
    }  
    catch { throw; }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="199f9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="199f9-120">See also</span></span>

- [<span data-ttu-id="199f9-121">Instructions de codage sécurisé</span><span class="sxs-lookup"><span data-stu-id="199f9-121">Secure Coding Guidelines</span></span>](../../../docs/standard/security/secure-coding-guidelines.md)
