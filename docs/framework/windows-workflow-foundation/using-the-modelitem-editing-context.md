---
title: Utilisation du contexte d'édition ModelItem
ms.date: 03/30/2017
ms.assetid: 7f9f1ea5-0147-4079-8eca-be94f00d3aa1
ms.openlocfilehash: a2628bbbf2f6684e5d484b05cd5a2ac622f3b664
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59296876"
---
# <a name="using-the-modelitem-editing-context"></a><span data-ttu-id="33b09-102">Utilisation du contexte d'édition ModelItem</span><span class="sxs-lookup"><span data-stu-id="33b09-102">Using the ModelItem Editing Context</span></span>
<span data-ttu-id="33b09-103">Le contexte d'édition <xref:System.Activities.Presentation.Model.ModelItem> est l'objet que l'application hôte utilise pour communiquer avec le concepteur.</span><span class="sxs-lookup"><span data-stu-id="33b09-103">The <xref:System.Activities.Presentation.Model.ModelItem> editing context is the object that the host application uses to communicate with the designer.</span></span> <xref:System.Activities.Presentation.EditingContext> <span data-ttu-id="33b09-104">expose deux méthodes, <xref:System.Activities.Presentation.EditingContext.Items%2A> et <xref:System.Activities.Presentation.EditingContext.Services%2A>, qui peut être utilisé</span><span class="sxs-lookup"><span data-stu-id="33b09-104">exposes two methods, <xref:System.Activities.Presentation.EditingContext.Items%2A> and <xref:System.Activities.Presentation.EditingContext.Services%2A>, which can be used</span></span>  
  
## <a name="the-items-collection"></a><span data-ttu-id="33b09-105">La collection Items</span><span class="sxs-lookup"><span data-stu-id="33b09-105">The Items collection</span></span>  
 <span data-ttu-id="33b09-106">La collection <xref:System.Activities.Presentation.EditingContext.Items%2A> permet d'accéder aux données partagées entre l'hôte et le concepteur ou aux données disponibles pour tous les concepteurs.</span><span class="sxs-lookup"><span data-stu-id="33b09-106">The <xref:System.Activities.Presentation.EditingContext.Items%2A> collection is used to access data that is shared between the host and the designer, or data that is available to all designers.</span></span> <span data-ttu-id="33b09-107">Cette collection fournit les fonctionnalités suivantes, accessibles via la classe <xref:System.Activities.Presentation.ContextItemManager> :</span><span class="sxs-lookup"><span data-stu-id="33b09-107">This collection has the following capabilities, accessed via the <xref:System.Activities.Presentation.ContextItemManager> class:</span></span>  
  
1. <xref:System.Activities.Presentation.ContextItemManager.GetValue%2A>  
  
2. <xref:System.Activities.Presentation.ContextItemManager.Subscribe%2A>  
  
3. <xref:System.Activities.Presentation.ContextItemManager.Unsubscribe%2A>  
  
4. <xref:System.Activities.Presentation.ContextItemManager.SetValue%2A>  
  
## <a name="the-services-collection"></a><span data-ttu-id="33b09-108">La collection Services</span><span class="sxs-lookup"><span data-stu-id="33b09-108">The Services collection</span></span>  
 <span data-ttu-id="33b09-109">La collection <xref:System.Activities.Presentation.EditingContext.Services%2A> permet d’accéder aux services que le concepteur utilise pour interagir avec l’hôte ou aux services que les concepteurs utilisent.</span><span class="sxs-lookup"><span data-stu-id="33b09-109">The <xref:System.Activities.Presentation.EditingContext.Services%2A> collection is used to access services that the designer uses to interact with the host, or services that all designers use.</span></span> <span data-ttu-id="33b09-110">Cette collection présente les méthodes de références suivantes :</span><span class="sxs-lookup"><span data-stu-id="33b09-110">This collection has the following methods of note:</span></span>  
  
1. <xref:System.Activities.Presentation.ServiceManager.Publish%2A>  
  
2. <xref:System.Activities.Presentation.ServiceManager.Subscribe%2A>  
  
3. <xref:System.Activities.Presentation.ServiceManager.Unsubscribe%2A>  
  
4. <xref:System.Activities.Presentation.ServiceManager.GetService%2A>  
  
## <a name="assigning-a-designer-an-activity"></a><span data-ttu-id="33b09-111">Assignation d'une activité à un concepteur</span><span class="sxs-lookup"><span data-stu-id="33b09-111">Assigning a designer an activity</span></span>  
 <span data-ttu-id="33b09-112">L'attribut Designer permet de spécifier le concepteur utilisé par une activité.</span><span class="sxs-lookup"><span data-stu-id="33b09-112">To specify which designer an activity uses, the Designer attribute is used.</span></span>  
  
