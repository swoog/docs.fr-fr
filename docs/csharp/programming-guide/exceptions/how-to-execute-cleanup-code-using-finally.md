---
title: Guide pratique pour exécuter le code de nettoyage à l'aide de finally (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- try/finally blocks [C#]
- exceptions [C#], try/finally block
- exception handling [C#], try/finally block
ms.assetid: 1b1e5aef-3f32-4a88-9d39-b5fffb33bdaf
ms.openlocfilehash: 47e9bb368deb077ef10ce474683d81e0cb56cef8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44183783"
---
# <a name="how-to-execute-cleanup-code-using-finally-c-programming-guide"></a><span data-ttu-id="b8730-102">Guide pratique pour exécuter le code de nettoyage à l'aide de finally (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="b8730-102">How to: Execute Cleanup Code Using finally (C# Programming Guide)</span></span>
<span data-ttu-id="b8730-103">L’objectif d’une instruction `finally` est de vérifier que le nettoyage nécessaire des objets, généralement ceux contenant des ressources externes, se produit immédiatement, même si une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="b8730-103">The purpose of a `finally` statement is to ensure that the necessary cleanup of objects, usually objects that are holding external resources, occurs immediately, even if an exception is thrown.</span></span> <span data-ttu-id="b8730-104">Un exemple de nettoyage de ce type est l’appel à <xref:System.IO.Stream.Close%2A> sur un <xref:System.IO.FileStream> immédiatement après son utilisation au lieu d’attendre que l’objet soit récupéré par garbage collection par le Common Language Runtime, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b8730-104">One example of such cleanup is calling <xref:System.IO.Stream.Close%2A> on a <xref:System.IO.FileStream> immediately after use instead of waiting for the object to be garbage collected by the common language runtime, as follows:</span></span>  
  
 [!code-csharp[csProgGuideExceptions#16](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/how-to-execute-cleanup-code-using-finally_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="b8730-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8730-105">Example</span></span>  
 <span data-ttu-id="b8730-106">Pour transformer le code précédent en instruction `try-catch-finally`, le code de nettoyage est séparé du code actif comme suit.</span><span class="sxs-lookup"><span data-stu-id="b8730-106">To turn the previous code into a `try-catch-finally` statement, the cleanup code is separated from the working code, as follows.</span></span>  
  
 [!code-csharp[csProgGuideExceptions#17](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/how-to-execute-cleanup-code-using-finally_2.cs)]  
  
 <span data-ttu-id="b8730-107">Comme une exception peut se produire à tout moment dans le bloc `try` avant l’appel à `OpenWrite()`, ou comme l’appel `OpenWrite()` lui-même peut échouer, nous n’avons aucune garantie que le fichier est ouvert quand nous essayons de le fermer.</span><span class="sxs-lookup"><span data-stu-id="b8730-107">Because an exception can occur at any time within the `try` block before the `OpenWrite()` call, or the `OpenWrite()` call itself could fail, we are not guaranteed that the file is open when we try to close it.</span></span> <span data-ttu-id="b8730-108">Le bloc `finally` ajoute un contrôle pour garantir que l’objet <xref:System.IO.FileStream> n’est pas `null` avant d’appeler la méthode <xref:System.IO.Stream.Close%2A>.</span><span class="sxs-lookup"><span data-stu-id="b8730-108">The `finally` block adds a check to make sure that the <xref:System.IO.FileStream> object is not `null` before you call the <xref:System.IO.Stream.Close%2A> method.</span></span> <span data-ttu-id="b8730-109">Sans le contrôle `null`, le bloc `finally` pourrait lever sa propre <xref:System.NullReferenceException>, mais la levée d’exceptions dans des blocs `finally` doit être évitée, dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="b8730-109">Without the `null` check, the `finally` block could throw its own <xref:System.NullReferenceException>, but throwing exceptions in `finally` blocks should be avoided if it is possible.</span></span>  
  
 <span data-ttu-id="b8730-110">Une connexion de base de données est également susceptible d’être fermée dans un bloc `finally`.</span><span class="sxs-lookup"><span data-stu-id="b8730-110">A database connection is another good candidate for being closed in a `finally` block.</span></span> <span data-ttu-id="b8730-111">Le nombre de connexions à un serveur de base de données étant parfois limité, vous devez fermer les connexions de base de données le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="b8730-111">Because the number of connections allowed to a database server is sometimes limited, you should close database connections as quickly as possible.</span></span> <span data-ttu-id="b8730-112">Si une exception est levée avant que vous puissiez fermer votre connexion, c’est un autre cas où il vaut mieux utiliser le bloc `finally` qu’attendre le nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b8730-112">If an exception is thrown before you can close your connection, this is another case where using the `finally` block is better than waiting for garbage collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8730-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8730-113">See Also</span></span>

- [<span data-ttu-id="b8730-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b8730-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="b8730-115">Exceptions et gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="b8730-115">Exceptions and Exception Handling</span></span>](../../../csharp/programming-guide/exceptions/index.md)  
- [<span data-ttu-id="b8730-116">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="b8730-116">Exception Handling</span></span>](../../../csharp/programming-guide/exceptions/exception-handling.md)  
- [<span data-ttu-id="b8730-117">using, instruction</span><span class="sxs-lookup"><span data-stu-id="b8730-117">using Statement</span></span>](../../../csharp/language-reference/keywords/using-statement.md)  
- [<span data-ttu-id="b8730-118">try-catch</span><span class="sxs-lookup"><span data-stu-id="b8730-118">try-catch</span></span>](../../../csharp/language-reference/keywords/try-catch.md)  
- [<span data-ttu-id="b8730-119">try-finally</span><span class="sxs-lookup"><span data-stu-id="b8730-119">try-finally</span></span>](../../../csharp/language-reference/keywords/try-finally.md)  
- [<span data-ttu-id="b8730-120">try-catch-finally</span><span class="sxs-lookup"><span data-stu-id="b8730-120">try-catch-finally</span></span>](../../../csharp/language-reference/keywords/try-catch-finally.md)
