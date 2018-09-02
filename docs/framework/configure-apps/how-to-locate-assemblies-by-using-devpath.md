---
title: "Comment : localiser des assemblys à l'aide de DEVPATH"
ms.date: 03/30/2017
helpviewer_keywords:
- DEVPATH
- .NET Framework application configuration, assemblies
- application configuration files, specifying assembly's location
- app.config files, assembly locations
- locating assemblies
- assemblies [.NET Framework], location
ms.assetid: 44d2eadf-7eec-443c-a2ac-d601fd919e17
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 9b8e3c89c13e7f5c294afca54af7f63293653e87
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43408786"
---
# <a name="how-to-locate-assemblies-by-using-devpath"></a><span data-ttu-id="5517c-102">Comment : localiser des assemblys à l'aide de DEVPATH</span><span class="sxs-lookup"><span data-stu-id="5517c-102">How to: Locate Assemblies by Using DEVPATH</span></span>
<span data-ttu-id="5517c-103">Les développeurs peuvent souhaiter vous assurer qu’un assembly partagé, qu'ils créent fonctionne correctement avec plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="5517c-103">Developers might want to make sure that a shared assembly they are building works correctly with multiple applications.</span></span> <span data-ttu-id="5517c-104">Au lieu de mettre en permanence l’assembly dans le global assembly cache au cours du cycle de développement, le développeur peut créer une variable d’environnement DEVPATH qui pointe vers le répertoire de sortie pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5517c-104">Instead of continually putting the assembly in the global assembly cache during the development cycle, the developer can create a DEVPATH environment variable that points to the build output directory for the assembly.</span></span>  
  
 <span data-ttu-id="5517c-105">Par exemple, supposons que vous générez un assembly partagé appelé MySharedAssembly et le répertoire de sortie soit C:\MySharedAssembly\Debug.</span><span class="sxs-lookup"><span data-stu-id="5517c-105">For example, assume that you are building a shared assembly called MySharedAssembly and the output directory is C:\MySharedAssembly\Debug.</span></span> <span data-ttu-id="5517c-106">Vous pouvez placer C:\MySharedAssembly\Debug dans la variable DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="5517c-106">You can put C:\MySharedAssembly\Debug in the DEVPATH variable.</span></span> <span data-ttu-id="5517c-107">Vous devez spécifier le [ \<developmentMode >](../../../docs/framework/configure-apps/file-schema/runtime/developmentmode-element.md) élément dans le fichier de configuration machine.</span><span class="sxs-lookup"><span data-stu-id="5517c-107">You must then specify the [\<developmentMode>](../../../docs/framework/configure-apps/file-schema/runtime/developmentmode-element.md) element in the machine configuration file.</span></span> <span data-ttu-id="5517c-108">Cet élément indique le common language runtime à utiliser DEVPATH pour rechercher des assemblys.</span><span class="sxs-lookup"><span data-stu-id="5517c-108">This element tells the common language runtime to use DEVPATH to locate assemblies.</span></span>  
  
 <span data-ttu-id="5517c-109">L’assembly partagé doit être détectable par le runtime.</span><span class="sxs-lookup"><span data-stu-id="5517c-109">The shared assembly must be discoverable by the runtime.</span></span>  <span data-ttu-id="5517c-110">Pour spécifier un répertoire privé pour la résolution des références d’assembly, utilisez le [ \<codeBase > élément](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) ou [ \<probing > élément](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) dans un fichier de configuration, comme décrit dans [Spécifiant l’emplacement d’un Assembly](../../../docs/framework/configure-apps/specify-assembly-location.md).</span><span class="sxs-lookup"><span data-stu-id="5517c-110">To specify a private directory for resolving assembly references use the [\<codeBase> Element](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) or [\<probing> Element](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) in a configuration file, as described in [Specifying an Assembly's Location](../../../docs/framework/configure-apps/specify-assembly-location.md).</span></span>  <span data-ttu-id="5517c-111">Vous pouvez également placer l’assembly dans un sous-répertoire du répertoire de l’application.</span><span class="sxs-lookup"><span data-stu-id="5517c-111">You can also put the assembly in a subdirectory of the application directory.</span></span> <span data-ttu-id="5517c-112">Pour plus d’informations, consultez [Méthode de localisation des assemblys par le runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="5517c-112">For more information, see [How the Runtime Locates Assemblies](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5517c-113">Il s’agit d’une fonctionnalité avancée, destinée uniquement au développement.</span><span class="sxs-lookup"><span data-stu-id="5517c-113">This is an advanced feature, intended only for development.</span></span>  
  
 <span data-ttu-id="5517c-114">L’exemple suivant montre comment entraîner le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="5517c-114">The following example shows how to cause the runtime to search for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5517c-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="5517c-115">Example</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <developmentMode developerInstallation="true"/>  
  </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="5517c-116">Ce paramètre par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="5517c-116">This setting defaults to false.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5517c-117">Utilisez ce paramètre uniquement au moment du développement.</span><span class="sxs-lookup"><span data-stu-id="5517c-117">Use this setting only at development time.</span></span> <span data-ttu-id="5517c-118">Le runtime ne vérifie pas les versions sur les assemblys avec nom fort trouvés dans DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="5517c-118">The runtime does not check the versions on strong-named assemblies found in the DEVPATH.</span></span> <span data-ttu-id="5517c-119">Elle utilise simplement le premier assembly qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="5517c-119">It simply uses the first assembly it finds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5517c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5517c-120">See Also</span></span>  
 [<span data-ttu-id="5517c-121">Configuration des applications .NET Framework</span><span class="sxs-lookup"><span data-stu-id="5517c-121">Configuring .NET Framework Apps</span></span>](https://msdn.microsoft.com/library/d789b592-fcb5-4e3d-8ac9-e0299adaaa42)
