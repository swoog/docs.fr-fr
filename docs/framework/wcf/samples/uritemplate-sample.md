---
title: UriTemplate, exemple
ms.date: 03/30/2017
ms.assetid: 0aaf91d0-ce18-468d-8006-bc9bc2e48231
ms.openlocfilehash: 0dfb2cdc27460f3bc30a1c4302206bf43f7ef007
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482959"
---
# <a name="uritemplate-sample"></a><span data-ttu-id="2f545-102">UriTemplate, exemple</span><span class="sxs-lookup"><span data-stu-id="2f545-102">UriTemplate Sample</span></span>
<span data-ttu-id="2f545-103">La classe <xref:System.UriTemplate> fournit des méthodes pour utiliser des ensembles d'URI qui partagent une structure commune.</span><span class="sxs-lookup"><span data-stu-id="2f545-103">The <xref:System.UriTemplate> class provides methods for working with sets of URIs that share a common structure.</span></span> <span data-ttu-id="2f545-104">Cet exemple illustre les concepts clés suivants relatifs au `UriTemplate` :</span><span class="sxs-lookup"><span data-stu-id="2f545-104">This sample demonstrates the following key concepts relating to `UriTemplate`:</span></span>  
  
-   <span data-ttu-id="2f545-105">Syntaxe de création des modèles.</span><span class="sxs-lookup"><span data-stu-id="2f545-105">Syntax for creating templates.</span></span>  
  
-   <span data-ttu-id="2f545-106">Instanciation d'URI depuis un `UriTemplate` à l'aide de <xref:System.UriTemplate.BindByName%2A> et <xref:System.UriTemplate.BindByPosition%2A>.</span><span class="sxs-lookup"><span data-stu-id="2f545-106">Instantiating URIs from a `UriTemplate` using <xref:System.UriTemplate.BindByName%2A> and <xref:System.UriTemplate.BindByPosition%2A>.</span></span>  
  
-   <span data-ttu-id="2f545-107"><xref:System.UriTemplateTable.Match%2A>, qui est l'opération inverse de `BindByName` et `BindByPosition`.</span><span class="sxs-lookup"><span data-stu-id="2f545-107"><xref:System.UriTemplateTable.Match%2A>, which is the inverse operation of `BindByName` and `BindByPosition`.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="2f545-108">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="2f545-108">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="2f545-109">Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2f545-109">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
2.  <span data-ttu-id="2f545-110">Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2f545-110">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="2f545-111">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2f545-111">The samples may already be installed on your computer.</span></span> <span data-ttu-id="2f545-112">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="2f545-112">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="2f545-113">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="2f545-113">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="2f545-114">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="2f545-114">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\UriTemplate`  
  
## <a name="see-also"></a><span data-ttu-id="2f545-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f545-115">See Also</span></span>  
 [<span data-ttu-id="2f545-116">Table UriTemplate</span><span class="sxs-lookup"><span data-stu-id="2f545-116">UriTemplate Table</span></span>](../../../../docs/framework/wcf/samples/uritemplate-table-sample.md)  
 [<span data-ttu-id="2f545-117">Répartiteur de table UriTemplate</span><span class="sxs-lookup"><span data-stu-id="2f545-117">UriTemplate Table Dispatcher</span></span>](../../../../docs/framework/wcf/samples/uritemplate-table-dispatcher-sample.md)
