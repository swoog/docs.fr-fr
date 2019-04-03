---
title: Using, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.using
helpviewer_keywords:
- resource disposal
- Try...Catch...Finally statements, equivalent to Using statement
- resources [Visual Basic], disposing
- Using statement [Visual Basic]
ms.assetid: 665d1580-dd54-4e96-a9a9-6be2a68948f1
ms.openlocfilehash: fe53ea58dc98a4de793fe9dad1c3ceeac71622fc
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58843199"
---
# <a name="using-statement-visual-basic"></a><span data-ttu-id="a4e0c-102">Using, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a4e0c-102">Using Statement (Visual Basic)</span></span>
<span data-ttu-id="a4e0c-103">Déclare le début d’un `Using` bloquer et acquiert éventuellement les ressources système qui contrôle le bloc.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-103">Declares the beginning of a `Using` block and optionally acquires the system resources that the block controls.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4e0c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4e0c-104">Syntax</span></span>  
  
```  
Using { resourcelist | resourceexpression }  
    [ statements ]  
End Using  
```  
  
## <a name="parts"></a><span data-ttu-id="a4e0c-105">Composants</span><span class="sxs-lookup"><span data-stu-id="a4e0c-105">Parts</span></span>  
  
|<span data-ttu-id="a4e0c-106">Terme</span><span class="sxs-lookup"><span data-stu-id="a4e0c-106">Term</span></span>|<span data-ttu-id="a4e0c-107">Définition</span><span class="sxs-lookup"><span data-stu-id="a4e0c-107">Definition</span></span>|  
|---|---|  
|`resourcelist`|<span data-ttu-id="a4e0c-108">Requis si vous ne fournissez pas `resourceexpression`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-108">Required if you do not supply `resourceexpression`.</span></span> <span data-ttu-id="a4e0c-109">Liste d’une ou plusieurs ressources système que ce `Using` bloquer des contrôles, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-109">List of one or more system resources that this `Using` block controls, separated by commas.</span></span>|  
|`resourceexpression`|<span data-ttu-id="a4e0c-110">Requis si vous ne fournissez pas `resourcelist`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-110">Required if you do not supply `resourcelist`.</span></span> <span data-ttu-id="a4e0c-111">Variable de référence ou une expression faisant référence à une ressource système à être contrôlé par ce `Using` bloc.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-111">Reference variable or expression referring to a system resource to be controlled by this `Using` block.</span></span>|  
|`statements`|<span data-ttu-id="a4e0c-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-112">Optional.</span></span> <span data-ttu-id="a4e0c-113">Bloc d’instructions qui la `Using` bloquer s’exécute.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-113">Block of statements that the `Using` block runs.</span></span>|  
|`End Using`|<span data-ttu-id="a4e0c-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-114">Required.</span></span> <span data-ttu-id="a4e0c-115">Termine la définition de la `Using` bloc et supprime toutes les ressources qu’il contrôle.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-115">Terminates the definition of the `Using` block and disposes of all the resources that it controls.</span></span>|  
  
 <span data-ttu-id="a4e0c-116">Chaque ressource dans le `resourcelist` partie a la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4e0c-116">Each resource in the `resourcelist` part has the following syntax and parts:</span></span>  
  
 `resourcename As New resourcetype [ ( [ arglist ] ) ]`  
  
 <span data-ttu-id="a4e0c-117">- ou -</span><span class="sxs-lookup"><span data-stu-id="a4e0c-117">-or-</span></span>  
  
 `resourcename As resourcetype = resourceexpression`  
  
## <a name="resourcelist-parts"></a><span data-ttu-id="a4e0c-118">Éléments resourcelist</span><span class="sxs-lookup"><span data-stu-id="a4e0c-118">resourcelist Parts</span></span>  
  
