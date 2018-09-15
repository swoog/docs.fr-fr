---
title: Activité NoPersistScope
ms.date: 03/30/2017
ms.assetid: 9a0baeb7-a05c-4fac-b905-252758cb71bb
ms.openlocfilehash: 6543756594b6734aec39bf22c5ab6215605341b1
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45649547"
---
# <a name="nopersistscope-activity"></a>Activité NoPersistScope
Cet exemple montre comment manipuler un état non sérialisable et supprimable dans un workflow. Il est important que les workflows n'essaient pas de rendre l'état non sérialisable persistant et il est également important de nettoyer les objets supprimables après qu'ils ont été utilisés dans le workflow.  
  
## <a name="demonstrates"></a>Démonstrations  
 Concepteur et activité personnalisée `NoPersistScope`.  
  
## <a name="using-the-nopersistzone-activity"></a>Utilisation de l'activité NoPersistZone  
 Lors de l'exécution de l'exemple de workflow, une activité personnalisée appelée `CreateTextWriter` crée un objet de type <xref:System.IO.TextWriter> et l'enregistre dans une variable de workflow. <xref:System.IO.TextWriter> est un objet <xref:System.IDisposable>. Ce <xref:System.IO.TextWriter>, configuré pour écrire dans un fichier nommé « out.txt » dans le répertoire dans lequel l'exemple s'exécute, est utilisé par une activité <xref:System.Activities.Statements.WriteLine> lors de l'écho de tout texte que vous entrez au niveau de la console.  
  
 La logique d'écho est exécutée dans une activité `NoPersistScope` (le code associé fait également partie de cet exemple), qui empêche de rendre le workflow persistant. Si vous tapez dans `unload` à la console, l’hôte tente de conserver l’instance de flux de travail, mais cette opération arrive à expiration, car le flux de travail reste dans un `NoPersistScope`. Le workflow utilise également une activité personnalisée appelée `Dispose` pour supprimer l'objet <xref:System.IO.TextWriter> lorsque le workflow a fini de l'utiliser. L'activité `Dispose` est placée dans le bloc <xref:System.Activities.Statements.TryCatch.Finally%2A> de l'activité <xref:System.Activities.Statements.TryCatch> où la variable <xref:System.IO.TextWriter> est déclarée pour garantir son exécution même si une exception devait se produire pendant l'exécution du bloc Try.  
  
 Vous pouvez taper dans `exit` pour terminer l’instance de flux de travail et de quitter le programme.  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1.  Ouvrez la solution NoPersistZone.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Pour générer la solution, appuyez sur CTRL + MAJ + B ou sélectionnez **générer la Solution** à partir de la **Build** menu.  
  
3.  Une fois la génération a réussi, appuyez sur F5 ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu ou bien, vous pouvez appuyer sur CTRL + F5 ou sélectionnez **démarrer sans débogage** à partir de la **Déboguer** menu afin d’exécuter sans débogage.  
  
#### <a name="to-cleanup-optional"></a>Pour effectuer un nettoyage (facultatif)  
  
1.  Pour supprimer le magasin d'instances SQL, exécutez Cleanup.cmd.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\NoPersistScope`