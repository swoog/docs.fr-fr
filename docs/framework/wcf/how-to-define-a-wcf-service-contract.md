---
title: 'Tutoriel : Définir un contrat de service Windows Communication Foundation'
ms.date: 03/19/2019
helpviewer_keywords:
- service contracts [WCF], defining
dev_langs:
- CSharp
- VB
ms.assetid: 67bf05b7-1d08-4911-83b7-a45d0b036fc3
ms.openlocfilehash: a1908339460191fcb81d03d45c56dd57b2cf4c4e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61929348"
---
# <a name="tutorial-define-a-windows-communication-foundation-service-contract"></a><span data-ttu-id="d87e5-102">Tutoriel : Définir un contrat de service Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="d87e5-102">Tutorial: Define a Windows Communication Foundation service contract</span></span>

<span data-ttu-id="d87e5-103">Ce didacticiel décrit la première des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="d87e5-103">This tutorial describes the first of five tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="d87e5-104">Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="d87e5-104">For an overview of the tutorials, see [Tutorial: Get started with Windows Communication Foundation applications](getting-started-tutorial.md).</span></span>

<span data-ttu-id="d87e5-105">Lorsque vous créez un service WCF, votre première tâche consiste à définir un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="d87e5-105">When you create a WCF service, your first task is to define a service contract.</span></span> <span data-ttu-id="d87e5-106">Le contrat de service spécifie les opérations prises en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="d87e5-106">The service contract specifies what operations the service supports.</span></span> <span data-ttu-id="d87e5-107">Une opération peut être considérée comme une méthode de service Web.</span><span class="sxs-lookup"><span data-stu-id="d87e5-107">An operation can be thought of as a Web service method.</span></span> <span data-ttu-id="d87e5-108">Créer des contrats de service, vous devez définir un élément visuel C# ou de l’interface de Visual Basic (VB).</span><span class="sxs-lookup"><span data-stu-id="d87e5-108">You create service contracts by defining a Visual C# or Visual Basic (VB) interface.</span></span> <span data-ttu-id="d87e5-109">Une interface possède les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d87e5-109">An interface has the following characteristics:</span></span>

- <span data-ttu-id="d87e5-110">Chaque méthode dans l'interface correspond à une opération de service spécifique.</span><span class="sxs-lookup"><span data-stu-id="d87e5-110">Each method in the interface corresponds to a specific service operation.</span></span> 
- <span data-ttu-id="d87e5-111">Pour chaque interface, vous devez appliquer le <xref:System.ServiceModel.ServiceContractAttribute> attribut.</span><span class="sxs-lookup"><span data-stu-id="d87e5-111">For each interface, you must apply the <xref:System.ServiceModel.ServiceContractAttribute> attribute.</span></span>
- <span data-ttu-id="d87e5-112">Pour chaque opération/méthode, vous devez appliquer le <xref:System.ServiceModel.OperationContractAttribute> attribut.</span><span class="sxs-lookup"><span data-stu-id="d87e5-112">For each operation/method, you must apply the <xref:System.ServiceModel.OperationContractAttribute> attribute.</span></span> 

<span data-ttu-id="d87e5-113">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="d87e5-113">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="d87e5-114">Créer un **bibliothèque du Service WCF** projet.</span><span class="sxs-lookup"><span data-stu-id="d87e5-114">Create a **WCF Service Library** project.</span></span>
> - <span data-ttu-id="d87e5-115">Définir une interface de contrat de service.</span><span class="sxs-lookup"><span data-stu-id="d87e5-115">Define a service contract interface.</span></span>

## <a name="create-a-wcf-service-library-project-and-define-a-service-contract-interface"></a><span data-ttu-id="d87e5-116">Créez un projet de bibliothèque du Service WCF et définir une interface de contrat de service</span><span class="sxs-lookup"><span data-stu-id="d87e5-116">Create a WCF Service Library project and define a service contract interface</span></span>

1. <span data-ttu-id="d87e5-117">Ouvrez Visual Studio en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d87e5-117">Open Visual Studio as an administrator.</span></span> <span data-ttu-id="d87e5-118">Pour ce faire, sélectionnez le programme Visual Studio dans le **Démarrer** menu, puis sélectionnez **plus** > **exécuter en tant qu’administrateur** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="d87e5-118">To do so, select the Visual Studio program in the **Start** menu, and then select **More** > **Run as administrator** from the shortcut menu.</span></span>

