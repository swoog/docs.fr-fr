---
title: Data Binding in a Windows Forms Client
ms.date: 03/30/2017
ms.assetid: a2a30b37-d6e2-4552-820e-e60b2bbe8829
ms.openlocfilehash: afca572fcc2c4e519d799511010d66859dc8b472
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54652105"
---
# <a name="data-binding-in-a-windows-forms-client"></a>Data Binding in a Windows Forms Client
Cet exemple montre comment lier aux données retournées par un service Windows Communication Foundation (WCF) dans une application Windows Forms.  
  
> [!NOTE]
>  La procédure d'installation ainsi que les instructions de génération relatives à cet exemple figurent en fin de rubrique.  
  
 Cet exemple contient un service qui implémente un contrat définissant un modèle de communication demande-réponse. L’exemple se compose d’un application Windows Forms (.exe) du client et un service WCF hébergé par Internet Information Services (IIS).  
  
 Le contrat est défini par l'interface `IWeatherService`, laquelle expose une opération nommée `GetWeatherData`. Cette opération accepte un tableau de villes et retourne un tableau d'objets `WeatherData` qui représente les prévisions de températures maximales et minimales d'une ville.  
  
 La liaison de données est générée sur le client, dans l'application Windows Forms. L'affichage `DataGridView`, qui correspond à une représentation graphique des données, est défini dans le concepteur Windows Forms. Un intermédiaire nommé `BindingSource` est également créé. La source de données de `BindingSource` a pour valeur le tableau de données retourné par le service. L'objectif de `BindingSource` est de fournir une couche d'indirection entre les données et leur affichage. Tous les processus concernant les données, telles que la navigation, le tri, le filtrage et la mise à jour, sont effectués en appelant le composant `BindingSource`. Pour lier les données à `DataGridView`, l'objet `datasource` est affecté à la source `DataGridView` de l'affichage `BindingSource`. Toutes les données retournées par le service WCF est ensuite affiché sous forme graphique à l’utilisateur.  Chaque fois que l'utilisateur clique sur le bouton, les données retournées sont automatiquement mises à jour dans l'affichage `DataGridView` lié aux données.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2.  Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3.  Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Scenario\DataBinding\WindowsForms`  
  
## <a name="see-also"></a>Voir aussi
