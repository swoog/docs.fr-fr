---
title: XAML Activation
ms.date: 03/30/2017
ms.assetid: 486760e2-bb10-4ed5-8c02-fe7472498d2d
ms.openlocfilehash: 8621b0ea7b390c81e76ac7eeedb0b547b44320d7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="xaml-activation"></a>XAML Activation
Cet exemple montre comment héberger un workflow déclaratif dans IIS. C'est un workflow de base appelé `EchoService` qui comporte une opération.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à (page de téléchargement) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\XAMLActivation`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Ouvrez la solution XAMLActivation.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Générez la solution en appuyant sur **F5**.  
  
3.  Exécutez WcfTestClient.exe. À partir d'une invite de commandes, tapez ce qui suit :  
  
    1.  cd %SystemDrive%\Program Files\Microsoft Visual Studio 10.0\Common7\IDE  
  
    2.  Exécutez WcfTestClient.exe.  
  
4.  Définir l’adresse du service sur WcfTestClient.exe en appuyant sur CTRL + MAJ + A et l’adresse du service http://localhost:56133/Service.xamlx.  
  
5.  Effectuez l'opération Echo pour tester le service.  
  
6.  Déployez le service dans IIS en utilisant DeployToIIS.Bat dans une invite de commandes avec des privilèges d'administrateur.  
  
7.  Mettre à jour l’adresse du service du client pour http://localhost/XAMLActivation/Service.xamlx et tester le service à l’aide de WcfTestClient.exe.
