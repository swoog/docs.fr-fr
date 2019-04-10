---
title: 'Procédure : Utiliser EdmGen.exe pour générer le code de couche objet'
ms.date: 03/30/2017
ms.assetid: c44d2ebe-f66f-42cb-9741-4a3f0c2dcffb
ms.openlocfilehash: 8a39027ee6a5647bbd645f5a38e35d61f7ebbd8e
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59333403"
---
# <a name="how-to-use-edmgenexe-to-generate-object-layer-code"></a><span data-ttu-id="9c2e2-102">Procédure : Utiliser EdmGen.exe pour générer le code de couche objet</span><span class="sxs-lookup"><span data-stu-id="9c2e2-102">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>
<span data-ttu-id="9c2e2-103">Cette rubrique montre comment utiliser le [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) outil pour générer le code de couche objet basée sur le fichier .csdl.</span><span class="sxs-lookup"><span data-stu-id="9c2e2-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to generate object-layer code  based on the .csdl file.</span></span>  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a><span data-ttu-id="9c2e2-104">Pour générer le code de couche objet pour le modèle School à l'aide d'EdmGen.exe dans le cadre d'un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9c2e2-104">To generate object-layer code for the School model for a Visual Basic project using EdmGen.exe</span></span>  
  
1. <span data-ttu-id="9c2e2-105">Créez la base de données School.</span><span class="sxs-lookup"><span data-stu-id="9c2e2-105">Create the School database.</span></span> <span data-ttu-id="9c2e2-106">Pour plus d’informations, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="9c2e2-106">For more information, see [Creating the School Sample Database](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span></span>  
  
2. <span data-ttu-id="9c2e2-107">Générez le modèle School ou obtenez le fichier School.csdl.</span><span class="sxs-lookup"><span data-stu-id="9c2e2-107">Generate the School model or obtain the School.csdl file.</span></span> <span data-ttu-id="9c2e2-108">Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="9c2e2-108">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3. <span data-ttu-id="9c2e2-109">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="9c2e2-109">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.vb /language:VB  
    ```  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-c-project-using-edmgenexe"></a><span data-ttu-id="9c2e2-110">Pour générer le code de couche objet pour le modèle School à l'aide d'EdmGen.exe dans le cadre d'un projet C#</span><span class="sxs-lookup"><span data-stu-id="9c2e2-110">To generate object-layer code for the School model for a C# project using EdmGen.exe</span></span>  
  
1. <span data-ttu-id="9c2e2-111">Créez la base de données School.</span><span class="sxs-lookup"><span data-stu-id="9c2e2-111">Create the School database.</span></span> <span data-ttu-id="9c2e2-112">Pour plus d’informations, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="9c2e2-112">For more information, see [Creating the School Sample Database](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).</span></span>  
  
2. <span data-ttu-id="9c2e2-113">Générez le modèle School ou obtenez le fichier School.csdl.</span><span class="sxs-lookup"><span data-stu-id="9c2e2-113">Generate the School model or obtain the School.csdl file.</span></span> <span data-ttu-id="9c2e2-114">Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="9c2e2-114">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3. <span data-ttu-id="9c2e2-115">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="9c2e2-115">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.cs /language:CSharp  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="9c2e2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c2e2-116">See also</span></span>

- [<span data-ttu-id="9c2e2-117">Modélisation et mappage</span><span class="sxs-lookup"><span data-stu-id="9c2e2-117">Modeling and Mapping</span></span>](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)
- [<span data-ttu-id="9c2e2-118">Procédure : Configurer manuellement un projet Entity Framework</span><span class="sxs-lookup"><span data-stu-id="9c2e2-118">How to: Manually Configure an Entity Framework Project</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100))
- [<span data-ttu-id="9c2e2-119">ADO.NET Entity Data Model Tools</span><span class="sxs-lookup"><span data-stu-id="9c2e2-119">ADO.NET Entity Data Model  Tools</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))
- [<span data-ttu-id="9c2e2-120">Procédure : Prégénérer des vues pour améliorer les performances de requête</span><span class="sxs-lookup"><span data-stu-id="9c2e2-120">How to: Pre-Generate Views to Improve Query Performance</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896240(v=vs.100))
- [<span data-ttu-id="9c2e2-121">Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et des fichiers de mappage</span><span class="sxs-lookup"><span data-stu-id="9c2e2-121">How to: Use EdmGen.exe to Generate the Model and Mapping Files</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)
