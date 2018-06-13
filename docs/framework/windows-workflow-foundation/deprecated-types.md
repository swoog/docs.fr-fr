---
title: Types déconseillés dans Windows Workflow Foundation
ms.date: 03/30/2017
ms.assetid: 4aebe928-a964-4c1c-abf7-0dbbd3604b13
ms.openlocfilehash: 899d21f23c0500a1df01916d1da210b2f9bea95b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33512425"
---
# <a name="deprecated-types-in-windows-workflow-foundation"></a>Types déconseillés dans Windows Workflow Foundation
Dans le .NET 4, l'équipe de workflow a mis à disposition un nouveau au moteur de workflow dans l'espace de noms <xref:System.Activities>. Avec la version de .NET 4.5 bêta, nous sommes marquant la plupart des types dans le « WF 3 » <xref:System.Workflow.Activities>, <xref:System.Workflow.ComponentModel>, et <xref:System.Workflow.Runtime> espaces de noms comme obsolète.  
  
## <a name="obsolete-namespaces-and-tools"></a>Espaces de noms et outils obsolètes  
 Les assemblys suivants ont un ou plusieurs types publics qui seront déconseillés :  
  
-   System.Workflow.Activities.dll  
  
-   System.Workflow.ComponentModel.dll  
  
-   System.Workflow.Runtime.dll  
  
-   System.WorkflowServices.dll  
  
-   Microsoft.Workflow.DebugController.dll  
  
-   Microsoft.Workflow.Compiler.exe  
  
-   Wfc.exe  
  
 Par conséquent, les clients qui utilisent les API WF 3 déconseillées rencontreront des avertissements de génération avec un message similaire au suivant :  
  
 **Avertissement BC40000 : X est obsolète : types WF 3 sont déconseillés. Utilisez plutôt WF 4.** Nous allons supprimer les types du .NET Framework dans une mise en production ultérieure, mais nous n’avons pas encore déterminé cette plage de temps (pas dans la version 4.5). Cette étape nous permet de communiquer notre direction à nos clients et leur laisse le temps de migrer vers le nouveau modèle WF4. Nous allons, bien entendu, continuer à prendre en charge ces types WF 3 sous le [Microsoft politique de Support](http://aka.ms/MicrosoftSupportLifecycle). Les applications WF3 existantes s'exécutent sans problème sur le .NET 4.5, et [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] prend en charge les solutions WF3 nouvelles et existantes.  
  
 Les types liés aux règles dans l'espace de noms <xref:System.Workflow.Activities.Rules>, qui n'ont pas été remplacés dans WF 4.5, n'ont pas été déconseillés.  
  
 Les clients qui souhaitent migrer leurs applications vers WF 4 trouveront aide dans le [conseils de Migration de flux de travail 4](migration-guidance.md).
