---
title: Transactions de workflow
ms.date: 03/30/2017
ms.assetid: 6081fb02-c0f2-483d-97b8-f3b7dc03011d
ms.openlocfilehash: 17e4b712f5b6955ab777168d60d8a28e8b0ebd63
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153294"
---
# <a name="workflow-transactions"></a>Transactions de workflow

[!INCLUDE[wf1](../../../includes/wf1-md.md)] offre une prise en charge pour participer aux transactions <xref:System.Transactions> en utilisant l'activité <xref:System.Activities.Statements.TransactionScope> pour étendre une unité traitée de travail. Alors que le <xref:System.Transactions.TransactionScope?displayProperty=nameWithType> doit être terminé explicitement, l'activité <xref:System.Activities.Statements.TransactionScope?displayProperty=nameWithType> appelle implicitement la transaction une fois cette dernière terminée. Toute activité contenue dans l’élément <xref:System.Activities.Statements.TransactionScope.Body%2A> de l’activité <xref:System.Activities.Statements.TransactionScope> participe à la transaction. WF peut transférer des transactions dans un workflow en faisant appel à l’activité <xref:System.ServiceModel.Activities.TransactedReceiveScope>. Comme l'activité <xref:System.Activities.Statements.TransactionScope>, toute activité contenue dans le <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> participe à la transaction. WF vérifie que les activités dépendant de <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType> utilisent à la fois <xref:System.Activities.Statements.TransactionScope> et <xref:System.ServiceModel.Activities.TransactedReceiveScope>. Si les activités fournies par le système ne remplissent pas toutes les conditions, les activités personnalisées peuvent être construites à l’aide du <xref:System.Activities.RuntimeTransactionHandle> afin d’activer un flux avancé et des scénarios de contrôle de transaction.  
  
Dans l’exemple suivant, un flux de travail est composé d’un <xref:System.Activities.Statements.Sequence> activité qui contient les activités enfants, y compris un <xref:System.Activities.Statements.TransactionScope> activité. Les activités <xref:System.Activities.Statements.TransactionScope.Body%2A> du <xref:System.Activities.Statements.TransactionScope> s'exécutent sous la transaction initialisée par l'activité <xref:System.Activities.Statements.TransactionScope>.  
  
```csharp  
static Activity ScenarioOne()  
{  
    return new Sequence  
    {  
        Activities =  
        {  
            new WriteLine { Text = "    Begin workflow" },  
  
            new TransactionScope  
            {  
                Body = new Sequence  
                {  
                    Activities =   
                    {  
                        new WriteLine { Text = "    Begin TransactionScope" },  
  
                        new PrintTransactionId(),  
  
                        new TransactionScopeTest(),  
  
                        new WriteLine { Text = "    End TransactionScope" },  
                    },  
                },  
            },  
  
            new WriteLine { Text = "    End workflow" },  
        }  
    };  
}  
```  
  
Pour plus d’informations, consultez Utilisation <xref:System.ServiceModel.Activities.TransactedReceiveScope>, consultez [Transactions circulant vers et depuis des Services de Workflow](../wcf/feature-details/flowing-transactions-into-and-out-of-workflow-services.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Activities.Statements.TransactionScope>
- <xref:System.Transactions.TransactionScope>
- <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType>