```  
[Designer(typeof(MyClassDesigner))]  
public sealed class MyClass : CodeActivity  
{  
```  
  
## <a name="creating-a-service"></a><span data-ttu-id="33b09-113">Création d'un service</span><span class="sxs-lookup"><span data-stu-id="33b09-113">Creating a service</span></span>  
 <span data-ttu-id="33b09-114">Pour créer un service servant de canal de transmission des informations entre le concepteur et l'hôte, une interface et une implémentation doivent être créées.</span><span class="sxs-lookup"><span data-stu-id="33b09-114">To create a service that serves as a conduit of information between the designer and the host, an interface and an implementation must be created.</span></span> <span data-ttu-id="33b09-115">L'interface est utilisée par la méthode <xref:System.Activities.Presentation.ServiceManager.Publish%2A> pour définir les membres du service et l'implémentation contient la logique du service.</span><span class="sxs-lookup"><span data-stu-id="33b09-115">The interface is used by the <xref:System.Activities.Presentation.ServiceManager.Publish%2A> method to define the members of the service, and the implementation contains the logic for the service.</span></span> <span data-ttu-id="33b09-116">Dans l'exemple de code suivant, une interface et une implémentation de service sont créées.</span><span class="sxs-lookup"><span data-stu-id="33b09-116">In the following code example, a service interface and implementation are created.</span></span>  
  
```  
public interface IMyService  
    {  
        IEnumerable<string> GetValues(string DisplayName);  
    }  
  
    public class MyServiceImpl : IMyService  
    {  
        public IEnumerable<string> GetValues(string DisplayName)  
        {  
            return new string[]  {   
                DisplayName + " One",   
                DisplayName + " Two",  
                "Three " + DisplayName  
            } ;  
        }  
    }  
```  
  
## <a name="publishing-a-service"></a><span data-ttu-id="33b09-117">Publication d'un service</span><span class="sxs-lookup"><span data-stu-id="33b09-117">Publishing a service</span></span>  
 <span data-ttu-id="33b09-118">Pour qu'un concepteur puisse consommer un service, il doit d'abord être publié par l'hôte à l'aide de la méthode <xref:System.Activities.Presentation.ServiceManager.Publish%2A>.</span><span class="sxs-lookup"><span data-stu-id="33b09-118">For a designer to consume a service, it must first be published by the host using the <xref:System.Activities.Presentation.ServiceManager.Publish%2A> method.</span></span>  
  
```  
this.Context.Services.Publish<IMyService>(new MyServiceImpl);  
```  
  
## <a name="subscribing-to-a-service"></a><span data-ttu-id="33b09-119">Abonnement à un service</span><span class="sxs-lookup"><span data-stu-id="33b09-119">Subscribing to a service</span></span>  
 <span data-ttu-id="33b09-120">Le concepteur obtient l'accès au service à l'aide de la méthode <xref:System.Activities.Presentation.ServiceManager.Subscribe%2A> dans la méthode <xref:System.Activities.Presentation.WorkflowViewElement.OnModelItemChanged%2A>.</span><span class="sxs-lookup"><span data-stu-id="33b09-120">The designer obtains access to the service using the <xref:System.Activities.Presentation.ServiceManager.Subscribe%2A> method in the <xref:System.Activities.Presentation.WorkflowViewElement.OnModelItemChanged%2A> method.</span></span> <span data-ttu-id="33b09-121">L'extrait de code suivant montre comment s'abonner à un service.</span><span class="sxs-lookup"><span data-stu-id="33b09-121">The following code snippet demonstrates how to subscribe to a service.</span></span>  
  
```  
protected override void OnModelItemChanged(object newItem)  
{  
    if (!subscribed)  
    {  
        this.Context.Services.Subscribe<IMyService>(  
            servInstance =>  
            {  
                listBox1.ItemsSource = servInstance.GetValues(this.ModelItem.Properties["DisplayName"].ComputedValue.ToString());  
            }  
            );  
        subscribed = true;   
    }  
}  
```  
  