|<span data-ttu-id="a4e0c-119">Terme</span><span class="sxs-lookup"><span data-stu-id="a4e0c-119">Term</span></span>|<span data-ttu-id="a4e0c-120">Définition</span><span class="sxs-lookup"><span data-stu-id="a4e0c-120">Definition</span></span>|  
|---|---|  
|`resourcename`|<span data-ttu-id="a4e0c-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-121">Required.</span></span> <span data-ttu-id="a4e0c-122">Variable de référence qui fait référence à une ressource système qui le `Using` bloquer les commandes.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-122">Reference variable that refers to a system resource that the `Using` block controls.</span></span>|  
|`New`|<span data-ttu-id="a4e0c-123">Obligatoire si le `Using` instruction acquiert la ressource.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-123">Required if the `Using` statement acquires the resource.</span></span> <span data-ttu-id="a4e0c-124">Si vous avez déjà acquis la ressource, utilisez la deuxième possibilité de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-124">If you have already acquired the resource, use the second syntax alternative.</span></span>|  
|`resourcetype`|<span data-ttu-id="a4e0c-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-125">Required.</span></span> <span data-ttu-id="a4e0c-126">La classe de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-126">The class of the resource.</span></span> <span data-ttu-id="a4e0c-127">La classe doit implémenter la <xref:System.IDisposable> interface.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-127">The class must implement the <xref:System.IDisposable> interface.</span></span>|  
|`arglist`|<span data-ttu-id="a4e0c-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-128">Optional.</span></span> <span data-ttu-id="a4e0c-129">Liste des arguments que vous passez au constructeur pour créer une instance de `resourcetype`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-129">List of arguments you are passing to the constructor to create an instance of `resourcetype`.</span></span> <span data-ttu-id="a4e0c-130">Consultez [liste de paramètres](../../../visual-basic/language-reference/statements/parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="a4e0c-130">See [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span></span>|  
|`resourceexpression`|<span data-ttu-id="a4e0c-131">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-131">Required.</span></span> <span data-ttu-id="a4e0c-132">Variable ou une expression faisant référence à une ressource système répondant aux exigences de `resourcetype`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-132">Variable or expression referring to a system resource satisfying the requirements of `resourcetype`.</span></span> <span data-ttu-id="a4e0c-133">Si vous utilisez la deuxième possibilité de syntaxe, vous devez acquérir la ressource avant de passer le contrôle à la `Using` instruction.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-133">If you use the second syntax alternative, you must acquire the resource before passing control to the `Using` statement.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a4e0c-134">Notes</span><span class="sxs-lookup"><span data-stu-id="a4e0c-134">Remarks</span></span>  
 <span data-ttu-id="a4e0c-135">Parfois, votre code requiert une ressource non managée, comme un descripteur de fichier, un wrapper COM ou une connexion SQL.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-135">Sometimes your code requires an unmanaged resource, such as a file handle, a COM wrapper, or a SQL connection.</span></span> <span data-ttu-id="a4e0c-136">Un `Using` bloc garantit la suppression d’un ou plusieurs de ces ressources lorsque votre code a fini avec eux.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-136">A `Using` block guarantees the disposal of one or more such resources when your code is finished with them.</span></span> <span data-ttu-id="a4e0c-137">Cela les rend disponibles pour tout autre code à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-137">This makes them available for other code to use.</span></span>  
  
 <span data-ttu-id="a4e0c-138">Ressources managées sont supprimées par le garbage collector (GC) du .NET Framework sans codage supplémentaire de votre part.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-138">Managed resources are disposed of by the .NET Framework garbage collector (GC) without any extra coding on your part.</span></span> <span data-ttu-id="a4e0c-139">Vous n’avez pas besoin un `Using` bloc pour les ressources managées.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-139">You do not need a `Using` block for managed resources.</span></span> <span data-ttu-id="a4e0c-140">Toutefois, vous pouvez toujours utiliser un `Using` bloc pour forcer la suppression d’une ressource managée au lieu d’attendre le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-140">However, you can still use a `Using` block to force the disposal of a managed resource instead of waiting for the garbage collector.</span></span>  
  
 <span data-ttu-id="a4e0c-141">Un `Using` bloc comprend trois parties : acquisition, de l’utilisation et de suppression.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-141">A `Using` block has three parts: acquisition, usage, and disposal.</span></span>  
  
