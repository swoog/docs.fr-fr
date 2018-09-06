---
title: Validation de base
ms.date: 03/30/2017
ms.assetid: ba1343cc-aaab-4ade-b0c0-1dd5063bf4ad
ms.openlocfilehash: 74d99e2d426e9ea5701fad80418fdf019112cc9e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43879643"
---
# <a name="basic-validation"></a>Validation de base
Cet exemple se compose d'une activité, `CreateProduct`, qui valide que son argument `Cost` est plus petit ou égal à son argument `Price`.  
  
## <a name="sample-details"></a>Détails de l'exemple  
 Deux auteurs utilisent la validation, l'auteur d'activité (qui crée la logique de validation pour l'activité) et l'auteur de workflow qui appelle des services de validation sur un workflow spécifique. Dans ce scénario, l'auteur d'activité souhaite faire en sorte que chaque instance de son activité ait un coût inférieur ou égal au prix.  
  
 L'auteur d'activité (à l'intérieur de l'activité) doit effectuer les opérations suivantes :  
  
-   Créer une contrainte (`PriceGreaterThanCost`). Il s'agit de l'emplacement de toute la logique de validation.  
  
-   Substituer `System.Activities.CodeActivity.OnGetConstraints()` et ajouter la contrainte (`PriceGreaterThanCost`) aux contraintes <xref:System.Collections.IList>.  
  
 L'auteur de workflow (programme principal) doit effectuer les opérations suivantes :  
  
-   Créer un workflow avec une instance de l'activité à valider (`CreateProduct`).  
  
-   Appeler <xref:System.Activities.Validation.ActivityValidationServices.Validate%2A>, qui retourne une collection <xref:System.Activities.Validation.ValidationResults> de <xref:System.Activities.Validation.ValidationError>.  
  
-   (Facultatif) Imprimer les objets <xref:System.Activities.Validation.ValidationError>.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Ouvrez l'exemple de solution BasicValidation.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Générez et exécutez la solution.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Validation\BasicValidation`