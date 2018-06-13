---
title: Bases de TransactionScope
ms.date: 03/30/2017
ms.assetid: 1e22b76a-76de-43b4-9be7-7a86ed3d5a44
ms.openlocfilehash: fe6877c4b2d72dc3d571740395fd4dc92ca8e99c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516800"
---
# <a name="basic-transactionscope"></a>Bases de TransactionScope
Cet exemple est composé de quatre scénarios qui s'exécutent pour montrer comment imbriquer des instances <xref:System.Activities.Statements.TransactionScope>. Le premier scénario présente l'imbrication d'une activité tierce dont l'auteur ignore totalement la construction. Les deuxième et troisième scénarios montrent comment les délais d'expiration sont respectés, et le dernier scénario présente le paramètre <xref:System.Activities.Statements.TransactionScope.AbortInstanceOnTransactionFailure%2A>.  
  
## <a name="nesting-of-transactionscopeactivity"></a>Imbrication de TransactionScopeActivity  
 Le workflow du premier scénario se compose d'une séquence de deux activités <xref:System.Activities.Statements.WriteLine> et d'un <xref:System.Activities.Statements.TransactionScope>. Le corps de <xref:System.Activities.Statements.TransactionScope> est une séquence de deux autres activités <xref:System.Activities.Statements.WriteLine>, d'une activité personnalisée qui imprime l'identificateur local de la transaction et d'une activité tierce. L'activité `TransactionScopeTest` tierce contient un <xref:System.Activities.Statements.TransactionScope>, mais l'auteur du workflow n'a aucun moyen de le savoir. Ce scénario montre que les activités <xref:System.Activities.Statements.TransactionScope> peuvent être imbriquées.  
  
## <a name="time-outs"></a>Délais d'expiration  
 Le workflow du deuxième scénario est presque identique au premier. `TransactionScopeTest` a été remplacé par un <xref:System.Activities.Statements.TransactionScope>. Le corps de <xref:System.Activities.Statements.TransactionScope> est un délai de cinq secondes et le délai d'expiration de la transaction est défini à deux secondes. La valeur du délai d'expiration de <xref:System.Activities.Statements.TransactionScope> est de 10 secondes. Notez que le plus petit délai d'expiration de l'étendue est respecté et que la transaction expire.  
  
 Le workflow du troisième scénario est presque identique au deuxième scénario. L'activité de délai a été déplacée du corps du <xref:System.Activities.Statements.TransactionScope> interne vers l'emplacement immédiatement après lui dans la séquence qui est le corps du <xref:System.Activities.Statements.TransactionScope> externe. La transaction expire toujours, mais cela est dû au fait que le délai d'expiration de deux secondes du <xref:System.Activities.Statements.TransactionScope> interne ne s'applique plus. La transaction expire au bout de 10 secondes lorsque le délai d'expiration du <xref:System.Activities.Statements.TransactionScope> externe est dépassé.  
  
## <a name="aborting-on-transaction-failure"></a>Abandon en cas d'échec de la transaction  
 Ce workflow est semblable au troisième scénario, excepté que les délais d'expiration ont été remplacés par la propriété <xref:System.Activities.Statements.TransactionScope.AbortInstanceOnTransactionFailure%2A>. Notez que les indicateurs de tous les enfants internes, s'ils sont définis, doivent correspondre au <xref:System.Activities.Statements.TransactionScope> externe. Dans ce scénario, ils ne le sont pas, et une exception est levée lorsque le workflow s'ouvre.  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1.  Ouvrez la solution BasicTransactionScopeSample.sl dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Pour générer la solution, appuyez sur CTRL + MAJ + B ou sélectionnez **générer la Solution** à partir de la **générer** menu.  
  
3.  Une fois la génération a réussi, appuyez sur F5 ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu. Ou bien vous pouvez appuyer sur CTRL + F5 ou sélectionnez **démarrer sans débogage** à partir de la **déboguer** menu pour exécuter sans débogage.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Transactions\BasicTransactionScope`