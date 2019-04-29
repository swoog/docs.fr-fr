---
title: 'Procédure : Localiser des assemblys à l’aide de DEVPATH'
ms.date: 03/30/2017
helpviewer_keywords:
- DEVPATH
- .NET Framework application configuration, assemblies
- application configuration files, specifying assembly's location
- app.config files, assembly locations
- locating assemblies
- assemblies [.NET Framework], location
ms.assetid: 44d2eadf-7eec-443c-a2ac-d601fd919e17
ms.openlocfilehash: 5c4041f42b0a9d1d1e4bc8438e662911534daa42
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775828"
---
# <a name="how-to-locate-assemblies-by-using-devpath"></a><span data-ttu-id="fff2f-102">Procédure : Localiser des assemblys à l’aide de DEVPATH</span><span class="sxs-lookup"><span data-stu-id="fff2f-102">How to: Locate Assemblies by Using DEVPATH</span></span>
<span data-ttu-id="fff2f-103">Les développeurs peuvent souhaiter vous assurer qu’un assembly partagé, qu'ils créent fonctionne correctement avec plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="fff2f-103">Developers might want to make sure that a shared assembly they are building works correctly with multiple applications.</span></span> <span data-ttu-id="fff2f-104">Au lieu de mettre en permanence l’assembly dans le global assembly cache au cours du cycle de développement, le développeur peut créer une variable d’environnement DEVPATH qui pointe vers le répertoire de sortie pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="fff2f-104">Instead of continually putting the assembly in the global assembly cache during the development cycle, the developer can create a DEVPATH environment variable that points to the build output directory for the assembly.</span></span>  
  
 <span data-ttu-id="fff2f-105">Par exemple, supposons que vous générez un assembly partagé appelé MySharedAssembly et le répertoire de sortie soit C:\MySharedAssembly\Debug.</span><span class="sxs-lookup"><span data-stu-id="fff2f-105">For example, assume that you are building a shared assembly called MySharedAssembly and the output directory is C:\MySharedAssembly\Debug.</span></span> <span data-ttu-id="fff2f-106">Vous pouvez placer C:\MySharedAssembly\Debug dans la variable DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fff2f-106">You can put C:\MySharedAssembly\Debug in the DEVPATH variable.</span></span> <span data-ttu-id="fff2f-107">Vous devez spécifier le [ \<developmentMode >](../../../docs/framework/configure-apps/file-schema/runtime/developmentmode-element.md) élément dans le fichier de configuration machine.</span><span class="sxs-lookup"><span data-stu-id="fff2f-107">You must then specify the [\<developmentMode>](../../../docs/framework/configure-apps/file-schema/runtime/developmentmode-element.md) element in the machine configuration file.</span></span> <span data-ttu-id="fff2f-108">Cet élément indique le common language runtime à utiliser DEVPATH pour rechercher des assemblys.</span><span class="sxs-lookup"><span data-stu-id="fff2f-108">This element tells the common language runtime to use DEVPATH to locate assemblies.</span></span>  
  
 <span data-ttu-id="fff2f-109">L’assembly partagé doit être détectable par le runtime.</span><span class="sxs-lookup"><span data-stu-id="fff2f-109">The shared assembly must be discoverable by the runtime.</span></span>  <span data-ttu-id="fff2f-110">Pour spécifier un répertoire privé pour la résolution des références d’assembly, utilisez le [ \<codeBase > élément](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) ou [ \<probing > élément](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) dans un fichier de configuration, comme décrit dans [Spécifiant l’emplacement d’un Assembly](../../../docs/framework/configure-apps/specify-assembly-location.md).</span><span class="sxs-lookup"><span data-stu-id="fff2f-110">To specify a private directory for resolving assembly references use the [\<codeBase> Element](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) or [\<probing> Element](../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md) in a configuration file, as described in [Specifying an Assembly's Location](../../../docs/framework/configure-apps/specify-assembly-location.md).</span></span>  <span data-ttu-id="fff2f-111">Vous pouvez également placer l’assembly dans un sous-répertoire du répertoire de l’application.</span><span class="sxs-lookup"><span data-stu-id="fff2f-111">You can also put the assembly in a subdirectory of the application directory.</span></span> <span data-ttu-id="fff2f-112">Pour plus d’informations, consultez [Méthode de localisation des assemblys par le runtime](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="fff2f-112">For more information, see [How the Runtime Locates Assemblies](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fff2f-113">Il s’agit d’une fonctionnalité avancée, destinée uniquement au développement.</span><span class="sxs-lookup"><span data-stu-id="fff2f-113">This is an advanced feature, intended only for development.</span></span>  
  
 <span data-ttu-id="fff2f-114">L’exemple suivant montre comment entraîner le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fff2f-114">The following example shows how to cause the runtime to search for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fff2f-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="fff2f-115">Example</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <developmentMode developerInstallation="true"/>  
  </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="fff2f-116">Ce paramètre par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="fff2f-116">This setting defaults to false.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fff2f-117">Utilisez ce paramètre uniquement au moment du développement.</span><span class="sxs-lookup"><span data-stu-id="fff2f-117">Use this setting only at development time.</span></span> <span data-ttu-id="fff2f-118">Le runtime ne vérifie pas les versions sur les assemblys avec nom fort trouvés dans DEVPATH.</span><span class="sxs-lookup"><span data-stu-id="fff2f-118">The runtime does not check the versions on strong-named assemblies found in the DEVPATH.</span></span> <span data-ttu-id="fff2f-119">Elle utilise simplement le premier assembly qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="fff2f-119">It simply uses the first assembly it finds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fff2f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fff2f-120">See also</span></span>

- [<span data-ttu-id="fff2f-121">Configuration d’applications à l’aide de fichiers de Configuration</span><span class="sxs-lookup"><span data-stu-id="fff2f-121">Configuring Apps by using Configuration Files</span></span>](index.md)
