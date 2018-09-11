---
title: '&lt;behaviorExtensions&gt;'
ms.date: 03/30/2017
ms.assetid: 59f2791a-c78f-40d7-aa80-0d9cd10135d9
ms.openlocfilehash: d025497956715913923e839cb6c482f44f96babb
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44353120"
---
# <a name="ltbehaviorextensionsgt"></a><span data-ttu-id="1f725-102">&lt;behaviorExtensions&gt;</span><span class="sxs-lookup"><span data-stu-id="1f725-102">&lt;behaviorExtensions&gt;</span></span>
<span data-ttu-id="1f725-103">Les extensions de comportement permettent la création d’éléments de comportement définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f725-103">Behavior extensions enable the user to create user-defined behavior elements.</span></span> <span data-ttu-id="1f725-104">Ces éléments peuvent être utilisés avec les éléments de comportement standard Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="1f725-104">These elements can be used alongside the standard Windows Communication Foundation (WCF) behavior elements.</span></span> <span data-ttu-id="1f725-105">La section `behaviorExtensions` définit l'élément tel qu'il peut être utilisé dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="1f725-105">The `behaviorExtensions` section defines the element such that it can be used in configuration.</span></span> <span data-ttu-id="1f725-106">Voici un exemple d'une extension de comportement typique.</span><span class="sxs-lookup"><span data-stu-id="1f725-106">Here is an example of a typical behavior extension.</span></span>  
  
```xml  
<system.serviceModel>  
    <extensions>  
        <behaviorExtensions>  
            <add name="myBehavior" type="Microsoft.ServiceModel.Samples.MyBehaviorSection, MyBehavior,  
                Version=1.0.0.0, Culture=neutral, PublicKeyToken=null" />  
       </behaviorExtensions>  
    </extensions>  
</system.serviceModel>  
```  
  
 <span data-ttu-id="1f725-107">Pour ajouter des capacités de configuration à l'élément, vous devez écrire et enregistrer un élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="1f725-107">To add configuration abilities to the element, you need to write and register a configuration element.</span></span> <span data-ttu-id="1f725-108">Pour plus d'informations, consultez la documentation <xref:System.Configuration>.</span><span class="sxs-lookup"><span data-stu-id="1f725-108">For more information on this, see the <xref:System.Configuration> documentation.</span></span>  
  
 <span data-ttu-id="1f725-109">Après la définition de l'élément et de son type de configuration, l'extension peut être utilisée comme dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="1f725-109">After the element and its configuration type are defined, the extension can be used, as shown in the following example.</span></span>  
  
```xml  
<behaviors>  
    <behavior configurationName="testChannelBehavior">  
        <myBehavior />  
        <channelSecurity cacheCookies="false" detectReplays="false" maxCachedNonces="9"  
            maxClockSkew="00:00:03" maxCookieCachingTime="00:07:24" replayWindow="00:07:22.2190000" />  
    </behavior>  
</behaviors>  
```  
  
## <a name="security"></a><span data-ttu-id="1f725-110">Sécurité</span><span class="sxs-lookup"><span data-stu-id="1f725-110">Security</span></span>  
 <span data-ttu-id="1f725-111">Il est fortement recommandé d'utiliser des noms d'assembly qualifiés complets lors de l'enregistrement de types dans les fichiers `machine.config` et `app.config`.</span><span class="sxs-lookup"><span data-stu-id="1f725-111">It is strongly recommended that you use fully qualified assembly names when registering types in the `machine.config` and `app.config` files.</span></span> <span data-ttu-id="1f725-112">Si le type n'est pas défini uniquement, le chargeur de type CLR le recherche dans les emplacements suivants dans l'ordre spécifié :</span><span class="sxs-lookup"><span data-stu-id="1f725-112">If the type is not uniquely defined, the CLR type loader searches for it in the following locations in the specified order:</span></span>  
  
 <span data-ttu-id="1f725-113">Si l'assembly du type est connu, le chargeur recherche les emplacements de redirection du fichier de configuration, GAC, l'assembly actuel à l'aide d'informations de configuration, et du répertoire de base de l'application.</span><span class="sxs-lookup"><span data-stu-id="1f725-113">If the assembly of the type is known, the loader searches the configuration file's redirect locations, GAC, the current assembly using configuration information, and the application base directory.</span></span> <span data-ttu-id="1f725-114">Si l'assembly est inconnu, le chargeur recherche l'assembly actuel, mscorlib, et l'emplacement retourné par le gestionnaire d'événements `TypeResolve`.</span><span class="sxs-lookup"><span data-stu-id="1f725-114">If the assembly is unknown, the loader searches the current assembly, mscorlib, and the location returned by the `TypeResolve` event handler.</span></span> <span data-ttu-id="1f725-115">Cet ordre de recherche du CLR peut être modifié avec les raccordements tels que le mécanisme de transfert de type et l'événement AppDomain.TypeResolve.</span><span class="sxs-lookup"><span data-stu-id="1f725-115">This CLR search order can be modified with hooks such as the Type Forwarding mechanism and the AppDomain.TypeResolve event.</span></span>  
  
 <span data-ttu-id="1f725-116">Un intrus peut exploiter l'ordre de recherche du CLR et exécuter le code non autorisé.</span><span class="sxs-lookup"><span data-stu-id="1f725-116">An attacker can exploit the CLR search order and execute unauthorized code.</span></span> <span data-ttu-id="1f725-117">L'utilisation de noms (forts) qualifiés complets identifie uniquement un type et augmente considérablement la sécurité de votre système.</span><span class="sxs-lookup"><span data-stu-id="1f725-117">Using fully qualified (strong) names uniquely identifies a type and further increases security of your system.</span></span>  
  
 <span data-ttu-id="1f725-118">Pour plus d’informations, consultez [méthode de localisation des assemblys par le Runtime](https://go.microsoft.com/fwlink/?LinkId=95336) et <xref:System.AppDomain.TypeResolve>.</span><span class="sxs-lookup"><span data-stu-id="1f725-118">For more information, see [How the Runtime Locates Assemblies](https://go.microsoft.com/fwlink/?LinkId=95336) and <xref:System.AppDomain.TypeResolve>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f725-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f725-119">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BehaviorExtensionElement>  
 [<span data-ttu-id="1f725-120">Configuration et extension de l’exécution à l’aide de comportements</span><span class="sxs-lookup"><span data-stu-id="1f725-120">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)
