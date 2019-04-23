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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228391"
---
# <a name="tutorial-define-a-windows-communication-foundation-service-contract"></a>Tutoriel : Définir un contrat de service Windows Communication Foundation

Ce didacticiel décrit la première des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).

Lorsque vous créez un service WCF, votre première tâche consiste à définir un contrat de service. Le contrat de service spécifie les opérations prises en charge par le service. Une opération peut être considérée comme une méthode de service Web. Créer des contrats de service, vous devez définir un élément visuel C# ou de l’interface de Visual Basic (VB). Une interface possède les caractéristiques suivantes :

- Chaque méthode dans l'interface correspond à une opération de service spécifique. 
- Pour chaque interface, vous devez appliquer le <xref:System.ServiceModel.ServiceContractAttribute> attribut.
- Pour chaque opération/méthode, vous devez appliquer le <xref:System.ServiceModel.OperationContractAttribute> attribut. 

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Créer un **bibliothèque du Service WCF** projet.
> - Définir une interface de contrat de service.

## <a name="create-a-wcf-service-library-project-and-define-a-service-contract-interface"></a>Créez un projet de bibliothèque du Service WCF et définir une interface de contrat de service

1. Ouvrez Visual Studio en tant qu’administrateur. Pour ce faire, sélectionnez le programme Visual Studio dans le **Démarrer** menu, puis sélectionnez **plus** > **exécuter en tant qu’administrateur** dans le menu contextuel.

2. Créer un **bibliothèque du Service WCF** projet.

   1. Dans le menu **Fichier**, sélectionnez **Nouveau** > **Projet**.

   2. Dans le **nouveau projet** boîte de dialogue, sur le côté gauche, développez **Visual C#** ou **Visual Basic**, puis sélectionnez le **WCF** catégorie. Visual Studio affiche une liste des modèles de projet dans la section centrale de la fenêtre. Sélectionnez **bibliothèque du Service WCF**.

      > [!NOTE]
      > Si vous ne voyez pas le **WCF** catégorie du modèle de projet, vous devrez peut-être installer le **Windows Communication Foundation** composant de Visual Studio. Dans le **nouveau projet** boîte de dialogue, sélectionnez le **ouvrir Visual Studio Installer** lien sur le côté gauche. Sélectionnez le **composants individuels** sous l’onglet, puis recherchez et sélectionnez **Windows Communication Foundation** sous le **activités de développement** catégorie. Choisissez **modifier** pour commencer l’installation du composant.

   3. Dans la section inférieure de la fenêtre, entrez *GettingStartedLib* pour le **nom** et *GettingStarted* pour le **nom de la Solution**. 

   4. Sélectionnez **OK**.

      Visual Studio crée le projet, qui comporte trois fichiers : *IService1.cs* (ou *IService1.vb* pour un projet Visual Basic), *Service1.cs* (ou *Service1.vb* pour un projet Visual Basic), et  *App.config*. Visual Studio définit ces fichiers comme suit : 
      - Le *IService1* fichier contient la définition par défaut du contrat de service. 
      - Le *Service1* fichier contient l’implémentation par défaut du contrat de service. 
      - Le *App.config* fichier contient les informations de configuration nécessaires pour charger le service par défaut avec l’outil hôte de Service WCF Visual Studio. Pour plus d’informations sur l’outil hôte de Service WCF, consultez [hôte de Service WCF (WcfSvcHost.exe)](wcf-service-host-wcfsvchost-exe.md).

      > [!NOTE]
      > Si vous avez installé Visual Studio avec des paramètres d’environnement de développement de Visual Basic, la solution peut être masquée. Si c’est le cas, sélectionnez **Options** à partir de la **outils** menu, puis sélectionnez **projets et Solutions** > **général** dans le **Options** fenêtre. Sélectionnez **toujours afficher la solution**. En outre, vérifiez que **enregistrer les nouveaux projets lors de la création** est sélectionné.

3. À partir de **l’Explorateur de solutions**, ouvrez le **IService1.cs** ou **IService1.vb** , puis remplacez son code avec le code suivant :

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

     Ce contrat définit une calculatrice en ligne. Notez que le `ICalculator` interface est marquée avec le <xref:System.ServiceModel.ServiceContractAttribute> attribut (simplifiée comme `ServiceContract`). Cet attribut définit un espace de noms pour lever l’ambiguïté du nom de contrat. Le code marque chaque opération de calculatrice avec le <xref:System.ServiceModel.OperationContractAttribute> attribut (simplifiée comme `OperationContract`).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> - Créez un projet bibliothèque du Service WCF.
> - Définir une interface de contrat de service.

Passez au didacticiel suivant pour apprendre à implémenter le contrat de service WCF.

> [!div class="nextstepaction"]
> [Tutoriel : Implémenter un contrat de service WCF](how-to-implement-a-wcf-contract.md)
