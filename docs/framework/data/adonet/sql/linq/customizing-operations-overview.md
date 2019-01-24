---
title: "Personnalisation d’opérations : Vue d'ensemble"
ms.date: 03/30/2017
ms.assetid: a3546296-1443-4b88-aa6e-d41011041ba7
ms.openlocfilehash: 4f13bed76ad2814d669f487b57ae9acbdc08eb74
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735459"
---
# <a name="customizing-operations-overview"></a>Personnalisation d’opérations : Vue d'ensemble
Par défaut, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] génère du SQL dynamique pour les opérations d'insertion, de mise à jour et de suppression selon le mappage. Dans la pratique cependant, vous souhaiterez généralement ajouter votre propre logique métier pour des raisons de sécurité, de validation, etc.  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] techniques de personnalisation de ces opérations sont les suivants :  
  
## <a name="loading-options"></a>Options de chargement  
 Dans vos requêtes, vous pouvez déterminer quelle quantité de données liées à votre cible principale est récupérée lorsque vous vous connectez à la base de données. Cette fonctionnalité est implémentée en grande partie à l'aide de <xref:System.Data.Linq.DataLoadOptions>. Pour plus d’informations, consultez [différée / le chargement immédiat](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md).  
  
## <a name="partial-methods"></a>Méthodes partielles  
 Dans son mappage par défaut, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] fournit des méthodes partielles qui vous permettent d'implémenter votre logique métier. Pour plus d’informations, consultez [Ajout d’entreprise logique par à l’aide de méthodes partielles](../../../../../../docs/framework/data/adonet/sql/linq/adding-business-logic-by-using-partial-methods.md).  
  
## <a name="stored-procedures-and-user-defined-functions"></a>Procédures stockées et fonctions définies par l'utilisateur  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] prend en charge l’utilisation de procédures stockées et fonctions définies par l’utilisateur. Les procédures stockées sont couramment utilisées pour personnaliser des opérations. Pour plus d’informations, consultez [Procédures stockées](../../../../../../docs/framework/data/adonet/sql/linq/stored-procedures.md).  
  
## <a name="see-also"></a>Voir aussi
- [Personnalisation des opérations d’insertion, de mise à jour et de suppression](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md)
