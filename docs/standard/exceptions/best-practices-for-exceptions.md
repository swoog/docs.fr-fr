---
title: Bonnes pratiques pour les exceptions
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- exceptions, best practices
ms.assetid: f06da765-235b-427a-bfb6-47cd219af539
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dd38b59e39f938d6347457100243f09935444d88
ms.sourcegitcommit: e8dc507cfdaad504fc9d4c83d28d24569dcef91c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/03/2018
ms.locfileid: "33578078"
---
# <a name="best-practices-for-exceptions"></a><span data-ttu-id="e4c24-102">Bonnes pratiques pour les exceptions</span><span class="sxs-lookup"><span data-stu-id="e4c24-102">Best practices for exceptions</span></span>

<span data-ttu-id="e4c24-103">Une application bien conçue gère les exceptions et les erreurs pour empêcher les incidents d'applications.</span><span class="sxs-lookup"><span data-stu-id="e4c24-103">A well-designed app handles exceptions and errors to prevent app crashes.</span></span> <span data-ttu-id="e4c24-104">Cette section présente les bonnes pratiques pour la gestion et la création des exceptions.</span><span class="sxs-lookup"><span data-stu-id="e4c24-104">This section describes best practices for handling and creating exceptions.</span></span>

## <a name="use-trycatchfinally-blocks"></a><span data-ttu-id="e4c24-105">Utiliser des blocs try/catch/finally</span><span class="sxs-lookup"><span data-stu-id="e4c24-105">Use try/catch/finally blocks</span></span>

<span data-ttu-id="e4c24-106">Utilisez des blocs `try`/`catch`/`finally` autour du code susceptible de générer une exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-106">Use `try`/`catch`/`finally` blocks around code that can potentially generate an exception.</span></span> 

<span data-ttu-id="e4c24-107">Dans les blocs `catch`, veillez à toujours classer les exceptions de la plus spécifique à la moins spécifique.</span><span class="sxs-lookup"><span data-stu-id="e4c24-107">In `catch` blocks, always order exceptions from the most specific to the least specific.</span></span>

<span data-ttu-id="e4c24-108">Utilisez un bloc `finally` pour nettoyer les ressources, que la récupération soit possible ou non.</span><span class="sxs-lookup"><span data-stu-id="e4c24-108">Use a `finally` block to clean up resources, whether you can recover or not.</span></span>

## <a name="handle-common-conditions-without-throwing-exceptions"></a><span data-ttu-id="e4c24-109">Gérer les conditions courantes sans lever d’exception</span><span class="sxs-lookup"><span data-stu-id="e4c24-109">Handle common conditions without throwing exceptions</span></span>

<span data-ttu-id="e4c24-110">En ce qui concerne les conditions susceptibles de se produire, mais pouvant déclencher une exception, gérez-les de façon à éviter l’exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-110">For conditions that are likely to occur but might trigger an exception, consider handling them in a way that will avoid the exception.</span></span> <span data-ttu-id="e4c24-111">Par exemple, si vous essayez de fermer une connexion déjà fermée, vous obtenez une exception `InvalidOperationException`.</span><span class="sxs-lookup"><span data-stu-id="e4c24-111">For example, if you try to close a connection that is already closed, you'll get an `InvalidOperationException`.</span></span> <span data-ttu-id="e4c24-112">Vous pouvez l’éviter avec une instruction `if` qui permet de vérifier l’état de la connexion avant d’essayer de la fermer.</span><span class="sxs-lookup"><span data-stu-id="e4c24-112">You can avoid that by using an `if` statement to check the connection state before trying to close it.</span></span>

