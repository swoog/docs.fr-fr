---
title: Personnalisation des opérations d'insertion, de mise à jour et de suppression
ms.date: 03/30/2017
ms.assetid: 07eef055-8f6c-414d-850e-d323ff946cd0
ms.openlocfilehash: b4578a030300872bf4e0bab30b8daf12544be0cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361638"
---
# <a name="customizing-insert-update-and-delete-operations"></a><span data-ttu-id="0f38d-102">Personnalisation des opérations d'insertion, de mise à jour et de suppression</span><span class="sxs-lookup"><span data-stu-id="0f38d-102">Customizing Insert, Update, and Delete Operations</span></span>
<span data-ttu-id="0f38d-103">Par défaut, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] génère du SQL dynamique pour implémenter les opérations d'insertion, de lecture, de mise à jour et de suppression.</span><span class="sxs-lookup"><span data-stu-id="0f38d-103">By default, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] generates dynamic SQL to implement insert, read, update, and delete operations.</span></span> <span data-ttu-id="0f38d-104">Dans la pratique toutefois, vous personnalisez généralement votre application en fonction de vos besoins professionnels.</span><span class="sxs-lookup"><span data-stu-id="0f38d-104">In practice, however, you typically customize your application to suit your business needs.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0f38d-105">Si vous utilisez Visual Studio, vous pouvez utiliser la [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour personnaliser les insérer, mettre à jour et supprimer des actions.</span><span class="sxs-lookup"><span data-stu-id="0f38d-105">If you are using Visual Studio, you can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to customize insert, update, and delete actions.</span></span>  
  
 <span data-ttu-id="0f38d-106">Cette section de rubriques décrit les techniques que [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] fournit pour personnaliser les opérations d'insertion, de lecture, de mise à jour et de suppression dans votre application.</span><span class="sxs-lookup"><span data-stu-id="0f38d-106">This section of topics describes the techniques that [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] provides for customizing insert, read, update, and delete operations in your application.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0f38d-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="0f38d-107">In This Section</span></span>  
 [<span data-ttu-id="0f38d-108">Personnalisation d’opérations : vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="0f38d-108">Customizing Operations: Overview</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/customizing-operations-overview.md)  
 <span data-ttu-id="0f38d-109">Décrit les différentes techniques fournies par [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour personnaliser les opérations d'insertion, de lecture, de mise à jour et de suppression.</span><span class="sxs-lookup"><span data-stu-id="0f38d-109">Describes the various techniques [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] provides for customizing insert, read, update, and delete operations.</span></span>  
  
 [<span data-ttu-id="0f38d-110">Opérations d’insertion, de mise à jour et de suppression</span><span class="sxs-lookup"><span data-stu-id="0f38d-110">Insert, Update, and Delete Operations</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/insert-update-and-delete-operations.md)  
 <span data-ttu-id="0f38d-111">Décrit les processus par défaut de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour manipuler des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="0f38d-111">Describes the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] default processes for manipulating database data.</span></span>  
  
 [<span data-ttu-id="0f38d-112">Responsabilités du développeur en matière de substitution du comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="0f38d-112">Responsibilities of the Developer In Overriding Default Behavior</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/responsibilities-of-the-developer-in-overriding-default-behavior.md)  
 <span data-ttu-id="0f38d-113">Décrit le rôle du développeur dans l'implémentation des spécifications non appliquées par [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="0f38d-113">Describes the role of the developer in implementing requirements not enforced by [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>  
  
 [<span data-ttu-id="0f38d-114">Ajout d’une logique métier à l’aide de méthodes partielles</span><span class="sxs-lookup"><span data-stu-id="0f38d-114">Adding Business Logic By Using Partial Methods</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/adding-business-logic-by-using-partial-methods.md)  
 <span data-ttu-id="0f38d-115">Explique comment utiliser des méthodes partielles pour substituer des méthodes générées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0f38d-115">Describes how to use partial methods to override autogenerated methods.</span></span>