-   <span data-ttu-id="a4e0c-142">*Acquisition* signifie que la création d’une variable et l’initialiser pour faire référence à la ressource du système.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-142">*Acquisition* means creating a variable and initializing it to refer to the system resource.</span></span> <span data-ttu-id="a4e0c-143">Le `Using` instruction peut acquérir une ou plusieurs ressources, ou vous pouvez acquérir exactement une ressource avant d’entrer dans le bloc et lui fournir à la `Using` instruction.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-143">The `Using` statement can acquire one or more resources, or you can acquire exactly one resource before entering the block and supply it to the `Using` statement.</span></span> <span data-ttu-id="a4e0c-144">Si vous fournissez `resourceexpression`, vous devez acquérir la ressource avant de passer le contrôle à la `Using` instruction.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-144">If you supply `resourceexpression`, you must acquire the resource before passing control to the `Using` statement.</span></span>  
  
-   <span data-ttu-id="a4e0c-145">*Utilisation* signifie que l’accès des ressources et d’exécuter des opérations.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-145">*Usage* means accessing the resources and performing actions with them.</span></span> <span data-ttu-id="a4e0c-146">Les instructions entre `Using` et `End Using` représentent l’utilisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-146">The statements between `Using` and `End Using` represent the usage of the resources.</span></span>  
  
-   <span data-ttu-id="a4e0c-147">*Élimination* signifie appeler le <xref:System.IDisposable.Dispose%2A> méthode sur l’objet dans `resourcename`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-147">*Disposal* means calling the <xref:System.IDisposable.Dispose%2A> method on the object in `resourcename`.</span></span> <span data-ttu-id="a4e0c-148">Cela permet à l’objet arrêter correctement ses ressources.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-148">This allows the object to cleanly terminate its resources.</span></span> <span data-ttu-id="a4e0c-149">Le `End Using` instruction supprime les ressources sous le `Using` contrôle du bloc.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-149">The `End Using` statement disposes of the resources under the `Using` block's control.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="a4e0c-150">Comportement</span><span class="sxs-lookup"><span data-stu-id="a4e0c-150">Behavior</span></span>  
 <span data-ttu-id="a4e0c-151">Un `Using` bloc se comporte comme un `Try`... `Finally` dans laquelle le `Try` bloc utilise les ressources et le `Finally` bloc supprime d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-151">A `Using` block behaves like a `Try`...`Finally` construction in which the `Try` block uses the resources and the `Finally` block disposes of them.</span></span> <span data-ttu-id="a4e0c-152">Pour cette raison, le `Using` bloc garantit l’élimination des ressources, quel que soit la manière dont vous quittez le bloc.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-152">Because of this, the `Using` block guarantees disposal of the resources, no matter how you exit the block.</span></span> <span data-ttu-id="a4e0c-153">Cela est vrai même en cas d’une exception non gérée, sauf pour un <xref:System.StackOverflowException>.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-153">This is true even in the case of an unhandled exception, except for a <xref:System.StackOverflowException>.</span></span>  
  
 <span data-ttu-id="a4e0c-154">La portée de chaque variable de ressource acquise par le `Using` instruction est limitée à la `Using` bloc.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-154">The scope of every resource variable acquired by the `Using` statement is limited to the `Using` block.</span></span>  
  
 <span data-ttu-id="a4e0c-155">Si vous spécifiez plusieurs ressources système dans le `Using` instruction, l’effet est le même que si vous imbriquez `Using` bloque une fois dans un autre.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-155">If you specify more than one system resource in the `Using` statement, the effect is the same as if you nested `Using` blocks one within another.</span></span>  
  
 <span data-ttu-id="a4e0c-156">Si `resourcename` est `Nothing`, aucun appel à <xref:System.IDisposable.Dispose%2A> est effectuée, et aucune exception n’est levée.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-156">If `resourcename` is `Nothing`, no call to <xref:System.IDisposable.Dispose%2A> is made, and no exception is thrown.</span></span>  
  
