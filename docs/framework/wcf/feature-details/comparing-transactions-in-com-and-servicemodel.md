---
title: Comparaison des transactions dans COM+ et dans ServiceModel
ms.date: 03/30/2017
ms.assetid: e493bcdd-b91a-4486-853f-83dbcd1931b7
ms.openlocfilehash: 4a47fe1686dff2e705b06b001d7d5e4ea6e8c5f2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33488645"
---
# <a name="comparing-transactions-in-com-and-servicemodel"></a>Comparaison des transactions dans COM+ et dans ServiceModel
Cette rubrique explique comment simuler le comportement d’un service COM + transactionnel à l’aide des attributs de Windows Communication Foundation (WCF) le <xref:System.ServiceModel> fournit de l’espace de noms.  
  
## <a name="emulating-com-using-servicemodel-attributes"></a>Émulation de COM+ à l'aide d'attributs ServiceModel  
 Le tableau suivant compare la <xref:System.EnterpriseServices.TransactionOption> énumération utilisée pour créer un `EnterpriseServices` transaction et comment elles sont corrélées aux attributs WCF le <xref:System.ServiceModel> fournit de l’espace de noms.  
  
|Attribut COM+|Attributs WCF|  
|---------------------|------------------------------------------------------------------------|  
|RequiresNew|<xref:System.ServiceModel.TransactionFlowAttribute> a la valeur <xref:System.ServiceModel.TransactionFlowOption.NotAllowed>.<br /><br /> <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionScopeRequired%2A> a la valeur `true`.<br /><br /> L'attribut `TransactionFlow` dans l'élément de liaison a la valeur `false`.|  
|Obligatoire|<xref:System.ServiceModel.TransactionFlowAttribute> a la valeur <xref:System.ServiceModel.TransactionFlowOption.Allowed>.<br /><br /> <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionScopeRequired%2A> a la valeur `true`.<br /><br /> L'attribut `TransactionFlow` dans l'élément de liaison a la valeur `true`.|  
|Pris en charge|Il n'existe pas d'équivalent direct. En général, vous devez à la place adopter le comportement spécifié pour `Required`.|  
|Non pris en charge|<xref:System.ServiceModel.OperationBehaviorAttribute.TransactionScopeRequired%2A> a la valeur `false`.<br /><br /> L'attribut `TransactionFlow` dans l'élément de liaison a la valeur `false`.|  
|Disabled|Il n'existe pas d'équivalent direct. En général, vous devez à la place adopter le comportement spécifié pour `NotSupported`.|