[!code-cpp[Conceptual.Exception.Handling#2](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.exception.handling/cpp/source.cpp#2)]
[!code-csharp[Conceptual.Exception.Handling#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.exception.handling/cs/source.cs#2)]
[!code-vb[Conceptual.Exception.Handling#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.exception.handling/vb/source.vb#2)]  

<span data-ttu-id="e4c24-113">Si vous ne vérifiez pas l’état de la connexion avant de la fermer, vous pouvez intercepter l’exception `InvalidOperationException`.</span><span class="sxs-lookup"><span data-stu-id="e4c24-113">If you don't check connection state before closing, you can catch the `InvalidOperationException` exception.</span></span>

[!code-cpp[Conceptual.Exception.Handling#3](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.exception.handling/cpp/source.cpp#3)]
[!code-csharp[Conceptual.Exception.Handling#3](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.exception.handling/cs/source.cs#3)]
[!code-vb[Conceptual.Exception.Handling#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.exception.handling/vb/source.vb#3)]  

<span data-ttu-id="e4c24-114">Le choix de la méthode dépend de la fréquence à laquelle l’événement doit se produire.</span><span class="sxs-lookup"><span data-stu-id="e4c24-114">The method to choose depends on how often you expect the event to occur.</span></span>

- <span data-ttu-id="e4c24-115">Utilisez la gestion des exceptions si l'événement ne se produit pas très souvent, c'est-à-dire, si l'événement est véritablement exceptionnel et indique une erreur (telle qu'une fin de fichier inattendue).</span><span class="sxs-lookup"><span data-stu-id="e4c24-115">Use exception handling if the event doesn't occur very often, that is, if the event is truly exceptional and indicates an error (such as an unexpected end-of-file).</span></span> <span data-ttu-id="e4c24-116">Lorsque vous utilisez la gestion des exceptions, la quantité de code exécutée en situation normale est moindre.</span><span class="sxs-lookup"><span data-stu-id="e4c24-116">When you use exception handling, less code is executed in normal conditions.</span></span>

- <span data-ttu-id="e4c24-117">Recherchez les conditions d’erreur dans le code si l’événement se produit régulièrement et peut être considéré comme faisant partie de l’exécution normale.</span><span class="sxs-lookup"><span data-stu-id="e4c24-117">Check for error conditions in code if the event happens routinely and could be considered part of normal execution.</span></span> <span data-ttu-id="e4c24-118">Quand vous recherchez les conditions d’erreur courantes, vous exécutez moins de code, car vous évitez les exceptions.</span><span class="sxs-lookup"><span data-stu-id="e4c24-118">When you check for common error conditions, less code is executed because you avoid exceptions.</span></span>

## <a name="design-classes-so-that-exceptions-can-be-avoided"></a><span data-ttu-id="e4c24-119">Concevoir des classes pour éviter les exceptions</span><span class="sxs-lookup"><span data-stu-id="e4c24-119">Design classes so that exceptions can be avoided</span></span>

<span data-ttu-id="e4c24-120">Une classe peut fournir des méthodes ou propriétés qui vous permettent d’éviter d’effectuer un appel susceptible de déclencher une exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-120">A class can provide methods or properties that enable you to avoid making a call that would trigger an exception.</span></span> <span data-ttu-id="e4c24-121">Par exemple, une classe <xref:System.IO.FileStream> fournit des méthodes qui permettent de déterminer si la fin du fichier a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="e4c24-121">For example, a <xref:System.IO.FileStream> class provides methods that help determine whether the end of the file has been reached.</span></span> <span data-ttu-id="e4c24-122">Ces méthodes peuvent servir à éviter l’exception qui est levée si vous dépassez la fin du fichier pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="e4c24-122">These can be used to avoid the exception that is thrown if you read past the end of the file.</span></span> <span data-ttu-id="e4c24-123">L’exemple suivant montre comment lire un fichier jusqu’à la fin sans lever d’exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-123">The following example shows how to read to the end of a file without triggering an exception.</span></span>

[!code-cpp[Conceptual.Exception.Handling#5](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.exception.handling/cpp/source.cpp#5)]
[!code-csharp[Conceptual.Exception.Handling#5](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.exception.handling/cs/source.cs#5)]
[!code-vb[Conceptual.Exception.Handling#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.exception.handling/vb/source.vb#5)]  

<span data-ttu-id="e4c24-124">Un autre moyen d’éviter les exceptions est de retourner Null pour les cas d’erreur très répandus au lieu de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-124">Another way to avoid exceptions is to return null for extremely common error cases instead of throwing an exception.</span></span> <span data-ttu-id="e4c24-125">Un cas d'erreur très répandu peut être considéré comme un flux de contrôle normal.</span><span class="sxs-lookup"><span data-stu-id="e4c24-125">An extremely common error case can be considered normal flow of control.</span></span> <span data-ttu-id="e4c24-126">En retournant null dans ces cas-là, vous réduisez l'impact sur les performances d'une application.</span><span class="sxs-lookup"><span data-stu-id="e4c24-126">By returning null in these cases, you minimize the performance impact to an app.</span></span>

## <a name="throw-exceptions-instead-of-returning-an-error-code"></a><span data-ttu-id="e4c24-127">Lever des exceptions au lieu de retourner un code d’erreur</span><span class="sxs-lookup"><span data-stu-id="e4c24-127">Throw exceptions instead of returning an error code</span></span>

<span data-ttu-id="e4c24-128">Les exceptions font en sorte que les échecs ne passent pas inaperçus parce que l’appel du code n’a pas vérifié le code de retour.</span><span class="sxs-lookup"><span data-stu-id="e4c24-128">Exceptions ensure that failures do not go unnoticed because calling code didn't check a return code.</span></span> 

## <a name="use-the-predefined-net-exception-types"></a><span data-ttu-id="e4c24-129">Utiliser les types d’exception .NET prédéfinis</span><span class="sxs-lookup"><span data-stu-id="e4c24-129">Use the predefined .NET exception types</span></span>

<span data-ttu-id="e4c24-130">N'introduisez une nouvelle classe d'exception que quand aucune classe d'exception prédéfinie ne s'applique.</span><span class="sxs-lookup"><span data-stu-id="e4c24-130">Introduce a new exception class only when a predefined one doesn't apply.</span></span> <span data-ttu-id="e4c24-131">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e4c24-131">For example:</span></span>

- <span data-ttu-id="e4c24-132">Levez une exception <xref:System.InvalidOperationException> si un appel de jeu de propriétés ou de méthode n'est pas approprié étant donné l'état actuel de l'objet.</span><span class="sxs-lookup"><span data-stu-id="e4c24-132">Throw an <xref:System.InvalidOperationException> exception if a property set or method call is not appropriate given the object's current state.</span></span>

- <span data-ttu-id="e4c24-133">Levez une exception <xref:System.ArgumentException> ou l’une des classes prédéfinies qui dérivent de <xref:System.ArgumentException> si des paramètres non valides sont passés.</span><span class="sxs-lookup"><span data-stu-id="e4c24-133">Throw an <xref:System.ArgumentException> exception or one of the predefined classes that derive from <xref:System.ArgumentException> if invalid parameters are passed.</span></span>

## <a name="end-exception-class-names-with-the-word-exception"></a><span data-ttu-id="e4c24-134">Terminer les noms de classes d’exception par le mot `Exception`</span><span class="sxs-lookup"><span data-stu-id="e4c24-134">End exception class names with the word `Exception`</span></span>

<span data-ttu-id="e4c24-135">Quand une exception personnalisée est nécessaire, nommez-la de manière appropriée et dérivez-la de la classe <xref:System.Exception>.</span><span class="sxs-lookup"><span data-stu-id="e4c24-135">When a custom exception is necessary, name it appropriately and derive it from the <xref:System.Exception> class.</span></span> <span data-ttu-id="e4c24-136">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e4c24-136">For example:</span></span>

[!code-cpp[Conceptual.Exception.Handling#4](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.exception.handling/cpp/source.cpp#4)]
[!code-csharp[Conceptual.Exception.Handling#4](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.exception.handling/cs/source.cs#4)]
[!code-vb[Conceptual.Exception.Handling#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.exception.handling/vb/source.vb#4)]  

## <a name="include-three-constructors-in-custom-exception-classes"></a><span data-ttu-id="e4c24-137">Inclure trois constructeurs dans des classes d’exception personnalisées</span><span class="sxs-lookup"><span data-stu-id="e4c24-137">Include three constructors in custom exception classes</span></span>

<span data-ttu-id="e4c24-138">Utilisez au moins les trois constructeurs communs pendant la création de vos propres classes d’exception : le constructeur par défaut, un constructeur qui prend un message de type chaîne et un constructeur qui prend un message de type chaîne et une exception interne.</span><span class="sxs-lookup"><span data-stu-id="e4c24-138">Use at least the three common constructors when creating your own exception classes: the default constructor, a constructor that takes a string message, and a constructor that takes a string message and an inner exception.</span></span>

* <span data-ttu-id="e4c24-139"><xref:System.Exception.%23ctor>, qui utilise les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4c24-139"><xref:System.Exception.%23ctor>, which uses default values.</span></span>
  
* <span data-ttu-id="e4c24-140"><xref:System.Exception.%23ctor%28System.String%29>, qui accepte un message de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="e4c24-140"><xref:System.Exception.%23ctor%28System.String%29>, which accepts a string message.</span></span>  
  
* <span data-ttu-id="e4c24-141"><xref:System.Exception.%23ctor%28System.String%2CSystem.Exception%29>, qui accepte un message de type chaîne et une exception interne.</span><span class="sxs-lookup"><span data-stu-id="e4c24-141"><xref:System.Exception.%23ctor%28System.String%2CSystem.Exception%29>, which accepts a string message and an inner exception.</span></span>  
  
<span data-ttu-id="e4c24-142">Pour obtenir un exemple, consultez [Guide pratique : créer des exceptions définies par l’utilisateur](how-to-create-user-defined-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="e4c24-142">For an example, see [How to: Create User-Defined Exceptions](how-to-create-user-defined-exceptions.md).</span></span>

## <a name="ensure-that-exception-data-is-available-when-code-executes-remotely"></a><span data-ttu-id="e4c24-143">Vérifier que les données d’exception sont disponibles quand le code s’exécute à distance</span><span class="sxs-lookup"><span data-stu-id="e4c24-143">Ensure that exception data is available when code executes remotely</span></span>

<span data-ttu-id="e4c24-144">Quand vous créez des exceptions définies par l’utilisateur, vous devez vérifier que les métadonnées des exceptions sont disponibles pour le code qui s’exécute à distance.</span><span class="sxs-lookup"><span data-stu-id="e4c24-144">When you create user-defined exceptions, ensure that the metadata for the exceptions is available to code that is executing remotely.</span></span> 

<span data-ttu-id="e4c24-145">Par exemple, sur les implémentations .NET qui prennent en charge des domaines d’application, des exceptions peuvent se produire entre domaines d’application.</span><span class="sxs-lookup"><span data-stu-id="e4c24-145">For example, on .NET implementations that support App Domains, exceptions may occur across App domains.</span></span> <span data-ttu-id="e4c24-146">Supposons que le domaine d’application A crée le domaine d’application B, lequel exécute du code qui lève une exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-146">Suppose App Domain A creates App Domain B, which executes code that throws an exception.</span></span> <span data-ttu-id="e4c24-147">Pour que le domaine d’application A intercepte et gère l’exception correctement, il doit pouvoir trouver l’assembly qui contient l’exception levée par le domaine d’application B. Si le domaine d’application B lève une exception qui est contenue dans un assembly sous sa base d’application, mais pas sous la base d’application du domaine d’application A, le domaine d’application A ne peut pas trouver l’exception et le Common Language Runtime lève une exception <xref:System.IO.FileNotFoundException>.</span><span class="sxs-lookup"><span data-stu-id="e4c24-147">For App Domain A to properly catch and handle the exception, it must be able to find the assembly that contains the exception thrown by App Domain B. If App Domain B throws an exception that is contained in an assembly under its application base, but not under App Domain A's application base, App Domain A will not be able to find the exception, and the common language runtime will throw a <xref:System.IO.FileNotFoundException> exception.</span></span> <span data-ttu-id="e4c24-148">Pour éviter cette situation, vous pouvez déployer l'assembly qui contient les informations sur les exceptions de deux façons :</span><span class="sxs-lookup"><span data-stu-id="e4c24-148">To avoid this situation, you can deploy the assembly that contains the exception information in two ways:</span></span>

- <span data-ttu-id="e4c24-149">Placez l'assembly dans une base d'application commune partagée par les deux domaines d'application.</span><span class="sxs-lookup"><span data-stu-id="e4c24-149">Put the assembly into a common application base shared by both app domains.</span></span>

    <span data-ttu-id="e4c24-150">\- ou -</span><span class="sxs-lookup"><span data-stu-id="e4c24-150">\- or -</span></span>

- <span data-ttu-id="e4c24-151">Si les domaines ne partagent pas une base d'application commune, signez l'assembly qui contient les informations sur les exceptions à l'aide d'un nom fort et déployez l'assembly dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="e4c24-151">If the domains do not share a common application base, sign the assembly that contains the exception information with a strong name and deploy the assembly into the global assembly cache.</span></span>

## <a name="use-grammatically-correct-error-messages"></a><span data-ttu-id="e4c24-152">Utiliser des messages d’erreur grammaticalement corrects</span><span class="sxs-lookup"><span data-stu-id="e4c24-152">Use grammatically correct error messages</span></span>

<span data-ttu-id="e4c24-153">Écrivez des phrases claires et insérez une ponctuation finale.</span><span class="sxs-lookup"><span data-stu-id="e4c24-153">Write clear sentences and include ending punctuation.</span></span> <span data-ttu-id="e4c24-154">Chaque phrase de la chaîne affectée à la propriété <xref:System.Exception.Message?displayProperty=nameWithType> doit se terminer par un point.</span><span class="sxs-lookup"><span data-stu-id="e4c24-154">Each sentence in the string assigned to the <xref:System.Exception.Message?displayProperty=nameWithType> property should end in a period.</span></span> <span data-ttu-id="e4c24-155">Par exemple, « La table du journal a débordé. »</span><span class="sxs-lookup"><span data-stu-id="e4c24-155">For example, "The log table has overflowed."</span></span> <span data-ttu-id="e4c24-156">est une chaîne de message appropriée.</span><span class="sxs-lookup"><span data-stu-id="e4c24-156">would be an appropriate message string.</span></span>

## <a name="include-a-localized-string-message-in-every-exception"></a><span data-ttu-id="e4c24-157">Inclure une chaîne de message localisée dans chaque exception</span><span class="sxs-lookup"><span data-stu-id="e4c24-157">Include a localized string message in every exception</span></span>

<span data-ttu-id="e4c24-158">Le message d’erreur que l’utilisateur voit est dérivé de la propriété <xref:System.Exception.Message?displayProperty=nameWithType> de l’exception qui a été levée, et non pas du nom de la classe d’exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-158">The error message that the user sees is derived from the <xref:System.Exception.Message?displayProperty=nameWithType> property of the exception that was thrown, and not from the name of the exception class.</span></span> <span data-ttu-id="e4c24-159">En règle générale, vous affectez une valeur à la propriété <xref:System.Exception.Message?displayProperty=nameWithType> en passant la chaîne de message à l’argument `message` d’un [constructeur d’exception](xref:System.Exception.%23ctor%2A).</span><span class="sxs-lookup"><span data-stu-id="e4c24-159">Typically, you assign a value to the <xref:System.Exception.Message?displayProperty=nameWithType>  property by passing the message string to the `message` argument of an [Exception constructor](xref:System.Exception.%23ctor%2A).</span></span> 

<span data-ttu-id="e4c24-160">Pour les applications localisées, vous devez fournir une chaîne de message localisée pour chaque exception que votre application peut lever.</span><span class="sxs-lookup"><span data-stu-id="e4c24-160">For localized applications, you should provide a localized message string for every exception that your application can throw.</span></span> <span data-ttu-id="e4c24-161">Vous utilisez des fichiers de ressources pour fournir les messages d’erreur localisés.</span><span class="sxs-lookup"><span data-stu-id="e4c24-161">You use resource files to provide localized error messages.</span></span> <span data-ttu-id="e4c24-162">Pour plus d’informations sur la localisation d’applications et la récupération des chaînes localisées, consultez [Ressources dans les applications pour poste de travail](../../framework/resources/index.md) et <xref:System.Resources.ResourceManager?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="e4c24-162">For information on localizing applications and retrieving localized strings, see [Resources in Desktop Apps](../../framework/resources/index.md) and <xref:System.Resources.ResourceManager?displayProperty=nameWithType>.</span></span>

## <a name="in-custom-exceptions-provide-additional-properties-as-needed"></a><span data-ttu-id="e4c24-163">Dans les exceptions personnalisées, fournir des propriétés supplémentaires si nécessaire</span><span class="sxs-lookup"><span data-stu-id="e4c24-163">In custom exceptions, provide additional properties as needed</span></span>

<span data-ttu-id="e4c24-164">Spécifiez des propriétés supplémentaires (en plus de la chaîne de message personnalisée) pour une exception seulement dans le cas d’un scénario du programme où les informations supplémentaires sont utiles.</span><span class="sxs-lookup"><span data-stu-id="e4c24-164">Provide additional properties for an exception (in addition to the custom message string) only when there's a programmatic scenario where the additional information is useful.</span></span> <span data-ttu-id="e4c24-165">Par exemple, la classe <xref:System.IO.FileNotFoundException> fournit la propriété <xref:System.IO.FileNotFoundException.FileName>.</span><span class="sxs-lookup"><span data-stu-id="e4c24-165">For example, the <xref:System.IO.FileNotFoundException> provides the <xref:System.IO.FileNotFoundException.FileName> property.</span></span>

## <a name="place-throw-statements-so-that-the-stack-trace-will-be-helpful"></a><span data-ttu-id="e4c24-166">Placer des instructions throw pour que la trace de la pile soit utile</span><span class="sxs-lookup"><span data-stu-id="e4c24-166">Place throw statements so that the stack trace will be helpful</span></span>

<span data-ttu-id="e4c24-167">La trace de la pile commence à l'instruction où l'exception est levée et se termine à l'instruction `catch` qui intercepte l'exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-167">The stack trace begins at the statement where the exception is thrown and ends at the `catch` statement that catches the exception.</span></span>

## <a name="use-exception-builder-methods"></a><span data-ttu-id="e4c24-168">Utiliser des méthodes de générateur d’exceptions</span><span class="sxs-lookup"><span data-stu-id="e4c24-168">Use exception builder methods</span></span>

<span data-ttu-id="e4c24-169">Il est fréquent qu'une classe lève la même exception à partir de différents endroits de son implémentation.</span><span class="sxs-lookup"><span data-stu-id="e4c24-169">It is common for a class to throw the same exception from different places in its implementation.</span></span> <span data-ttu-id="e4c24-170">Pour éviter un excès de code, utilisez des méthodes d'assistance qui créent une exception et la retournent.</span><span class="sxs-lookup"><span data-stu-id="e4c24-170">To avoid excessive code, use helper methods that create the exception and return it.</span></span> <span data-ttu-id="e4c24-171">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e4c24-171">For example:</span></span>

[!code-cpp[Conceptual.Exception.Handling#6](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.exception.handling/cpp/source.cpp#6)]
[!code-csharp[Conceptual.Exception.Handling#6](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.exception.handling/cs/source.cs#6)]
[!code-vb[Conceptual.Exception.Handling#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.exception.handling/vb/source.vb#6)]  
  
<span data-ttu-id="e4c24-172">Dans certains cas, il est plus approprié d’utiliser le constructeur de l’exception pour générer l’exception.</span><span class="sxs-lookup"><span data-stu-id="e4c24-172">In some cases, it's more appropriate to use the exception's constructor to build the exception.</span></span> <span data-ttu-id="e4c24-173">Par exemple, une classe d’exception globale comme <xref:System.ArgumentException>.</span><span class="sxs-lookup"><span data-stu-id="e4c24-173">An example is a global exception class such as <xref:System.ArgumentException>.</span></span>

## <a name="clean-up-intermediate-results-when-throwing-an-exception"></a><span data-ttu-id="e4c24-174">Nettoyer les résultats intermédiaires quand vous levez une exception</span><span class="sxs-lookup"><span data-stu-id="e4c24-174">Clean up intermediate results when throwing an exception</span></span>

<span data-ttu-id="e4c24-175">Les appelants doivent supposer qu'il n'y a aucun effet secondaire quand une exception est levée à partir d'une méthode.</span><span class="sxs-lookup"><span data-stu-id="e4c24-175">Callers should be able to assume that there are no side effects when an exception is thrown from a method.</span></span> <span data-ttu-id="e4c24-176">Par exemple, si vous avez du code qui transfère de l’argent en le retirant d’un compte pour le déposer dans un autre, et qu’une exception est levée pendant l’exécution du transfert, vous ne voulez pas que le retrait reste en vigueur.</span><span class="sxs-lookup"><span data-stu-id="e4c24-176">For example, if you have code that transfers money by withdrawing from one account and depositing in another account, and an exception is thrown while executing the deposit, you don't want the withdrawal to remain in effect.</span></span>

```csharp
public void TransferFunds(Account from, Account to, decimal amount)
{
    from.Withdrawal(amount);
    // If the deposit fails, the withdrawal shouldn't remain in effect. 
    to.Deposit(amount);
}
```

<span data-ttu-id="e4c24-177">Pour gérer cette situation, vous pouvez intercepter toutes les exceptions levées par la transaction de dépôt et annuler le retrait.</span><span class="sxs-lookup"><span data-stu-id="e4c24-177">One way to handle this situation is to catch any exceptions thrown by the deposit transaction and roll back the withdrawal.</span></span>

```csharp
private static void TransferFunds(Account from, Account to, decimal amount)
{
    string withdrawalTrxID = from.Withdrawal(amount);
    try
    {
        to.Deposit(amount);
    }
    catch
    {
        from.RollbackTransaction(withdrawalTrxID);
        throw;
    }
}
```

<span data-ttu-id="e4c24-178">Cet exemple illustre l’utilisation de `throw` pour lever de nouveau l’exception d’origine, ce qui peut permettre aux appelants de voir plus facilement la véritable cause du problème sans avoir à examiner la propriété <xref:System.Exception.InnerException>.</span><span class="sxs-lookup"><span data-stu-id="e4c24-178">This example illustrates the use of `throw` to re-throw the original exception, which can make it easier for callers to see the real cause of the problem without having to examine the <xref:System.Exception.InnerException> property.</span></span> <span data-ttu-id="e4c24-179">Vous pouvez aussi lever une nouvelle exception et inclure l’exception d’origine comme exception interne :</span><span class="sxs-lookup"><span data-stu-id="e4c24-179">An alternative is to throw a new exception and include the original exception as the inner exception:</span></span>

```csharp
catch (Exception ex)
{
    from.RollbackTransaction(withdrawalTrxID);
    throw new Exception("Withdrawal failed", ex);
}
```

## <a name="see-also"></a><span data-ttu-id="e4c24-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4c24-180">See Also</span></span>  
[<span data-ttu-id="e4c24-181">Exceptions</span><span class="sxs-lookup"><span data-stu-id="e4c24-181">Exceptions</span></span>](index.md)
