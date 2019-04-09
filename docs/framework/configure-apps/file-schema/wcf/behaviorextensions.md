---
title: <behaviorExtensions>
ms.date: 03/30/2017
ms.assetid: 59f2791a-c78f-40d7-aa80-0d9cd10135d9
ms.openlocfilehash: 81ce9bb0e55fe4570f8a21187d9df80ea22393fe
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59191417"
---
# <a name="behaviorextensions"></a><span data-ttu-id="781c6-101">\<behaviorExtensions></span><span class="sxs-lookup"><span data-stu-id="781c6-101">\<behaviorExtensions></span></span>
<span data-ttu-id="781c6-102">Les extensions de comportement permettent la création d'éléments de comportement définis par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="781c6-102">Behavior extensions enable the user to create user-defined behavior elements.</span></span> <span data-ttu-id="781c6-103">Ces éléments peuvent être utilisés avec les éléments de comportement standard Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="781c6-103">These elements can be used alongside the standard Windows Communication Foundation (WCF) behavior elements.</span></span> <span data-ttu-id="781c6-104">La section `behaviorExtensions` définit l'élément tel qu'il peut être utilisé dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="781c6-104">The `behaviorExtensions` section defines the element such that it can be used in configuration.</span></span> <span data-ttu-id="781c6-105">Voici un exemple d'une extension de comportement typique.</span><span class="sxs-lookup"><span data-stu-id="781c6-105">Here is an example of a typical behavior extension.</span></span>  
  
```xml  
<system.serviceModel>
  <extensions>
    <behaviorExtensions>
      <add name="myBehavior"
           type="Microsoft.ServiceModel.Samples.MyBehaviorSection, MyBehavior,
                 Version=1.0.0.0, Culture=neutral, PublicKeyToken=null" />
    </behaviorExtensions>
  </extensions>
</system.serviceModel>
```  
  
 <span data-ttu-id="781c6-106">Pour ajouter des capacités de configuration à l'élément, vous devez écrire et enregistrer un élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="781c6-106">To add configuration abilities to the element, you need to write and register a configuration element.</span></span> <span data-ttu-id="781c6-107">Pour plus d'informations, consultez la documentation <xref:System.Configuration>.</span><span class="sxs-lookup"><span data-stu-id="781c6-107">For more information on this, see the <xref:System.Configuration> documentation.</span></span>  
  
 <span data-ttu-id="781c6-108">Après la définition de l’élément et de son type de configuration, l’extension peut être utilisée comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="781c6-108">After the element and its configuration type are defined, the extension can be used, as shown in the following example.</span></span>  
  
```xml  
<behaviors>
  <behavior configurationName="testChannelBehavior">
    <myBehavior />
    <channelSecurity cacheCookies="false"
                     detectReplays="false"
                     maxCachedNonces="9"
                     maxClockSkew="00:00:03"
                     maxCookieCachingTime="00:07:24"
                     replayWindow="00:07:22.2190000" />
  </behavior>
</behaviors>
```  
  
## <a name="security"></a><span data-ttu-id="781c6-109">Sécurité</span><span class="sxs-lookup"><span data-stu-id="781c6-109">Security</span></span>  
 <span data-ttu-id="781c6-110">Il est fortement recommandé d'utiliser des noms d'assembly qualifiés complets lors de l'enregistrement de types dans les fichiers `machine.config` et `app.config`.</span><span class="sxs-lookup"><span data-stu-id="781c6-110">It is strongly recommended that you use fully qualified assembly names when registering types in the `machine.config` and `app.config` files.</span></span> <span data-ttu-id="781c6-111">Si le type n'est pas défini uniquement, le chargeur de type CLR le recherche dans les emplacements suivants dans l'ordre spécifié :</span><span class="sxs-lookup"><span data-stu-id="781c6-111">If the type is not uniquely defined, the CLR type loader searches for it in the following locations in the specified order:</span></span>  
  
 <span data-ttu-id="781c6-112">Si l'assembly du type est connu, le chargeur recherche les emplacements de redirection du fichier de configuration, GAC, l'assembly actuel à l'aide d'informations de configuration, et du répertoire de base de l'application.</span><span class="sxs-lookup"><span data-stu-id="781c6-112">If the assembly of the type is known, the loader searches the configuration file's redirect locations, GAC, the current assembly using configuration information, and the application base directory.</span></span> <span data-ttu-id="781c6-113">Si l'assembly est inconnu, le chargeur recherche l'assembly actuel, mscorlib, et l'emplacement retourné par le gestionnaire d'événements `TypeResolve`.</span><span class="sxs-lookup"><span data-stu-id="781c6-113">If the assembly is unknown, the loader searches the current assembly, mscorlib, and the location returned by the `TypeResolve` event handler.</span></span> <span data-ttu-id="781c6-114">Cet ordre de recherche du CLR peut être modifié avec les raccordements tels que le mécanisme de transfert de type et l'événement AppDomain.TypeResolve.</span><span class="sxs-lookup"><span data-stu-id="781c6-114">This CLR search order can be modified with hooks such as the Type Forwarding mechanism and the AppDomain.TypeResolve event.</span></span>  
  
 <span data-ttu-id="781c6-115">Un intrus peut exploiter l'ordre de recherche du CLR et exécuter le code non autorisé.</span><span class="sxs-lookup"><span data-stu-id="781c6-115">An attacker can exploit the CLR search order and execute unauthorized code.</span></span> <span data-ttu-id="781c6-116">L'utilisation de noms (forts) qualifiés complets identifie uniquement un type et augmente considérablement la sécurité de votre système.</span><span class="sxs-lookup"><span data-stu-id="781c6-116">Using fully qualified (strong) names uniquely identifies a type and further increases security of your system.</span></span>  
  
 <span data-ttu-id="781c6-117">Pour plus d’informations, consultez [méthode de localisation des assemblys par le Runtime](https://go.microsoft.com/fwlink/?LinkId=95336) et <xref:System.AppDomain.TypeResolve>.</span><span class="sxs-lookup"><span data-stu-id="781c6-117">For more information, see [How the Runtime Locates Assemblies](https://go.microsoft.com/fwlink/?LinkId=95336) and <xref:System.AppDomain.TypeResolve>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="781c6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="781c6-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.BehaviorExtensionElement>
- [<span data-ttu-id="781c6-119">Configuration et extension de l'exécution à l'aide de comportements</span><span class="sxs-lookup"><span data-stu-id="781c6-119">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)
