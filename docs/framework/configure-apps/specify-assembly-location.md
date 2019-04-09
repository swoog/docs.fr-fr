---
title: Spécification de l'emplacement d'un assembly
ms.date: 03/30/2017
helpviewer_keywords:
- configuration [.NET Framework], applications
- application configuration [.NET Framework]
- assemblies [.NET Framework], specifying location
ms.assetid: 1cb92bd7-6bab-44cf-8fd3-36303ce84fea
ms.openlocfilehash: f7d09e315f2ccc7ecdcf22719ca6dce1ee1411b4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59186288"
---
# <a name="specifying-an-assemblys-location"></a><span data-ttu-id="66267-102">Spécification de l'emplacement d'un assembly</span><span class="sxs-lookup"><span data-stu-id="66267-102">Specifying an Assembly's Location</span></span>
<span data-ttu-id="66267-103">Il existe deux façons de spécifier l’emplacement d’un assembly :</span><span class="sxs-lookup"><span data-stu-id="66267-103">There are two ways to specify an assembly's location:</span></span>  
  
-   <span data-ttu-id="66267-104">À l’aide de la [ \<codeBase >](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="66267-104">Using the [\<codeBase>](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) element.</span></span>  
  
-   <span data-ttu-id="66267-105">À l’aide de la [ \<probing >](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="66267-105">Using the [\<probing>](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) element.</span></span>  
  
 <span data-ttu-id="66267-106">Vous pouvez également utiliser le [.NET Framework Configuration Tool (Mscorcfg.msc)](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/2bc0cxhc(v=vs.100)) pour spécifier les emplacements des assemblys ou spécifier des emplacements pour le common language runtime détecter les assemblys.</span><span class="sxs-lookup"><span data-stu-id="66267-106">You can also use the [.NET Framework Configuration Tool (Mscorcfg.msc)](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/2bc0cxhc(v=vs.100)) to specify assembly locations or specify locations for the common language runtime to probe for assemblies.</span></span>  
  
## <a name="using-the-codebase-element"></a><span data-ttu-id="66267-107">À l’aide de la \<codeBase > élément</span><span class="sxs-lookup"><span data-stu-id="66267-107">Using the \<codeBase> Element</span></span>  
 <span data-ttu-id="66267-108">Vous pouvez utiliser la  **\<codeBase >** élément uniquement dans la machine serveur de publication stratégie fichiers de configuration ou qui redirigent également la version d’assembly.</span><span class="sxs-lookup"><span data-stu-id="66267-108">You can use the **\<codeBase>** element only in machine configuration or publisher policy files that also redirect the assembly version.</span></span> <span data-ttu-id="66267-109">Lorsque le runtime détermine la version d’assembly à utiliser, elle s’applique le paramètre de base de code à partir du fichier qui détermine la version.</span><span class="sxs-lookup"><span data-stu-id="66267-109">When the runtime determines which assembly version to use, it applies the code base setting from the file that determines the version.</span></span> <span data-ttu-id="66267-110">Si aucune base de code n’est indiqué, le runtime détecte l’assembly de façon normale.</span><span class="sxs-lookup"><span data-stu-id="66267-110">If no code base is indicated, the runtime probes for the assembly in the normal way.</span></span> <span data-ttu-id="66267-111">Pour plus d’informations, consultez [méthode de localisation des assemblys par le Runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="66267-111">For details, see [How the Runtime Locates Assemblies](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span></span>  
  
 <span data-ttu-id="66267-112">L’exemple suivant montre comment spécifier l’emplacement d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="66267-112">The following example shows how to specify an assembly's location.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
       <dependentAssembly>  
         <assemblyIdentity name="myAssembly"  
                           publicKeyToken="32ab4ba45e0a69a1"  
                           culture="en-us" />  
         <codeBase version="2.0.0.0"  
                   href="http://www.litwareinc.com/myAssembly.dll"/>  
       </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="66267-113">Le **version** attribut est obligatoire pour tous les assemblys avec nom fort, mais doit être omis pour les assemblys qui ne sont pas de nom fort.</span><span class="sxs-lookup"><span data-stu-id="66267-113">The **version** attribute is required for all strong-named assemblies but should be omitted for assemblies that are not strong-named.</span></span> <span data-ttu-id="66267-114">Le  **\<codeBase >** élément requiert le **href** attribut.</span><span class="sxs-lookup"><span data-stu-id="66267-114">The **\<codeBase>** element requires the **href** attribute.</span></span> <span data-ttu-id="66267-115">Vous ne pouvez pas spécifier des plages de versions dans le  **\<codeBase >** élément.</span><span class="sxs-lookup"><span data-stu-id="66267-115">You cannot specify version ranges in the **\<codeBase>** element.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="66267-116">Si vous fournissez un indicateur de base de code pour un assembly qui n’est pas un nom fort, l’indicateur doit pointer vers la base de l’application ou un sous-répertoire du répertoire de base de l’application.</span><span class="sxs-lookup"><span data-stu-id="66267-116">If you are supplying a code base hint for an assembly that is not strong-named, the hint must point to the application base or a subdirectory of the application base directory.</span></span>  
  
## <a name="using-the-probing-element"></a><span data-ttu-id="66267-117">À l’aide de la \<probing > élément</span><span class="sxs-lookup"><span data-stu-id="66267-117">Using the \<probing> Element</span></span>  
 <span data-ttu-id="66267-118">Le runtime localise les assemblys qui n’ont pas d’une base de code par la détection.</span><span class="sxs-lookup"><span data-stu-id="66267-118">The runtime locates assemblies that do not have a code base by probing.</span></span> <span data-ttu-id="66267-119">Pour plus d’informations sur la détection, consultez [méthode de localisation des assemblys par le Runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="66267-119">For more information about probing, see [How the Runtime Locates Assemblies](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span></span>  
  
 <span data-ttu-id="66267-120">Vous pouvez utiliser la [ \<probing >](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) élément dans le fichier de configuration d’application pour spécifier le runtime doit rechercher lors de la localisation d’un assembly de sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="66267-120">You can use the [\<probing>](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) element in the application configuration file to specify subdirectories the runtime should search when locating an assembly.</span></span> <span data-ttu-id="66267-121">L’exemple suivant montre comment spécifier le runtime doit rechercher les répertoires.</span><span class="sxs-lookup"><span data-stu-id="66267-121">The following example shows how to specify directories the runtime should search.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <probing privatePath="bin;bin2\subbin;bin3"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="66267-122">Le **privatePath** attribut contient les répertoires dans lesquels le runtime doit rechercher les assemblys.</span><span class="sxs-lookup"><span data-stu-id="66267-122">The **privatePath** attribute contains the directories that the runtime should search for assemblies.</span></span> <span data-ttu-id="66267-123">Si l’application se trouve dans C:\Program Files\MyApp, le runtime recherche les assemblys qui ne spécifient pas une base de code dans C:\Program Files\MyApp\Bin, C:\Program Files\MyApp\Bin2\Subbin et C:\Program Files\MyApp\Bin3.</span><span class="sxs-lookup"><span data-stu-id="66267-123">If the application is located at C:\Program Files\MyApp, the runtime will look for assemblies that do not specify a code base in C:\Program Files\MyApp\Bin, C:\Program Files\MyApp\Bin2\Subbin, and C:\Program Files\MyApp\Bin3.</span></span> <span data-ttu-id="66267-124">Les répertoires spécifiés dans **privatePath** doivent être des sous-répertoires du répertoire de base d’application.</span><span class="sxs-lookup"><span data-stu-id="66267-124">The directories specified in **privatePath** must be subdirectories of the application base directory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66267-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66267-125">See also</span></span>

- [<span data-ttu-id="66267-126">Assemblys dans le Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="66267-126">Assemblies in the Common Language Runtime</span></span>](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)
- [<span data-ttu-id="66267-127">Programmation à l'aide d'assemblys</span><span class="sxs-lookup"><span data-stu-id="66267-127">Programming with Assemblies</span></span>](../../../docs/framework/app-domains/programming-with-assemblies.md)
- [<span data-ttu-id="66267-128">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="66267-128">How the Runtime Locates Assemblies</span></span>](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [<span data-ttu-id="66267-129">Configuration des applications à l'aide de fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="66267-129">Configuring Apps by using Configuration Files</span></span>](index.md)