2. <span data-ttu-id="d87e5-119">Créer un **bibliothèque du Service WCF** projet.</span><span class="sxs-lookup"><span data-stu-id="d87e5-119">Create a **WCF Service Library** project.</span></span>

   1. <span data-ttu-id="d87e5-120">Dans le menu **Fichier**, sélectionnez **Nouveau** > **Projet**.</span><span class="sxs-lookup"><span data-stu-id="d87e5-120">From the **File** menu, select **New** > **Project**.</span></span>

   2. <span data-ttu-id="d87e5-121">Dans le **nouveau projet** boîte de dialogue, sur le côté gauche, développez **Visual C#** ou **Visual Basic**, puis sélectionnez le **WCF** catégorie.</span><span class="sxs-lookup"><span data-stu-id="d87e5-121">In the **New Project** dialog, on the left-hand side, expand **Visual C#** or **Visual Basic**, and then select the **WCF** category.</span></span> <span data-ttu-id="d87e5-122">Visual Studio affiche une liste des modèles de projet dans la section centrale de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d87e5-122">Visual Studio displays a list of project templates in the center section of the window.</span></span> <span data-ttu-id="d87e5-123">Sélectionnez **bibliothèque du Service WCF**.</span><span class="sxs-lookup"><span data-stu-id="d87e5-123">Select **WCF Service Library**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="d87e5-124">Si vous ne voyez pas le **WCF** catégorie du modèle de projet, vous devrez peut-être installer le **Windows Communication Foundation** composant de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d87e5-124">If you don't see the **WCF** project template category, you may need to install the **Windows Communication Foundation** component of Visual Studio.</span></span> <span data-ttu-id="d87e5-125">Dans le **nouveau projet** boîte de dialogue, sélectionnez le **ouvrir Visual Studio Installer** lien sur le côté gauche.</span><span class="sxs-lookup"><span data-stu-id="d87e5-125">In the **New Project** dialog box, select the **Open Visual Studio Installer** link on the left side.</span></span> <span data-ttu-id="d87e5-126">Sélectionnez le **composants individuels** sous l’onglet, puis recherchez et sélectionnez **Windows Communication Foundation** sous le **activités de développement** catégorie.</span><span class="sxs-lookup"><span data-stu-id="d87e5-126">Select the **Individual components** tab, and then find and select **Windows Communication Foundation** under the **Development activities** category.</span></span> <span data-ttu-id="d87e5-127">Choisissez **modifier** pour commencer l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="d87e5-127">Choose **Modify** to begin installing the component.</span></span>

   3. <span data-ttu-id="d87e5-128">Dans la section inférieure de la fenêtre, entrez *GettingStartedLib* pour le **nom** et *GettingStarted* pour le **nom de la Solution**.</span><span class="sxs-lookup"><span data-stu-id="d87e5-128">In the bottom section of the window, enter *GettingStartedLib* for the **Name** and *GettingStarted* for the **Solution name**.</span></span> 

   4. <span data-ttu-id="d87e5-129">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="d87e5-129">Select **OK**.</span></span>

      <span data-ttu-id="d87e5-130">Visual Studio crée le projet, qui comporte trois fichiers : *IService1.cs* (ou *IService1.vb* pour un projet Visual Basic), *Service1.cs* (ou *Service1.vb* pour un projet Visual Basic), et  *App.config*. Visual Studio définit ces fichiers comme suit :</span><span class="sxs-lookup"><span data-stu-id="d87e5-130">Visual Studio creates the project, which has three files: *IService1.cs* (or *IService1.vb* for a Visual Basic project), *Service1.cs* (or *Service1.vb* for a Visual Basic project), and *App.config*. Visual Studio defines these files as follows:</span></span> 
      - <span data-ttu-id="d87e5-131">Le *IService1* fichier contient la définition par défaut du contrat de service.</span><span class="sxs-lookup"><span data-stu-id="d87e5-131">The *IService1* file contains the default definition of the service contract.</span></span> 
      - <span data-ttu-id="d87e5-132">Le *Service1* fichier contient l’implémentation par défaut du contrat de service.</span><span class="sxs-lookup"><span data-stu-id="d87e5-132">The *Service1* file contains the default implementation of the service contract.</span></span> 
      - <span data-ttu-id="d87e5-133">Le *App.config* fichier contient les informations de configuration nécessaires pour charger le service par défaut avec l’outil hôte de Service WCF Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d87e5-133">The *App.config* file contains the configuration info needed to load the default service with the Visual Studio WCF Service Host tool.</span></span> <span data-ttu-id="d87e5-134">Pour plus d’informations sur l’outil hôte de Service WCF, consultez [hôte de Service WCF (WcfSvcHost.exe)](wcf-service-host-wcfsvchost-exe.md).</span><span class="sxs-lookup"><span data-stu-id="d87e5-134">For more information about the WCF Service Host tool, see [WCF Service Host (WcfSvcHost.exe)](wcf-service-host-wcfsvchost-exe.md).</span></span>

      > [!NOTE]
      > <span data-ttu-id="d87e5-135">Si vous avez installé Visual Studio avec des paramètres d’environnement de développement de Visual Basic, la solution peut être masquée.</span><span class="sxs-lookup"><span data-stu-id="d87e5-135">If you installed Visual Studio with Visual Basic developer environment settings, the solution might be hidden.</span></span> <span data-ttu-id="d87e5-136">Si c’est le cas, sélectionnez **Options** à partir de la **outils** menu, puis sélectionnez **projets et Solutions** > **général** dans le **Options** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d87e5-136">If this is the case, select **Options** from the **Tools** menu, then select **Projects and Solutions** > **General** in the **Options** window.</span></span> <span data-ttu-id="d87e5-137">Sélectionnez **toujours afficher la solution**.</span><span class="sxs-lookup"><span data-stu-id="d87e5-137">Select **Always show solution**.</span></span> <span data-ttu-id="d87e5-138">En outre, vérifiez que **enregistrer les nouveaux projets lors de la création** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d87e5-138">Also, verify that **Save new projects when created** is selected.</span></span>

