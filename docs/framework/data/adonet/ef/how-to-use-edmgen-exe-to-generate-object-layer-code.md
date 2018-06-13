---
title: 'Comment : utiliser EdmGen.exe pour générer le code de couche objet'
ms.date: 03/30/2017
ms.assetid: c44d2ebe-f66f-42cb-9741-4a3f0c2dcffb
ms.openlocfilehash: cd919f382096af6ff3e5e27225619767f3922ff0
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32761088"
---
# <a name="how-to-use-edmgenexe-to-generate-object-layer-code"></a><span data-ttu-id="b2be9-102">Comment : utiliser EdmGen.exe pour générer le code de couche objet</span><span class="sxs-lookup"><span data-stu-id="b2be9-102">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>
<span data-ttu-id="b2be9-103">Cette rubrique montre comment utiliser le [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) outil pour générer le code de couche objet basé sur le fichier .csdl.</span><span class="sxs-lookup"><span data-stu-id="b2be9-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to generate object-layer code  based on the .csdl file.</span></span>  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a><span data-ttu-id="b2be9-104">Pour générer le code de couche objet pour le modèle School à l'aide d'EdmGen.exe dans le cadre d'un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b2be9-104">To generate object-layer code for the School model for a Visual Basic project using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="b2be9-105">Créez la base de données School.</span><span class="sxs-lookup"><span data-stu-id="b2be9-105">Create the School database.</span></span> <span data-ttu-id="b2be9-106">Pour plus d’informations, consultez [création de la base de données School](http://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span><span class="sxs-lookup"><span data-stu-id="b2be9-106">For more information, see [Creating the School Sample Database](http://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span></span>  
  
2.  <span data-ttu-id="b2be9-107">Générez le modèle School ou obtenez le fichier School.csdl.</span><span class="sxs-lookup"><span data-stu-id="b2be9-107">Generate the School model or obtain the School.csdl file.</span></span> <span data-ttu-id="b2be9-108">Pour plus d’informations, consultez [Comment : utiliser des EdmGen.exe pour générer des fichiers de modèle et de mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="b2be9-108">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="b2be9-109">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="b2be9-109">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.vb /language:VB  
    ```  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-c-project-using-edmgenexe"></a><span data-ttu-id="b2be9-110">Pour générer le code de couche objet pour le modèle School à l'aide d'EdmGen.exe dans le cadre d'un projet C#</span><span class="sxs-lookup"><span data-stu-id="b2be9-110">To generate object-layer code for the School model for a C# project using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="b2be9-111">Créez la base de données School.</span><span class="sxs-lookup"><span data-stu-id="b2be9-111">Create the School database.</span></span> <span data-ttu-id="b2be9-112">Pour plus d’informations, consultez [création de la base de données School](http://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span><span class="sxs-lookup"><span data-stu-id="b2be9-112">For more information, see [Creating the School Sample Database](http://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span></span>  
  
2.  <span data-ttu-id="b2be9-113">Générez le modèle School ou obtenez le fichier School.csdl.</span><span class="sxs-lookup"><span data-stu-id="b2be9-113">Generate the School model or obtain the School.csdl file.</span></span> <span data-ttu-id="b2be9-114">Pour plus d’informations, consultez [Comment : utiliser des EdmGen.exe pour générer des fichiers de modèle et de mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="b2be9-114">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="b2be9-115">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="b2be9-115">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.cs /language:CSharp  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b2be9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2be9-116">See Also</span></span>  
 [<span data-ttu-id="b2be9-117">Modélisation et mappage</span><span class="sxs-lookup"><span data-stu-id="b2be9-117">Modeling and Mapping</span></span>](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)  
 [<span data-ttu-id="b2be9-118">Comment : configurer manuellement un projet Entity Framework</span><span class="sxs-lookup"><span data-stu-id="b2be9-118">How to: Manually Configure an Entity Framework Project</span></span>](http://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)  
 [<span data-ttu-id="b2be9-119">Outils ADO.NET Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="b2be9-119">ADO.NET Entity Data Model  Tools</span></span>](http://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)  
 [<span data-ttu-id="b2be9-120">Comment : prégénérer des vues pour améliorer les performances des requêtes</span><span class="sxs-lookup"><span data-stu-id="b2be9-120">How to: Pre-Generate Views to Improve Query Performance</span></span>](http://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)  
 [<span data-ttu-id="b2be9-121">Guide pratique pour utiliser EdmGen.exe pour générer les fichiers de modèle et les fichiers de mappage</span><span class="sxs-lookup"><span data-stu-id="b2be9-121">How to: Use EdmGen.exe to Generate the Model and Mapping Files</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)
