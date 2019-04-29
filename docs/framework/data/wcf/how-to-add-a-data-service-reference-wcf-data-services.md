---
title: 'Procédure : Ajouter une référence de Service de données (WCF Data Services)'
ms.date: 08/24/2018
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 62c6f318-3ee1-433a-b7a3-efa234c3034c
ms.openlocfilehash: fc1786e1c6102c702374989253cd3ce23e3f7b54
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765529"
---
# <a name="how-to-add-a-data-service-reference-wcf-data-services"></a><span data-ttu-id="c127b-102">Procédure : Ajouter une référence de service de données (WCF Data Services)</span><span class="sxs-lookup"><span data-stu-id="c127b-102">How to: Add a data service reference (WCF Data Services)</span></span>

<span data-ttu-id="c127b-103">Vous pouvez utiliser la **ajouter une référence de Service** boîte de dialogue dans Visual Studio pour ajouter une référence à WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="c127b-103">You can use the **Add Service Reference** dialog in Visual Studio to add a reference to WCF Data Services.</span></span> <span data-ttu-id="c127b-104">De cette manière, vous pouvez accéder plus facilement à un service de données dans une application cliente que vous développez dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c127b-104">This enables you to more easily access a data service in a client application that you develop in Visual Studio.</span></span> <span data-ttu-id="c127b-105">Lorsque vous complétez cette procédure, les classes de données sont générées selon les métadonnées obtenues auprès du service de données.</span><span class="sxs-lookup"><span data-stu-id="c127b-105">When you complete this procedure, data classes are generated based on metadata that is obtained from the data service.</span></span> <span data-ttu-id="c127b-106">Pour plus d’informations, consultez [génération de la bibliothèque de Client de Service de données](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="c127b-106">For more information, see [Generating the Data Service Client Library](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md).</span></span>

## <a name="add-a-data-service-reference"></a><span data-ttu-id="c127b-107">Ajouter une référence de service de données</span><span class="sxs-lookup"><span data-stu-id="c127b-107">Add a data service reference</span></span>

1. <span data-ttu-id="c127b-108">(Facultatif) Si le service de données n'appartient pas à la solution et n'est pas déjà en cours d'exécution, démarrez le service de données et notez l'URI du service de données.</span><span class="sxs-lookup"><span data-stu-id="c127b-108">(Optional) If the data service is not part of the solution and is not already running, start the data service and note the URI of the data service.</span></span>

2. <span data-ttu-id="c127b-109">Dans Visual Studio, dans **l’Explorateur de solutions**, cliquez sur le projet client, puis sélectionnez **ajouter** > **une référence de Service**.</span><span class="sxs-lookup"><span data-stu-id="c127b-109">In Visual Studio, in **Solution Explorer**, right-click the client project and then select **Add** > **Service Reference**.</span></span>

3. <span data-ttu-id="c127b-110">Si le service de données fait partie de la solution actuelle, cliquez sur **Discover**.</span><span class="sxs-lookup"><span data-stu-id="c127b-110">If the data service is part of the current solution, click **Discover**.</span></span>

     <span data-ttu-id="c127b-111">- ou -</span><span class="sxs-lookup"><span data-stu-id="c127b-111">-or-</span></span>

     <span data-ttu-id="c127b-112">Dans le **adresse** zone de texte, tapez l’URL de base du service de données, telles que `http://localhost:1234/Northwind.svc`, puis cliquez sur **accédez**.</span><span class="sxs-lookup"><span data-stu-id="c127b-112">In the **Address** text box, type the base URL of the data service, such as `http://localhost:1234/Northwind.svc`, and then click **Go**.</span></span>

4. <span data-ttu-id="c127b-113">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="c127b-113">Select **OK**.</span></span>

     <span data-ttu-id="c127b-114">Un nouveau fichier de code qui contient les classes de données qui peuvent accéder et interagir avec les ressources de service de données est ajouté au projet.</span><span class="sxs-lookup"><span data-stu-id="c127b-114">A new code file that contains the data classes that can access and interact with data service resources is added to the project.</span></span>

## <a name="see-also"></a><span data-ttu-id="c127b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c127b-115">See also</span></span>

- [<span data-ttu-id="c127b-116">Démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="c127b-116">Quickstart</span></span>](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)