3. <span data-ttu-id="d87e5-139">À partir de **l’Explorateur de solutions**, ouvrez le **IService1.cs** ou **IService1.vb** , puis remplacez son code avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d87e5-139">From **Solution Explorer**, open the **IService1.cs** or **IService1.vb** file, and replace its code with the following code:</span></span>

    ```csharp
    using System;
    using System.ServiceModel;

    namespace GettingStartedLib
    {
            [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
            public interface ICalculator
            {
                [OperationContract]
                double Add(double n1, double n2);
                [OperationContract]
                double Subtract(double n1, double n2);
                [OperationContract]
                double Multiply(double n1, double n2);
                [OperationContract]
                double Divide(double n1, double n2);
            }
    }
    ```

    ```vb
    Imports System.ServiceModel

    Namespace GettingStartedLib

        <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
        Public Interface ICalculator

            <OperationContract()> _
            Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
        End Interface
    End Namespace
    ```

     <span data-ttu-id="d87e5-140">Ce contrat définit une calculatrice en ligne.</span><span class="sxs-lookup"><span data-stu-id="d87e5-140">This contract defines an online calculator.</span></span> <span data-ttu-id="d87e5-141">Notez que le `ICalculator` interface est marquée avec le <xref:System.ServiceModel.ServiceContractAttribute> attribut (simplifiée comme `ServiceContract`).</span><span class="sxs-lookup"><span data-stu-id="d87e5-141">Notice the `ICalculator` interface is marked with the <xref:System.ServiceModel.ServiceContractAttribute> attribute (simplified as `ServiceContract`).</span></span> <span data-ttu-id="d87e5-142">Cet attribut définit un espace de noms pour lever l’ambiguïté du nom de contrat.</span><span class="sxs-lookup"><span data-stu-id="d87e5-142">This attribute defines a namespace to disambiguate the contract name.</span></span> <span data-ttu-id="d87e5-143">Le code marque chaque opération de calculatrice avec le <xref:System.ServiceModel.OperationContractAttribute> attribut (simplifiée comme `OperationContract`).</span><span class="sxs-lookup"><span data-stu-id="d87e5-143">The code marks each calculator operation with the <xref:System.ServiceModel.OperationContractAttribute> attribute (simplified as `OperationContract`).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d87e5-144">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d87e5-144">Next steps</span></span>

<span data-ttu-id="d87e5-145">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="d87e5-145">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="d87e5-146">Créez un projet bibliothèque du Service WCF.</span><span class="sxs-lookup"><span data-stu-id="d87e5-146">Create a WCF Service Library project.</span></span>
> - <span data-ttu-id="d87e5-147">Définir une interface de contrat de service.</span><span class="sxs-lookup"><span data-stu-id="d87e5-147">Define a service contract interface.</span></span>

<span data-ttu-id="d87e5-148">Passez au didacticiel suivant pour apprendre à implémenter le contrat de service WCF.</span><span class="sxs-lookup"><span data-stu-id="d87e5-148">Advance to the next tutorial to learn how to implement the WCF service contract.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d87e5-149">Tutoriel : Implémenter un contrat de service WCF</span><span class="sxs-lookup"><span data-stu-id="d87e5-149">Tutorial: Implement a WCF service contract</span></span>](how-to-implement-a-wcf-contract.md)
