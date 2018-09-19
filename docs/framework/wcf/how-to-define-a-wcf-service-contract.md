---
title: 'Comment : définir un contrat de service Windows Communication Foundation'
ms.date: 09/14/2018
helpviewer_keywords:
- service contracts [WCF], defining
dev_langs:
- CSharp
- VB
ms.assetid: 67bf05b7-1d08-4911-83b7-a45d0b036fc3
ms.openlocfilehash: 4f85a51c47eb045d1d2f0111cb217199c9acf0d7
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46009006"
---
# <a name="how-to-define-a-windows-communication-foundation-service-contract"></a><span data-ttu-id="8b611-102">Comment : définir un contrat de service Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="8b611-102">How to: Define a Windows Communication Foundation Service Contract</span></span>

<span data-ttu-id="8b611-103">Il s’agit de la première des six tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="8b611-103">This is the first of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="8b611-104">Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="8b611-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

 <span data-ttu-id="8b611-105">Lorsque vous créez un service WCF, la première tâche consiste à définir un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="8b611-105">When creating a WCF service, the first task is to define a service contract.</span></span> <span data-ttu-id="8b611-106">Le contrat de service spécifie les opérations prises en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="8b611-106">The service contract specifies what operations the service supports.</span></span> <span data-ttu-id="8b611-107">Une opération peut être considérée comme une méthode de service Web.</span><span class="sxs-lookup"><span data-stu-id="8b611-107">An operation can be thought of as a Web service method.</span></span> <span data-ttu-id="8b611-108">Les contrats sont créés en définissant une interface C++, C# ou Visual Basic (VB).</span><span class="sxs-lookup"><span data-stu-id="8b611-108">Contracts are created by defining a C++, C#, or Visual Basic (VB) interface.</span></span> <span data-ttu-id="8b611-109">Chaque méthode dans l'interface correspond à une opération de service spécifique.</span><span class="sxs-lookup"><span data-stu-id="8b611-109">Each method in the interface corresponds to a specific service operation.</span></span> <span data-ttu-id="8b611-110">Chaque interface doit avoir le <xref:System.ServiceModel.ServiceContractAttribute> qui s'applique à elle et chaque opération doit avoir l'attribut <xref:System.ServiceModel.OperationContractAttribute> qui s'applique à elle.</span><span class="sxs-lookup"><span data-stu-id="8b611-110">Each interface must have the <xref:System.ServiceModel.ServiceContractAttribute> applied to it and each operation must have the <xref:System.ServiceModel.OperationContractAttribute> attribute applied to it.</span></span> <span data-ttu-id="8b611-111">Si une méthode dans une interface qui a l'attribut <xref:System.ServiceModel.ServiceContractAttribute> n'a pas l'attribut <xref:System.ServiceModel.OperationContractAttribute>, cette méthode n'est pas exposée par le service.</span><span class="sxs-lookup"><span data-stu-id="8b611-111">If a method within an interface that has the <xref:System.ServiceModel.ServiceContractAttribute> attribute does not have the <xref:System.ServiceModel.OperationContractAttribute> attribute, that method is not exposed by the service.</span></span>

 <span data-ttu-id="8b611-112">Le code utilisé pour cette tâche est fourni dans l’exemple qui suit la procédure.</span><span class="sxs-lookup"><span data-stu-id="8b611-112">The code used for this task is provided in the example following the procedure.</span></span>

## <a name="define-a-service-contract"></a><span data-ttu-id="8b611-113">Définir un contrat de service</span><span class="sxs-lookup"><span data-stu-id="8b611-113">Define a service contract</span></span>

1. <span data-ttu-id="8b611-114">Ouvrez Visual Studio en tant qu’administrateur en cliquant sur le programme dans le **Démarrer** menu et en sélectionnant **plus** > **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="8b611-114">Open Visual Studio as an administrator by right-clicking the program in the **Start** menu and selecting **More** > **Run as administrator**.</span></span>

