---
title: 'Procédure : Utiliser EdmGen.exe pour valider les fichiers de modèle et mappage'
ms.date: 03/30/2017
ms.assetid: 2641906a-971a-4d0b-8aee-13fabc02a1cc
ms.openlocfilehash: 12258236c904c70d6d94490e3d1c6af2457bbe0c
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827885"
---
# <a name="how-to-use-edmgenexe-to-validate-model-and-mapping-files"></a><span data-ttu-id="e32e5-102">Procédure : Utiliser EdmGen.exe pour valider les fichiers de modèle et mappage</span><span class="sxs-lookup"><span data-stu-id="e32e5-102">How to: Use EdmGen.exe to Validate Model and Mapping Files</span></span>
<span data-ttu-id="e32e5-103">Cette rubrique montre comment utiliser le [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) outil pour valider le modèle et les fichiers de mappage.</span><span class="sxs-lookup"><span data-stu-id="e32e5-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to validate the model and mapping files.</span></span> <span data-ttu-id="e32e5-104">Pour plus d’informations, consultez [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).</span><span class="sxs-lookup"><span data-stu-id="e32e5-104">For more information, see [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).</span></span>  
  
### <a name="to-validate-the-school-model-using-edmgenexe"></a><span data-ttu-id="e32e5-105">Pour valider le modèle School à l'aide d'EdmGen.exe</span><span class="sxs-lookup"><span data-stu-id="e32e5-105">To validate the School model using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="e32e5-106">Créez la base de données School.</span><span class="sxs-lookup"><span data-stu-id="e32e5-106">Create the School database.</span></span> <span data-ttu-id="e32e5-107">Pour plus d’informations, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e32e5-107">For more information, see [Creating the School Sample Database](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span></span>  
  
2.  <span data-ttu-id="e32e5-108">Générez le modèle School.</span><span class="sxs-lookup"><span data-stu-id="e32e5-108">Generate the School model.</span></span> <span data-ttu-id="e32e5-109">Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="e32e5-109">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="e32e5-110">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="e32e5-110">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```console
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:ValidateArtifacts /inssdl:.\School.ssdl /inmsl:.\School.msl /incsdl:.\School.csdl  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="e32e5-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e32e5-111">See also</span></span>
- <span data-ttu-id="e32e5-112">[Guide pratique pour Configurer manuellement un projet Entity Framework](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e32e5-112">[How to: Manually Configure an Entity Framework Project](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100))</span></span>
- <span data-ttu-id="e32e5-113">[ADO.NET Entity Data Model Tools](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e32e5-113">[ADO.NET Entity Data Model Tools](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))</span></span>
- <span data-ttu-id="e32e5-114">[Guide pratique pour Prégénérer des vues pour améliorer les performances de requête](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896240(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e32e5-114">[How to: Pre-Generate Views to Improve Query Performance](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896240(v=vs.100))</span></span>
- [<span data-ttu-id="e32e5-115">Guide pratique pour Utiliser EdmGen.exe pour générer le Code de couche objet</span><span class="sxs-lookup"><span data-stu-id="e32e5-115">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-object-layer-code.md)