## <a name="sharing-data-using-the-items-collection"></a><span data-ttu-id="33b09-122">Partage de données à l’aide de la collection Items</span><span class="sxs-lookup"><span data-stu-id="33b09-122">Sharing data using the Items collection</span></span>  
 <span data-ttu-id="33b09-123">L'utilisation de la collection Items est similaire à celle de la collection Services, à ceci près que <xref:System.Activities.Presentation.ContextItemManager.SetValue%2A> est utilisé à la place de Publish.</span><span class="sxs-lookup"><span data-stu-id="33b09-123">Using the Items collection is similar to using the Services collection, except that <xref:System.Activities.Presentation.ContextItemManager.SetValue%2A> is used instead of Publish.</span></span> <span data-ttu-id="33b09-124">Cette collection est plus appropriée pour le partage de données simples entre les concepteurs et l’hôte qu’une fonctionnalité complexe.</span><span class="sxs-lookup"><span data-stu-id="33b09-124">This collection is more appropriate for sharing simple data between the designers and the host, rather than complex functionality.</span></span>  
  
## <a name="editingcontext-host-items-and-services"></a><span data-ttu-id="33b09-125">Éléments et services de l'hôte EditingContext</span><span class="sxs-lookup"><span data-stu-id="33b09-125">EditingContext host items and services</span></span>  
 <span data-ttu-id="33b09-126">Le .NET Framework fournit un nombre d’éléments intégrés et de services accédés via le contexte d’édition.</span><span class="sxs-lookup"><span data-stu-id="33b09-126">The .NET Framework provides a number of built-in items and services accessed through the editing context.</span></span>  
  
 <span data-ttu-id="33b09-127">Éléments :</span><span class="sxs-lookup"><span data-stu-id="33b09-127">Items:</span></span>  
  
-   <xref:System.Activities.Presentation.Hosting.AssemblyContextControlItem><span data-ttu-id="33b09-128">: Gère la liste des assemblys locaux référencés qui seront utilisés dans le flux de travail pour les contrôles (par exemple, l’éditeur d’expressions).</span><span class="sxs-lookup"><span data-stu-id="33b09-128">: Manages the list of referenced local assemblies that will be used inside the workflow for controls (such as the expression editor).</span></span>  
  
-   <xref:System.Activities.Presentation.Hosting.ReadOnlyState><span data-ttu-id="33b09-129">: Indique si le concepteur est dans un état en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="33b09-129">: Indicates whether the designer is in a read-only state.</span></span>  
  
-   <xref:System.Activities.Presentation.View.Selection><span data-ttu-id="33b09-130">: Définit la collection d’objets qui sont actuellement sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="33b09-130">: Defines the collection of objects that are currently selected.</span></span>  
  
-   <xref:System.Activities.Presentation.Hosting.WorkflowCommandExtensionItem><span data-ttu-id="33b09-131">:</span><span class="sxs-lookup"><span data-stu-id="33b09-131">:</span></span>  
  
-   <xref:System.Activities.Presentation.WorkflowFileItem><span data-ttu-id="33b09-132">: Fournit des informations sur le fichier basé sur la session d’édition actuelle.</span><span class="sxs-lookup"><span data-stu-id="33b09-132">: Provides information on the file that the current editing session is based on.</span></span>  
  
 <span data-ttu-id="33b09-133">Services :</span><span class="sxs-lookup"><span data-stu-id="33b09-133">Services:</span></span>  
  
-   <xref:System.Activities.Presentation.Model.AttachedPropertiesService><span data-ttu-id="33b09-134">: Permet de propriétés à ajouter à l’instance actuelle, à l’aide de <xref:System.Activities.Presentation.Model.AttachedPropertiesService.AddProperty%2A>.</span><span class="sxs-lookup"><span data-stu-id="33b09-134">: Allows properties to be added to the current instance, using <xref:System.Activities.Presentation.Model.AttachedPropertiesService.AddProperty%2A>.</span></span>  
  
-   <xref:System.Activities.Presentation.View.DesignerView><span data-ttu-id="33b09-135">: Autorise l’accès aux propriétés de la zone de conception.</span><span class="sxs-lookup"><span data-stu-id="33b09-135">: Allows access to the properties of the designer canvas.</span></span>  
  
-   <xref:System.Activities.Presentation.IActivityToolboxService><span data-ttu-id="33b09-136">: Permet au contenu de la boîte à outils à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="33b09-136">: Allows the contents of the toolbox to be updated.</span></span>  
  
-   <xref:System.Activities.Presentation.Hosting.ICommandService><span data-ttu-id="33b09-137">: Utilisé pour intégrer des commandes du concepteur (par exemple, le Menu contextuel) avec des implémentations de service personnalisé fourni.</span><span class="sxs-lookup"><span data-stu-id="33b09-137">: Used to integrate designer commands (such as Context Menu) with custom-provided service implementations.</span></span>  
  