2. <span data-ttu-id="8b611-115">Créez un projet bibliothèque du Service WCF.</span><span class="sxs-lookup"><span data-stu-id="8b611-115">Create a WCF Service Library project.</span></span>

   1. <span data-ttu-id="8b611-116">Dans le menu **Fichier**, sélectionnez **Nouveau** > **Projet**.</span><span class="sxs-lookup"><span data-stu-id="8b611-116">From the **File** menu, select **New** > **Project**.</span></span>

   2. <span data-ttu-id="8b611-117">Dans le **nouveau projet** boîte de dialogue, sur le côté gauche, développez **Visual C#** ou **Visual Basic**, puis sélectionnez le **WCF** catégorie.</span><span class="sxs-lookup"><span data-stu-id="8b611-117">In the **New Project** dialog, on the left-hand side, expand **Visual C#** or **Visual Basic**, and then select the **WCF** category.</span></span> <span data-ttu-id="8b611-118">Une liste des modèles de projet s’affiche dans la section centrale de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8b611-118">A list of project templates is displayed in the center section of the dialog.</span></span> <span data-ttu-id="8b611-119">Sélectionnez **bibliothèque du Service WCF**.</span><span class="sxs-lookup"><span data-stu-id="8b611-119">Select **WCF Service Library**.</span></span>

   3. <span data-ttu-id="8b611-120">Entrez `GettingStartedLib` dans le **nom** zone de texte et `GettingStarted` dans le **nom de la Solution** zone de texte en bas de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8b611-120">Enter `GettingStartedLib` in the **Name** textbox and `GettingStarted` in the **Solution name** textbox at the bottom of the dialog.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8b611-121">Si vous ne voyez pas le **WCF** catégorie du modèle de projet, vous devrez peut-être installer le **Windows Communication Foundation** composant de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8b611-121">If you don't see the **WCF** project template category, you may need to install the **Windows Communication Foundation** component of Visual Studio.</span></span> <span data-ttu-id="8b611-122">Dans le **nouveau projet** boîte de dialogue, cliquez sur le lien **ouvrir Visual Studio Installer**.</span><span class="sxs-lookup"><span data-stu-id="8b611-122">In the **New Project** dialog box, click the link that says **Open Visual Studio Installer**.</span></span> <span data-ttu-id="8b611-123">Sélectionnez le **composants individuels** sous l’onglet, puis recherchez et sélectionnez **Windows Communication Foundation** sous le **activités de développement** catégorie.</span><span class="sxs-lookup"><span data-stu-id="8b611-123">Select the **Individual Components** tab, and then find and select **Windows Communication Foundation** under the **Development activities** category.</span></span> <span data-ttu-id="8b611-124">Choisissez **modifier** pour commencer l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="8b611-124">Choose **Modify** to begin installing the component.</span></span>

   <span data-ttu-id="8b611-125">Visual Studio crée le projet qui contient 3 fichiers : IService1.cs (ou IService1.vb), Service1.cs (ou Service1.vb) et App.config. Le fichier IService1 contient un contrat de service par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b611-125">Visual Studio creates the project, which contains 3 files: IService1.cs (or IService1.vb), Service1.cs (or Service1.vb), and App.config. The IService1 file contains a default service contract.</span></span> <span data-ttu-id="8b611-126">Le fichier Service1 contient une implémentation par défaut du contrat de service.</span><span class="sxs-lookup"><span data-stu-id="8b611-126">The Service1 file contains a default implementation of the service contract.</span></span> <span data-ttu-id="8b611-127">Le fichier App.config contient la configuration nécessaire pour charger le service par défaut avec l'hôte de service WCF Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8b611-127">The App.config file contains configuration needed to load the default service with the Visual Studio WCF Service Host.</span></span> <span data-ttu-id="8b611-128">Pour plus d’informations sur l’outil hôte de Service WCF, consultez [hôte de Service WCF (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)</span><span class="sxs-lookup"><span data-stu-id="8b611-128">For more information about the WCF Service Host tool, see [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)</span></span>

3. <span data-ttu-id="8b611-129">Ouvrez le fichier IService1.cs ou IService1.vb et supprimez le code au sein de la déclaration d’espace de noms, en laissant la déclaration d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="8b611-129">Open the IService1.cs or IService1.vb file and delete the code within the namespace declaration, leaving the namespace declaration.</span></span> <span data-ttu-id="8b611-130">Dans la déclaration d'espace de noms, définissez une nouvelle interface appelée `ICalculator` comme indiqué dans le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8b611-130">Inside the namespace declaration define a new interface called `ICalculator` as shown in the code below.</span></span>

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

     <span data-ttu-id="8b611-131">Ce contrat définit une calculatrice en ligne.</span><span class="sxs-lookup"><span data-stu-id="8b611-131">This contract defines an online calculator.</span></span> <span data-ttu-id="8b611-132">Notez que l'interface `ICalculator`est marquée avec l'attribut <xref:System.ServiceModel.ServiceContractAttribute>.</span><span class="sxs-lookup"><span data-stu-id="8b611-132">Notice the `ICalculator` interface is marked with the <xref:System.ServiceModel.ServiceContractAttribute> attribute.</span></span> <span data-ttu-id="8b611-133">Cet attribut définit un espace de noms qui est utilisé pour lever l'ambiguïté du nom de contrat.</span><span class="sxs-lookup"><span data-stu-id="8b611-133">This attribute defines a namespace that is used to disambiguate the contract name.</span></span> <span data-ttu-id="8b611-134">Chaque opération de calculatrice est marquée avec l'attribut <xref:System.ServiceModel.OperationContractAttribute>.</span><span class="sxs-lookup"><span data-stu-id="8b611-134">Each calculator operation is marked with the <xref:System.ServiceModel.OperationContractAttribute> attribute.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8b611-135">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8b611-135">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8b611-136">Comment : implémenter un contrat de service</span><span class="sxs-lookup"><span data-stu-id="8b611-136">How to: Implement a service contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

## <a name="see-also"></a><span data-ttu-id="8b611-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b611-137">See also</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [<span data-ttu-id="8b611-138">Guide pratique pour implémenter un contrat de service</span><span class="sxs-lookup"><span data-stu-id="8b611-138">How to: Implement a Service Contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [<span data-ttu-id="8b611-139">Prise en main</span><span class="sxs-lookup"><span data-stu-id="8b611-139">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="8b611-140">Auto-hébergement</span><span class="sxs-lookup"><span data-stu-id="8b611-140">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)