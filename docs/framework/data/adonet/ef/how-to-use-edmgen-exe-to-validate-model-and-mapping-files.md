---
title: 'Procédure : Utiliser EdmGen.exe pour valider les fichiers de modèle et les fichiers de mappage'
ms.date: 03/30/2017
ms.assetid: 2641906a-971a-4d0b-8aee-13fabc02a1cc
ms.openlocfilehash: 1981e293d634af451a7084ac519a97f1ad5b5fd6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59076518"
---
# <a name="how-to-use-edmgenexe-to-validate-model-and-mapping-files"></a><span data-ttu-id="f9638-102">Procédure : Utiliser EdmGen.exe pour valider les fichiers de modèle et les fichiers de mappage</span><span class="sxs-lookup"><span data-stu-id="f9638-102">How to: Use EdmGen.exe to Validate Model and Mapping Files</span></span>
<span data-ttu-id="f9638-103">Cette rubrique montre comment utiliser le [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) outil pour valider le modèle et les fichiers de mappage.</span><span class="sxs-lookup"><span data-stu-id="f9638-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to validate the model and mapping files.</span></span> <span data-ttu-id="f9638-104">Pour plus d’informations, consultez [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).</span><span class="sxs-lookup"><span data-stu-id="f9638-104">For more information, see [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).</span></span>  
  
### <a name="to-validate-the-school-model-using-edmgenexe"></a><span data-ttu-id="f9638-105">Pour valider le modèle School à l'aide d'EdmGen.exe</span><span class="sxs-lookup"><span data-stu-id="f9638-105">To validate the School model using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="f9638-106">Créez la base de données School.</span><span class="sxs-lookup"><span data-stu-id="f9638-106">Create the School database.</span></span> <span data-ttu-id="f9638-107">Pour plus d’informations, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f9638-107">For more information, see [Creating the School Sample Database](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span></span>  
  
2.  <span data-ttu-id="f9638-108">Générez le modèle School.</span><span class="sxs-lookup"><span data-stu-id="f9638-108">Generate the School model.</span></span> <span data-ttu-id="f9638-109">Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="f9638-109">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="f9638-110">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="f9638-110">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```console
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:ValidateArtifacts /inssdl:.\School.ssdl /inmsl:.\School.msl /incsdl:.\School.csdl  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="f9638-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9638-111">See also</span></span>

- [<span data-ttu-id="f9638-112">Procédure : Configurer manuellement un projet Entity Framework</span><span class="sxs-lookup"><span data-stu-id="f9638-112">How to: Manually Configure an Entity Framework Project</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100))
- [<span data-ttu-id="f9638-113">Outils ADO.NET Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="f9638-113">ADO.NET Entity Data Model Tools</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))
- [<span data-ttu-id="f9638-114">Procédure : Prégénérer des vues pour améliorer les performances de requête</span><span class="sxs-lookup"><span data-stu-id="f9638-114">How to: Pre-Generate Views to Improve Query Performance</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896240(v=vs.100))
- [<span data-ttu-id="f9638-115">Procédure : Utiliser EdmGen.exe pour générer le code de couche objet</span><span class="sxs-lookup"><span data-stu-id="f9638-115">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-object-layer-code.md)