## <a name="structured-exception-handling-within-a-using-block"></a><span data-ttu-id="a4e0c-157">Structurée des exceptions dans un bloc à l’aide de</span><span class="sxs-lookup"><span data-stu-id="a4e0c-157">Structured Exception Handling Within a Using Block</span></span>  
 <span data-ttu-id="a4e0c-158">Si vous avez besoin gérer une exception qui peut-être se produire dans le `Using` bloc, vous pouvez ajouter un `Try`... `Finally` construction à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-158">If you need to handle an exception that might occur within the `Using` block, you can add a complete `Try`...`Finally` construction to it.</span></span> <span data-ttu-id="a4e0c-159">Si vous avez besoin gérer le cas où le `Using` instruction n’a pas réussie à acquérir une ressource, vous pouvez tester pour voir si `resourcename` est `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-159">If you need to handle the case where the `Using` statement is not successful in acquiring a resource, you can test to see if `resourcename` is `Nothing`.</span></span>  
  
## <a name="structured-exception-handling-instead-of-a-using-block"></a><span data-ttu-id="a4e0c-160">Structurée des exceptions au lieu d’un bloc à l’aide de</span><span class="sxs-lookup"><span data-stu-id="a4e0c-160">Structured Exception Handling Instead of a Using Block</span></span>  
 <span data-ttu-id="a4e0c-161">Si vous avez besoin d’un contrôle plus précis sur l’acquisition des ressources, ou si vous avez besoin de code supplémentaire dans le `Finally` bloc, vous pouvez réécrire la `Using` bloquer comme un `Try`... `Finally` construction.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-161">If you need finer control over the acquisition of the resources, or you need additional code in the `Finally` block, you can rewrite the `Using` block as a `Try`...`Finally` construction.</span></span> <span data-ttu-id="a4e0c-162">L’exemple suivant montre la structure `Try` et `Using` constructions qui sont équivalentes dans l’acquisition et l’élimination des `resource`.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-162">The following example shows skeleton `Try` and `Using` constructions that are equivalent in the acquisition and disposal of `resource`.</span></span>  
  
```vb  
Using resource As New resourceType   
    ' Insert code to work with resource.  
End Using  
  
' For the acquisition and disposal of resource, the following  
' Try construction is equivalent to the Using block.  
Dim resource As New resourceType  
Try   
    ' Insert code to work with resource.  
Finally   
    If resource IsNot Nothing Then  
        resource.Dispose()   
    End If  
End Try   
```  
  
> [!NOTE]
>  <span data-ttu-id="a4e0c-163">Le code à l’intérieur de la `Using` bloc ne doit pas affecter l’objet dans `resourcename` à une autre variable.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-163">The code inside the `Using` block should not assign the object in `resourcename` to another variable.</span></span> <span data-ttu-id="a4e0c-164">Lorsque vous quittez le `Using` bloc, la ressource est supprimée, et l’autre variable ne peut pas accéder à la ressource vers laquelle il pointe.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-164">When you exit the `Using` block, the resource is disposed, and the other variable cannot access the resource to which it points.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a4e0c-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="a4e0c-165">Example</span></span>  
 <span data-ttu-id="a4e0c-166">L’exemple suivant crée un fichier nommé log.txt et écrit deux lignes de texte dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-166">The following example creates a file that is named log.txt and writes two lines of text to the file.</span></span> <span data-ttu-id="a4e0c-167">L’exemple lit ce même fichier également et affiche les lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-167">The example also reads that same file and displays the lines of text.</span></span>  
  
 <span data-ttu-id="a4e0c-168">Étant donné que le <xref:System.IO.TextWriter> et <xref:System.IO.TextReader> classes implémentent le <xref:System.IDisposable> interface, le code peut utiliser `Using` instructions pour vous assurer que le fichier est correctement fermé lors de l’écriture et les opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="a4e0c-168">Because the <xref:System.IO.TextWriter> and <xref:System.IO.TextReader> classes implement the <xref:System.IDisposable> interface, the code can use `Using` statements to ensure that the file is correctly closed after the write and read operations.</span></span>  
  
 [!code-vb[VbVbalrStatements#50](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#50)]  
  
## <a name="see-also"></a><span data-ttu-id="a4e0c-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4e0c-169">See also</span></span>

- <xref:System.IDisposable>
- [<span data-ttu-id="a4e0c-170">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="a4e0c-170">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [<span data-ttu-id="a4e0c-171">Guide pratique pour Supprimer une ressource système</span><span class="sxs-lookup"><span data-stu-id="a4e0c-171">How to: Dispose of a System Resource</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/how-to-dispose-of-a-system-resource.md)
