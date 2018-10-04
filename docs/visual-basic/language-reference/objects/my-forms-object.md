---
title: My.Forms (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.Forms
- My.MyProject.Forms
helpviewer_keywords:
- My.Forms object
ms.assetid: f6bff4e6-6769-4294-956b-037aa6106d2a
ms.openlocfilehash: d15765b7673f321d4362ceea0adb73959a7e7726
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582656"
---
# <a name="myforms-object"></a><span data-ttu-id="6429b-102">My.Forms, objet</span><span class="sxs-lookup"><span data-stu-id="6429b-102">My.Forms Object</span></span>
<span data-ttu-id="6429b-103">Fournit des propriétés pour accéder à une instance de chaque formulaire Windows déclaré dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6429b-103">Provides properties for accessing an instance of each Windows form declared in the current project.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6429b-104">Notes</span><span class="sxs-lookup"><span data-stu-id="6429b-104">Remarks</span></span>  
 <span data-ttu-id="6429b-105">Le `My.Forms` objet fournit une instance de chaque formulaire dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6429b-105">The `My.Forms` object provides an instance of each form in the current project.</span></span> <span data-ttu-id="6429b-106">Le nom de la propriété est le même que le nom du formulaire qui accède à la propriété.</span><span class="sxs-lookup"><span data-stu-id="6429b-106">The name of the property is the same as the name of the form that the property accesses.</span></span>   
  
 <span data-ttu-id="6429b-107">Vous pouvez accéder à des formulaires fournis par le `My.Forms` objet en utilisant le nom du formulaire, sans qualification.</span><span class="sxs-lookup"><span data-stu-id="6429b-107">You can access the forms provided by the `My.Forms` object by using the name of the form, without qualification.</span></span> <span data-ttu-id="6429b-108">Étant donné que le nom de propriété est identique au nom de type du formulaire, cela vous permet d’accès à un formulaire comme s’il avait une instance par défaut.</span><span class="sxs-lookup"><span data-stu-id="6429b-108">Because the property name is the same as the form's type name, this allows you to access a form as if it had a default instance.</span></span> <span data-ttu-id="6429b-109">Par exemple, `My.Forms.Form1.Show` équivaut à `Form1.Show`.</span><span class="sxs-lookup"><span data-stu-id="6429b-109">For example, `My.Forms.Form1.Show` is equivalent to `Form1.Show`.</span></span>  
  
 <span data-ttu-id="6429b-110">Le `My.Forms` objet expose uniquement les formulaires associés au projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6429b-110">The `My.Forms` object exposes only the forms associated with the current project.</span></span> <span data-ttu-id="6429b-111">Il ne donne pas accès aux formulaires déclarés dans les DLL référencées.</span><span class="sxs-lookup"><span data-stu-id="6429b-111">It does not provide access to forms declared in referenced DLLs.</span></span> <span data-ttu-id="6429b-112">Pour accéder à un formulaire qui fournit une DLL, vous devez utiliser le nom qualifié du formulaire, écrit sous la forme *DllName*. *FormName*.</span><span class="sxs-lookup"><span data-stu-id="6429b-112">To access a form that a DLL provides, you must use the qualified name of the form, written as *DllName*.*FormName*.</span></span>  
  
 <span data-ttu-id="6429b-113">Vous pouvez utiliser le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A> propriété pour obtenir une collection de formulaires ouverts de toute l’application.</span><span class="sxs-lookup"><span data-stu-id="6429b-113">You can use the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A> property to get a collection of all the application's open forms.</span></span>  
  
 <span data-ttu-id="6429b-114">L’objet et ses propriétés sont disponibles uniquement pour les applications de Windows.</span><span class="sxs-lookup"><span data-stu-id="6429b-114">The object and its properties are available only for Windows applications.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6429b-115">Properties</span><span class="sxs-lookup"><span data-stu-id="6429b-115">Properties</span></span>  
 <span data-ttu-id="6429b-116">Chaque propriété de la `My.Forms` objet fournit l’accès à une instance d’un formulaire dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6429b-116">Each property of the `My.Forms` object provides access to an instance of a form in the current project.</span></span> <span data-ttu-id="6429b-117">Le nom de la propriété est le même que le nom du formulaire qui accède à la propriété et le type de propriété est identique au type du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6429b-117">The name of the property is the same as the name of the form that the property accesses, and the property type is the same as the form's type.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6429b-118">S’il existe un conflit de noms, le nom de propriété pour accéder à un formulaire est *RootNamespace*_*Namespace*\_*FormName*.</span><span class="sxs-lookup"><span data-stu-id="6429b-118">If there is a name collision, the property name to access a form is *RootNamespace*_*Namespace*\_*FormName*.</span></span> <span data-ttu-id="6429b-119">Par exemple, prenons deux formulaires nommés `Form1.`si une de ces formes est dans l’espace de noms racine `WindowsApplication1` et dans l’espace de noms `Namespace1`, vous accédez à ce formulaire via `My.Forms.WindowsApplication1_Namespace1_Form1`.</span><span class="sxs-lookup"><span data-stu-id="6429b-119">For example, consider two forms named `Form1.`If one of these forms is in the root namespace `WindowsApplication1` and in the namespace `Namespace1`, you would access that form through `My.Forms.WindowsApplication1_Namespace1_Form1`.</span></span>  
  
 <span data-ttu-id="6429b-120">Le `My.Forms` objet fournit l’accès à l’instance du formulaire principal de l’application qui a été créé au démarrage.</span><span class="sxs-lookup"><span data-stu-id="6429b-120">The `My.Forms` object provides access to the instance of the application's main form that was created on startup.</span></span> <span data-ttu-id="6429b-121">Pour toutes les autres formes, le `My.Forms` objet crée une nouvelle instance du formulaire lorsqu’il est accessible et qu’il stocke.</span><span class="sxs-lookup"><span data-stu-id="6429b-121">For all other forms, the `My.Forms` object creates a new instance of the form when it is accessed and stores it.</span></span> <span data-ttu-id="6429b-122">Les tentatives suivantes pour accéder à cette propriété retournent cette instance du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6429b-122">Subsequent attempts to access that property return that instance of the form.</span></span>  
  
 <span data-ttu-id="6429b-123">Vous pouvez supprimer un formulaire en assignant `Nothing` à la propriété pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="6429b-123">You can dispose of a form by assigning `Nothing` to the property for that form.</span></span> <span data-ttu-id="6429b-124">Les appels de méthode setter de propriété le <xref:System.Windows.Forms.Form.Close%2A> méthode du formulaire, puis assigne `Nothing` à la valeur stockée.</span><span class="sxs-lookup"><span data-stu-id="6429b-124">The property setter calls the <xref:System.Windows.Forms.Form.Close%2A> method of the form, and then assigns `Nothing` to the stored value.</span></span> <span data-ttu-id="6429b-125">Si vous assignez une valeur autre que `Nothing` à la propriété, l’accesseur Set lève une <xref:System.ArgumentException> exception.</span><span class="sxs-lookup"><span data-stu-id="6429b-125">If you assign any value other than `Nothing` to the property, the setter throws an <xref:System.ArgumentException> exception.</span></span>  
  
 <span data-ttu-id="6429b-126">Vous pouvez tester si une propriété de la `My.Forms` objet stocke une instance du formulaire à l’aide de la `Is` ou `IsNot` opérateur.</span><span class="sxs-lookup"><span data-stu-id="6429b-126">You can test whether a property of the `My.Forms` object stores an instance of the form by using the `Is` or `IsNot` operator.</span></span> <span data-ttu-id="6429b-127">Vous pouvez utiliser ces opérateurs pour vérifier si la valeur de la propriété est `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="6429b-127">You can use those operators to check if the value of the property is `Nothing`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6429b-128">En règle générale, le `Is` ou `IsNot` opérateur doit lire la valeur de la propriété pour effectuer la comparaison.</span><span class="sxs-lookup"><span data-stu-id="6429b-128">Typically, the `Is` or `IsNot` operator has to read the value of the property to perform the comparison.</span></span> <span data-ttu-id="6429b-129">Toutefois, si la propriété stocke actuellement `Nothing`, la propriété crée une nouvelle instance de la forme et puis la retourne.</span><span class="sxs-lookup"><span data-stu-id="6429b-129">However, if the property currently stores `Nothing`, the property creates a new instance of the form and then returns that instance.</span></span> <span data-ttu-id="6429b-130">Toutefois, le compilateur Visual Basic traite les propriétés de la `My.Forms` différemment de l’objet et permet la `Is` ou `IsNot` opérateur pour vérifier l’état de la propriété sans modifier sa valeur.</span><span class="sxs-lookup"><span data-stu-id="6429b-130">However, the Visual Basic compiler treats the properties of the `My.Forms` object differently and allows the `Is` or `IsNot` operator to check the status of the property without altering its value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6429b-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="6429b-131">Example</span></span>  
 <span data-ttu-id="6429b-132">Cet exemple modifie le titre de la valeur par défaut `SidebarMenu` formulaire.</span><span class="sxs-lookup"><span data-stu-id="6429b-132">This example changes the title of the default `SidebarMenu` form.</span></span>  
  
 [!code-vb[VbVbalrMyForms#2](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-forms-object_1.vb)]  
  
 <span data-ttu-id="6429b-133">Pour cet exemple fonctionne, votre projet doit avoir un formulaire nommé `SidebarMenu`.</span><span class="sxs-lookup"><span data-stu-id="6429b-133">For this example to work, your project must have a form named `SidebarMenu`.</span></span>  
  
 <span data-ttu-id="6429b-134">Ce code fonctionne uniquement dans un projet d’Application de Windows.</span><span class="sxs-lookup"><span data-stu-id="6429b-134">This code will work only in a Windows Application project.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6429b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6429b-135">Requirements</span></span>  
  
### <a name="availability-by-project-type"></a><span data-ttu-id="6429b-136">Disponibilité par Type de projet</span><span class="sxs-lookup"><span data-stu-id="6429b-136">Availability by Project Type</span></span>  
  
|<span data-ttu-id="6429b-137">Type de projet</span><span class="sxs-lookup"><span data-stu-id="6429b-137">Project type</span></span>|<span data-ttu-id="6429b-138">Disponible</span><span class="sxs-lookup"><span data-stu-id="6429b-138">Available</span></span>|  
|---|---|  
|<span data-ttu-id="6429b-139">Application Windows</span><span class="sxs-lookup"><span data-stu-id="6429b-139">Windows Application</span></span>|<span data-ttu-id="6429b-140">**Oui**</span><span class="sxs-lookup"><span data-stu-id="6429b-140">**Yes**</span></span>|  
|<span data-ttu-id="6429b-141">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="6429b-141">Class Library</span></span>|<span data-ttu-id="6429b-142">Non</span><span class="sxs-lookup"><span data-stu-id="6429b-142">No</span></span>|  
|<span data-ttu-id="6429b-143">Application console</span><span class="sxs-lookup"><span data-stu-id="6429b-143">Console Application</span></span>|<span data-ttu-id="6429b-144">Non</span><span class="sxs-lookup"><span data-stu-id="6429b-144">No</span></span>|  
|<span data-ttu-id="6429b-145">Bibliothèque de contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="6429b-145">Windows Control Library</span></span>|<span data-ttu-id="6429b-146">Non</span><span class="sxs-lookup"><span data-stu-id="6429b-146">No</span></span>|  
|<span data-ttu-id="6429b-147">Bibliothèque de contrôles Web</span><span class="sxs-lookup"><span data-stu-id="6429b-147">Web Control Library</span></span>|<span data-ttu-id="6429b-148">Non</span><span class="sxs-lookup"><span data-stu-id="6429b-148">No</span></span>|  
|<span data-ttu-id="6429b-149">Service Windows</span><span class="sxs-lookup"><span data-stu-id="6429b-149">Windows Service</span></span>|<span data-ttu-id="6429b-150">Non</span><span class="sxs-lookup"><span data-stu-id="6429b-150">No</span></span>|  
|<span data-ttu-id="6429b-151">Site web</span><span class="sxs-lookup"><span data-stu-id="6429b-151">Web Site</span></span>|<span data-ttu-id="6429b-152">Non</span><span class="sxs-lookup"><span data-stu-id="6429b-152">No</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6429b-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6429b-153">See Also</span></span>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A>  
 <xref:System.Windows.Forms.Form>  
 <xref:System.Windows.Forms.Form.Close%2A>  
 [<span data-ttu-id="6429b-154">Objects</span><span class="sxs-lookup"><span data-stu-id="6429b-154">Objects</span></span>](../../../visual-basic/language-reference/objects/index.md)  
 [<span data-ttu-id="6429b-155">Is (opérateur)</span><span class="sxs-lookup"><span data-stu-id="6429b-155">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)  
 [<span data-ttu-id="6429b-156">IsNot (opérateur)</span><span class="sxs-lookup"><span data-stu-id="6429b-156">IsNot Operator</span></span>](../../../visual-basic/language-reference/operators/isnot-operator.md)  
 [<span data-ttu-id="6429b-157">Accès aux formulaires de l’application</span><span class="sxs-lookup"><span data-stu-id="6429b-157">Accessing Application Forms</span></span>](../../../visual-basic/developing-apps/programming/accessing-application-forms.md)