-   <xref:System.Activities.Presentation.Debug.IDesignerDebugView><span data-ttu-id="33b09-138">: Fournit des fonctionnalités du débogueur du concepteur.</span><span class="sxs-lookup"><span data-stu-id="33b09-138">: Provides functionality for the designer debugger.</span></span>  
  
-   <xref:System.Activities.Presentation.View.IExpressionEditorService><span data-ttu-id="33b09-139">: Fournit l’accès à la boîte de dialogue Éditeur d’expressions.</span><span class="sxs-lookup"><span data-stu-id="33b09-139">: Provides access to the Expression Editor dialog.</span></span>  
  
-   <xref:System.Activities.Presentation.IIntegratedHelpService><span data-ttu-id="33b09-140">: Fournit le concepteur avec une fonctionnalité d’aide.</span><span class="sxs-lookup"><span data-stu-id="33b09-140">: Provides the designer with integrated help functionality.</span></span>  
  
-   <xref:System.Activities.Presentation.Validation.IValidationErrorService><span data-ttu-id="33b09-141">: Fournit l’accès aux erreurs de validation à l’aide de <xref:System.Activities.Presentation.Validation.IValidationErrorService.ShowValidationErrors%2A>.</span><span class="sxs-lookup"><span data-stu-id="33b09-141">: Provides access to validation errors using <xref:System.Activities.Presentation.Validation.IValidationErrorService.ShowValidationErrors%2A>.</span></span>  
  
-   <xref:System.Activities.Presentation.IWorkflowDesignerStorageService><span data-ttu-id="33b09-142">: Fournit un service interne pour stocker et récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="33b09-142">: Provides an internal service to store and retrieve data.</span></span> <span data-ttu-id="33b09-143">Ce service est utilisé en interne par le .NET Framework et n’est pas destiné à un usage externe.</span><span class="sxs-lookup"><span data-stu-id="33b09-143">This service is used internally by the .NET Framework, and is not intended for external use.</span></span>  
  
-   <xref:System.Activities.Presentation.IXamlLoadErrorService><span data-ttu-id="33b09-144">: Fournit l’accès au XAML charge erreur collection en utilisant <xref:System.Activities.Presentation.IXamlLoadErrorService.ShowXamlLoadErrors%2A>.</span><span class="sxs-lookup"><span data-stu-id="33b09-144">: Provides access to the XAML load error collection using <xref:System.Activities.Presentation.IXamlLoadErrorService.ShowXamlLoadErrors%2A>.</span></span>  
  
-   <xref:System.Activities.Presentation.Services.ModelService><span data-ttu-id="33b09-145">: Utilisé par le concepteur pour interagir avec le modèle du flux de travail en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="33b09-145">: Used by the designer to interact with the model of the workflow being edited.</span></span>  
  
-   <xref:System.Activities.Presentation.Model.ModelTreeManager><span data-ttu-id="33b09-146">: Fournit l’accès à la racine de l’arborescence d’élément de modèle à l’aide <xref:System.Activities.Presentation.Model.ModelItem.Root%2A>.</span><span class="sxs-lookup"><span data-stu-id="33b09-146">: Provides access to the root of the model item tree using <xref:System.Activities.Presentation.Model.ModelItem.Root%2A>.</span></span>  
  
-   <xref:System.Activities.Presentation.UndoEngine><span data-ttu-id="33b09-147">: Fournit d’annulation et rétablissement des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="33b09-147">: Provides undo and redo functionality.</span></span>  
  
-   <xref:System.Activities.Presentation.Services.ViewService><span data-ttu-id="33b09-148">: Mappe les éléments visuels à des éléments de modèle sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="33b09-148">: Maps visual elements to underlying model items.</span></span>  
  
-   <xref:System.Activities.Presentation.View.ViewStateService><span data-ttu-id="33b09-149">: Stocke des États pour les éléments de modèle d’affichage.</span><span class="sxs-lookup"><span data-stu-id="33b09-149">: Stores view states for model items.</span></span>  
  
-   <xref:System.Activities.Presentation.View.VirtualizedContainerService><span data-ttu-id="33b09-150">: Utilisé pour personnaliser le comportement de l’interface utilisateur du conteneur virtuel.</span><span class="sxs-lookup"><span data-stu-id="33b09-150">: Used to customize the virtual container UI behavior.</span></span>  
  
-   <xref:System.Activities.Presentation.Hosting.WindowHelperService><span data-ttu-id="33b09-151">: Utilisé pour inscrire et désinscrire des délégués pour les notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="33b09-151">: Used to register and unregister delegates for event notifications.</span></span> <span data-ttu-id="33b09-152">Permet également de définir un propriétaire de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="33b09-152">Also allows a window owner to be set.</span></span>
