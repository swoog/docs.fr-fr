---
title: OverloadGroups
ms.date: 03/30/2017
ms.assetid: d1d547d2-f5fb-4de3-a959-ee6139a4f1ad
ms.openlocfilehash: 0773e76d36b25ad5485cc8912c7012815412de9f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43469867"
---
# <a name="overloadgroups"></a>OverloadGroups
Cet exemple se compose d'une activité (`CreateLocation`) qui a deux caractéristiques intéressantes :  
  
1.  Elle comprend quelques arguments obligatoires et quelques arguments facultatifs.  
  
2.  Elle permet à l'utilisateur de fournir un jeu d'arguments sélectionné parmi deux jeux d'arguments différents.  
  
 Ces comportements sont obtenus à l'aide des deux fonctionnalités suivantes :  
  
-   `[isRequired]` valide qu'une propriété d'une activité spécifique est affectée et, dans le cas contraire, lève une exception.  
  
-   `[OverloadGroup]` réunit un jeu d'arguments afin que l'utilisateur de l'activité puisse choisir d'utiliser l'un des deux jeux. L'utilisateur ne peut pas utiliser d'arguments de différents groupes surchargés dans la même instance.  
  
 Après avoir configuré des workflows différents, appelez <xref:System.Activities.Validation.ActivityValidationServices.Validate%2A> qui retourne une collection <xref:System.Activities.Validation.ValidationResults> de <xref:System.Activities.Validation.Constraint>. Imprimez les objets <xref:System.Activities.Validation.Constraint> sur la console.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Ouvrez le **OverloadGroups.sln** exemple de solution dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Générez et exécutez la solution.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Validation\OverloadGroups`
