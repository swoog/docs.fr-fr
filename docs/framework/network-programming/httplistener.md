---
title: HttpListener
ms.date: 03/30/2017
helpviewer_keywords:
- HTTP
ms.assetid: 5b89d3fb-3c9a-49e2-af1f-c34c020c68ac
ms.openlocfilehash: d3fecb9fe78ca54f68d3c5a97dae5d5dd9fbb28d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075416"
---
# <a name="httplistener"></a><span data-ttu-id="5e3c1-102">HttpListener</span><span class="sxs-lookup"><span data-stu-id="5e3c1-102">HttpListener</span></span>
<span data-ttu-id="5e3c1-103">La classe <xref:System.Net.HttpListener> fournit un écouteur de protocole HTTP contrôlé par programmation.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-103">The <xref:System.Net.HttpListener> class provides a programmatically controlled HTTP protocol listener.</span></span> <span data-ttu-id="5e3c1-104">L'écouteur est actif pendant toute la durée de vie de l'objet <xref:System.Net.HttpListener> et s'exécute au sein de votre application.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-104">The listener is active for the lifetime of the <xref:System.Net.HttpListener> object and runs within your application.</span></span>  
  
## <a name="httpsys"></a><span data-ttu-id="5e3c1-105">HTTP.SYS</span><span class="sxs-lookup"><span data-stu-id="5e3c1-105">HTTP.SYS</span></span>  
 <span data-ttu-id="5e3c1-106">La classe <xref:System.Net.HttpListener> repose sur HTTP.sys, qui est l'écouteur en mode noyau qui gère tout le trafic HTTP pour Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-106">The <xref:System.Net.HttpListener> class is built on top of HTTP.sys, which is the kernel mode listener that handles all HTTP traffic for Windows.</span></span> <span data-ttu-id="5e3c1-107">HTTP.sys assure la gestion des connexions, la limitation de la bande passante et la journalisation du serveur web.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-107">HTTP.sys provides connection management, bandwidth throttling, and Web server logging.</span></span> <span data-ttu-id="5e3c1-108">Utilisez l'outil `HttpCfg.exe` pour ajouter des certificats SSL.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-108">Use the `HttpCfg.exe` tool to add SSL certificates.</span></span> <span data-ttu-id="5e3c1-109">Pour plus d’informations, consultez les explications sur l’outil [HttpCfg.exe](https://go.microsoft.com/fwlink/?LinkID=178284) dans la documentation du [serveur](https://go.microsoft.com/fwlink/?LinkID=178285).</span><span class="sxs-lookup"><span data-stu-id="5e3c1-109">For more information, see the documentation on the [HttpCfg.exe](https://go.microsoft.com/fwlink/?LinkID=178284) tool in the [Server](https://go.microsoft.com/fwlink/?LinkID=178285) documentation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e3c1-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e3c1-110">See also</span></span>

- <xref:System.Net.HttpListener>
- <xref:System.Net.HttpWebRequest>
- <xref:System.Net.HttpWebResponse>
- [<span data-ttu-id="5e3c1-111">Serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="5e3c1-111">HTTP Server</span></span>](https://go.microsoft.com/fwlink/?LinkID=178285)
- [<span data-ttu-id="5e3c1-112">Améliorations apportées à la sécurité des informations Internet</span><span class="sxs-lookup"><span data-stu-id="5e3c1-112">Security Enhancements in Internet Information</span></span>](https://go.microsoft.com/fwlink/?LinkID=178286)
- [<span data-ttu-id="5e3c1-113">Exemple d’application hôte ASPX HttpListener</span><span class="sxs-lookup"><span data-stu-id="5e3c1-113">HttpListener ASPX Host Application Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=179560)
- [<span data-ttu-id="5e3c1-114">Exemple de technologie HttpListener</span><span class="sxs-lookup"><span data-stu-id="5e3c1-114">HttpListener Technology Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=179558)
- [<span data-ttu-id="5e3c1-115">Exemples de programmation réseau</span><span class="sxs-lookup"><span data-stu-id="5e3c1-115">Network Programming Samples</span></span>](../../../docs/framework/network-programming/network-programming-samples.md)
