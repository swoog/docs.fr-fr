---
title: Informations relatives à l’appelant (C#)
ms.date: 07/20/2015
ms.assetid: ffad3d24-2fb7-4641-9124-53b5bc91d339
ms.openlocfilehash: 048e91ad337f74ef04a2a03412a44a0be0ef9506
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45676387"
---
# <a name="caller-information-c"></a><span data-ttu-id="459aa-102">Informations relatives à l’appelant (C#)</span><span class="sxs-lookup"><span data-stu-id="459aa-102">Caller Information (C#)</span></span>
<span data-ttu-id="459aa-103">À l'aide des attributs d'informations de l'appelant, vous pouvez obtenir des informations sur l'appelant d'une méthode.</span><span class="sxs-lookup"><span data-stu-id="459aa-103">By using Caller Info attributes, you can obtain information about the caller to a method.</span></span> <span data-ttu-id="459aa-104">Vous pouvez obtenir le chemin d'accès du fichier de code source, le numéro de ligne dans le code source, puis le nom du membre de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="459aa-104">You can obtain file path of the source code, the line number in the source code, and the member name of the caller.</span></span> <span data-ttu-id="459aa-105">Ces informations sont utiles pour suivre, déboguer, et créer des outils de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="459aa-105">This information is helpful for tracing, debugging, and creating diagnostic tools.</span></span>  
  
 <span data-ttu-id="459aa-106">Pour obtenir ces informations, vous utilisez les attributs qui sont appliqués aux paramètres facultatifs, qui a une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="459aa-106">To obtain this information, you use attributes that are applied to optional parameters, each of which has a default value.</span></span> <span data-ttu-id="459aa-107">Le tableau suivant répertorie les attributs d'informations de l'appelant définis dans l'espace de noms <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> :</span><span class="sxs-lookup"><span data-stu-id="459aa-107">The following table lists the Caller Info attributes that are defined in the <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> namespace:</span></span>  
  
|<span data-ttu-id="459aa-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="459aa-108">Attribute</span></span>|<span data-ttu-id="459aa-109">Description</span><span class="sxs-lookup"><span data-stu-id="459aa-109">Description</span></span>|<span data-ttu-id="459aa-110">Type</span><span class="sxs-lookup"><span data-stu-id="459aa-110">Type</span></span>|  
|---|---|---|  
|<xref:System.Runtime.CompilerServices.CallerFilePathAttribute>|<span data-ttu-id="459aa-111">Chemin d’accès complet du fichier source qui contient l’appelant.</span><span class="sxs-lookup"><span data-stu-id="459aa-111">Full path of the source file that contains the caller.</span></span> <span data-ttu-id="459aa-112">C’est le chemin d’accès au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="459aa-112">This is the file path at compile time.</span></span>|`String`|  
|<xref:System.Runtime.CompilerServices.CallerLineNumberAttribute>|<span data-ttu-id="459aa-113">Numéro de ligne dans le fichier source dans lequel la méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="459aa-113">Line number in the source file at which the method is called.</span></span>|`Integer`|  
|<xref:System.Runtime.CompilerServices.CallerMemberNameAttribute>|<span data-ttu-id="459aa-114">Méthode ou nom de la propriété de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="459aa-114">Method or property name of the caller.</span></span> <span data-ttu-id="459aa-115">Consultez [Noms de membres](#MEMBERNAMES), plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="459aa-115">See [Member Names](#MEMBERNAMES) later in this topic.</span></span>|`String`|  
  
## <a name="example"></a><span data-ttu-id="459aa-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="459aa-116">Example</span></span>  
 <span data-ttu-id="459aa-117">L'exemple suivant indique comment utiliser des attributs d'informations de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="459aa-117">The following example shows how to use Caller Info attributes.</span></span> <span data-ttu-id="459aa-118">À chaque appel à la méthode `TraceMessage`, les informations d'appel sont remplacées par des arguments pour les paramètres optionnels.</span><span class="sxs-lookup"><span data-stu-id="459aa-118">On each call to the `TraceMessage` method, the caller information is substituted as arguments to the optional parameters.</span></span>  
  
```csharp  
public void DoProcessing()  
{  
    TraceMessage("Something happened.");  
}  
  
public void TraceMessage(string message,  
        [System.Runtime.CompilerServices.CallerMemberName] string memberName = "",  
        [System.Runtime.CompilerServices.CallerFilePath] string sourceFilePath = "",  
        [System.Runtime.CompilerServices.CallerLineNumber] int sourceLineNumber = 0)  
{  
    System.Diagnostics.Trace.WriteLine("message: " + message);  
    System.Diagnostics.Trace.WriteLine("member name: " + memberName);  
    System.Diagnostics.Trace.WriteLine("source file path: " + sourceFilePath);  
    System.Diagnostics.Trace.WriteLine("source line number: " + sourceLineNumber);  
}  
  
// Sample Output:  
//  message: Something happened.  
//  member name: DoProcessing  
//  source file path: c:\Users\username\Documents\Visual Studio 2012\Projects\CallerInfoCS\CallerInfoCS\Form1.cs  
//  source line number: 31  
```  
  
## <a name="remarks"></a><span data-ttu-id="459aa-119">Notes</span><span class="sxs-lookup"><span data-stu-id="459aa-119">Remarks</span></span>  
 <span data-ttu-id="459aa-120">Vous devez spécifier une valeur par défaut explicite pour chaque paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="459aa-120">You must specify an explicit default value for each optional parameter.</span></span> <span data-ttu-id="459aa-121">Vous ne pouvez pas appliquer des attributs d'informations de l'appelant aux paramètres qui ne sont pas spécifiés comme facultatifs.</span><span class="sxs-lookup"><span data-stu-id="459aa-121">You can't apply Caller Info attributes to parameters that aren't specified as optional.</span></span>  
  
 <span data-ttu-id="459aa-122">Les attributs d'informations de l'appelant ne rendent pas un paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="459aa-122">The Caller Info attributes don't make a parameter optional.</span></span> <span data-ttu-id="459aa-123">À la place, ils affectent la valeur par défaut qui est passée si l'argument est oublié.</span><span class="sxs-lookup"><span data-stu-id="459aa-123">Instead, they affect the default value that's passed in when the argument is omitted.</span></span>  
  
 <span data-ttu-id="459aa-124">Les valeurs d'informations de l'appelant sont émises en tant que littéraux en langage intermédiaire (IL) au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="459aa-124">Caller Info values are emitted as literals into the Intermediate Language (IL) at compile time.</span></span> <span data-ttu-id="459aa-125">Contrairement aux résultats de la propriété <xref:System.Exception.StackTrace%2A> pour les exceptions, les résultats ne sont pas affectés par l'obfuscation (protection de code).</span><span class="sxs-lookup"><span data-stu-id="459aa-125">Unlike the results of the <xref:System.Exception.StackTrace%2A> property for exceptions, the results aren't affected by obfuscation.</span></span>  
  
 <span data-ttu-id="459aa-126">Vous pouvez fournir explicitement les arguments facultatifs pour contrôler ou masquer des informations de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="459aa-126">You can explicitly supply the optional arguments to control the caller information or to hide caller information.</span></span>  
  
###  <a name="MEMBERNAMES"></a> <span data-ttu-id="459aa-127">Noms de membres</span><span class="sxs-lookup"><span data-stu-id="459aa-127">Member Names</span></span>  
 <span data-ttu-id="459aa-128">Vous pouvez utiliser l'attribut `CallerMemberName` pour éviter de spécifier le nom du membre comme argument de `String` à la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="459aa-128">You can use the `CallerMemberName` attribute to avoid specifying the member name as a `String` argument to the called method.</span></span> <span data-ttu-id="459aa-129">Vous évitez ainsi le problème que la **refactorisation de changement de nom** ne modifie pas les valeurs `String`.</span><span class="sxs-lookup"><span data-stu-id="459aa-129">By using this technique, you avoid the problem that **Rename Refactoring** doesn't change the `String` values.</span></span> <span data-ttu-id="459aa-130">Cet avantage est particulièrement utile pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="459aa-130">This benefit is especially useful for the following tasks:</span></span>  
  
-   <span data-ttu-id="459aa-131">Utilisation du traçage et des programmes de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="459aa-131">Using tracing and diagnostic routines.</span></span>  
  
-   <span data-ttu-id="459aa-132">Implémentation de l'interface <xref:System.ComponentModel.INotifyPropertyChanged> lors de la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="459aa-132">Implementing the <xref:System.ComponentModel.INotifyPropertyChanged> interface when binding data.</span></span> <span data-ttu-id="459aa-133">Cette interface permet à la propriété d'un objet de signaler à un contrôle dépendant que la propriété a été modifiée, afin que ce contrôle puisse afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="459aa-133">This interface allows the property of an object to notify a bound control that the property has changed, so that the control can display the updated information.</span></span> <span data-ttu-id="459aa-134">Sans attribut `CallerMemberName`, vous devez spécifier le nom de la propriété comme littéral.</span><span class="sxs-lookup"><span data-stu-id="459aa-134">Without the `CallerMemberName` attribute, you must specify the property name as a literal.</span></span>  
  
 <span data-ttu-id="459aa-135">Le graphique suivant affiche les noms des membres qui sont retournés lorsque vous utilisez l'attribut `CallerMemberName`.</span><span class="sxs-lookup"><span data-stu-id="459aa-135">The following chart shows the member names that are returned when you use the `CallerMemberName` attribute.</span></span>  
  
|<span data-ttu-id="459aa-136">Les appels se produisent à l'intérieur</span><span class="sxs-lookup"><span data-stu-id="459aa-136">Calls occurs within</span></span>|<span data-ttu-id="459aa-137">Résultat de nom de membre</span><span class="sxs-lookup"><span data-stu-id="459aa-137">Member name result</span></span>|  
|-------------------------|------------------------|  
|<span data-ttu-id="459aa-138">Méthode, propriété ou événement</span><span class="sxs-lookup"><span data-stu-id="459aa-138">Method, property, or event</span></span>|<span data-ttu-id="459aa-139">Le nom de la méthode, la propriété ou l'événement dont l'appel est originaire.</span><span class="sxs-lookup"><span data-stu-id="459aa-139">The name of the method, property, or event from which the call originated.</span></span>|  
|<span data-ttu-id="459aa-140">Constructeur</span><span class="sxs-lookup"><span data-stu-id="459aa-140">Constructor</span></span>|<span data-ttu-id="459aa-141">La chaîne « .ctor »</span><span class="sxs-lookup"><span data-stu-id="459aa-141">The string ".ctor"</span></span>|  
|<span data-ttu-id="459aa-142">Constructeur statique</span><span class="sxs-lookup"><span data-stu-id="459aa-142">Static constructor</span></span>|<span data-ttu-id="459aa-143">La chaîne « .cctor »</span><span class="sxs-lookup"><span data-stu-id="459aa-143">The string ".cctor"</span></span>|  
|<span data-ttu-id="459aa-144">Destructeur</span><span class="sxs-lookup"><span data-stu-id="459aa-144">Destructor</span></span>|<span data-ttu-id="459aa-145">La chaîne « finalize »</span><span class="sxs-lookup"><span data-stu-id="459aa-145">The string "Finalize"</span></span>|  
|<span data-ttu-id="459aa-146">Opérateurs définis par l'utilisateur ou conversions</span><span class="sxs-lookup"><span data-stu-id="459aa-146">User-defined operators or conversions</span></span>|<span data-ttu-id="459aa-147">Le nom généré pour le membre, par exemple, « op_Addition ».</span><span class="sxs-lookup"><span data-stu-id="459aa-147">The generated name for the member, for example, "op_Addition".</span></span>|  
|<span data-ttu-id="459aa-148">Constructeur d'attribut</span><span class="sxs-lookup"><span data-stu-id="459aa-148">Attribute constructor</span></span>|<span data-ttu-id="459aa-149">Le nom du membre auquel l'attribut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="459aa-149">The name of the member to which the attribute is applied.</span></span> <span data-ttu-id="459aa-150">Si l'attribut est un élément dans un membre (tel qu'un paramètre, une valeur de retour, ou un paramètre de type générique), le résultat est le nom du membre qui est associé à cet élément.</span><span class="sxs-lookup"><span data-stu-id="459aa-150">If the attribute is any element within a member (such as a parameter, a return value, or a generic type parameter), this result is the name of the member that's associated with that element.</span></span>|  
|<span data-ttu-id="459aa-151">Aucun membre contenant (par exemple, niveau assembly ou attributs qui sont appliqués aux types)</span><span class="sxs-lookup"><span data-stu-id="459aa-151">No containing member (for example, assembly-level or attributes that are applied to types)</span></span>|<span data-ttu-id="459aa-152">Valeur par défaut du paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="459aa-152">The default value of the optional parameter.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="459aa-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="459aa-153">See Also</span></span>

- [<span data-ttu-id="459aa-154">Attributs (C#)</span><span class="sxs-lookup"><span data-stu-id="459aa-154">Attributes (C#)</span></span>](../../../csharp/programming-guide/concepts/attributes/index.md)  
- [<span data-ttu-id="459aa-155">Attributs courants (C#)</span><span class="sxs-lookup"><span data-stu-id="459aa-155">Common Attributes (C#)</span></span>](../../../csharp/programming-guide/concepts/attributes/common-attributes.md)  
- [<span data-ttu-id="459aa-156">Arguments nommés et facultatifs</span><span class="sxs-lookup"><span data-stu-id="459aa-156">Named and Optional Arguments</span></span>](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)  
- [<span data-ttu-id="459aa-157">Concepts de programmation (C#)</span><span class="sxs-lookup"><span data-stu-id="459aa-157">Programming Concepts (C#)</span></span>](../../../csharp/programming-guide/concepts/index.md)
