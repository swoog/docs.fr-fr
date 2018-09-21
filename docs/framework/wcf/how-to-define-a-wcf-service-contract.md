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
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46537876"
---
# <a name="how-to-define-a-windows-communication-foundation-service-contract"></a>Comment : définir un contrat de service Windows Communication Foundation

Il s’agit de la première des six tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).

 Lorsque vous créez un service WCF, la première tâche consiste à définir un contrat de service. Le contrat de service spécifie les opérations prises en charge par le service. Une opération peut être considérée comme une méthode de service Web. Les contrats sont créés en définissant une interface C++, C# ou Visual Basic (VB). Chaque méthode dans l'interface correspond à une opération de service spécifique. Chaque interface doit avoir le <xref:System.ServiceModel.ServiceContractAttribute> qui s'applique à elle et chaque opération doit avoir l'attribut <xref:System.ServiceModel.OperationContractAttribute> qui s'applique à elle. Si une méthode dans une interface qui a l'attribut <xref:System.ServiceModel.ServiceContractAttribute> n'a pas l'attribut <xref:System.ServiceModel.OperationContractAttribute>, cette méthode n'est pas exposée par le service.

 Le code utilisé pour cette tâche est fourni dans l’exemple qui suit la procédure.

## <a name="define-a-service-contract"></a>Définir un contrat de service

1. Ouvrez Visual Studio en tant qu’administrateur en cliquant sur le programme dans le **Démarrer** menu et en sélectionnant **plus** > **exécuter en tant qu’administrateur**.

2. Créez un projet bibliothèque du Service WCF.

   1. Dans le menu **Fichier**, sélectionnez **Nouveau** > **Projet**.

   2. Dans le **nouveau projet** boîte de dialogue, sur le côté gauche, développez **Visual C#** ou **Visual Basic**, puis sélectionnez le **WCF** catégorie. Une liste des modèles de projet s’affiche dans la section centrale de la boîte de dialogue. Sélectionnez **bibliothèque du Service WCF**.

   3. Entrez `GettingStartedLib` dans le **nom** zone de texte et `GettingStarted` dans le **nom de la Solution** zone de texte en bas de la boîte de dialogue.

   > [!NOTE]
   > Si vous ne voyez pas le **WCF** catégorie du modèle de projet, vous devrez peut-être installer le **Windows Communication Foundation** composant de Visual Studio. Dans le **nouveau projet** boîte de dialogue, cliquez sur le lien **ouvrir Visual Studio Installer**. Sélectionnez le **composants individuels** sous l’onglet, puis recherchez et sélectionnez **Windows Communication Foundation** sous le **activités de développement** catégorie. Choisissez **modifier** pour commencer l’installation du composant.

   Visual Studio crée le projet qui contient 3 fichiers : IService1.cs (ou IService1.vb), Service1.cs (ou Service1.vb) et App.config. Le fichier IService1 contient un contrat de service par défaut. Le fichier Service1 contient une implémentation par défaut du contrat de service. Le fichier App.config contient la configuration nécessaire pour charger le service par défaut avec l'hôte de service WCF Visual Studio. Pour plus d’informations sur l’outil hôte de Service WCF, consultez [hôte de Service WCF (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)

3. Ouvrez le fichier IService1.cs ou IService1.vb et supprimez le code au sein de la déclaration d’espace de noms, en laissant la déclaration d’espace de noms. Dans la déclaration d'espace de noms, définissez une nouvelle interface appelée `ICalculator` comme indiqué dans le code ci-dessous.

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

     Ce contrat définit une calculatrice en ligne. Notez que l'interface `ICalculator`est marquée avec l'attribut <xref:System.ServiceModel.ServiceContractAttribute>. Cet attribut définit un espace de noms qui est utilisé pour lever l'ambiguïté du nom de contrat. Chaque opération de calculatrice est marquée avec l'attribut <xref:System.ServiceModel.OperationContractAttribute>.

## <a name="next-steps"></a>Étapes suivantes

> [!div class="nextstepaction"]
> [Comment : implémenter un contrat de service](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [Guide pratique pour implémenter un contrat de service](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)