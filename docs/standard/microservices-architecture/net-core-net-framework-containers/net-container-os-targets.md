---
title: Quel système d’exploitation cibler avec les conteneurs .NET
description: Architecture de microservices .NET pour les applications .NET en conteneur | Quel système d’exploitation cibler avec les conteneurs .NET
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/11/2018
ms.openlocfilehash: b2ae1d2e732f152133dd8a8757b955e05cdd88eb
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45970823"
---
# <a name="what-os-to-target-with-net-containers"></a>Quel système d’exploitation cibler avec les conteneurs .NET

Compte tenu de la diversité des systèmes d’exploitation pris en charge par Docker et des différences entre .NET Framework et .NET Core, vous avez tout intérêt à cibler le système d’exploitation et la version en fonction du framework que vous utilisez.

Pour Windows, vous pouvez utiliser Windows Server Core ou Windows Nano Server. Ces versions de Windows offrent des caractéristiques différentes (IIS dans Windows Server Core et un serveur web auto-hébergé comme Kestrel dans Nano Server) qui peuvent être nécessaires à .NET Framework ou .NET Core, respectivement.

Pour Linux, plusieurs distributions sont disponibles et prises en charge dans les images .NET Docker officielles (comme Debian).

La figure 3-1 indique la version du système d’exploitation à utiliser en fonction de la version du .NET Framework utilisée.

![Lorsque vous déployez des applications .NET Framework héritées, vous devez cibler Windows Server Core, compatible avec les applications héritées et IIS, qui a une image plus grande. Lorsque vous déployez des applications .NET Core, vous pouvez cibler Windows Nano Server, optimisé pour le cloud, qui utilise Kestrel, est plus petit et démarre plus rapidement. Vous pouvez également cibler Linux, prenant en charge Debian, Alpine et d’autres. Utilise également Kestrel, est plus petit et démarre plus rapidement.](./media/image1.png)

**Figure 3-1** : systèmes d’exploitation à cibler en fonction des versions de .NET Framework

Vous pouvez aussi créer votre propre image Docker si souhaitez utiliser une autre distribution Linux ou une image contenant des versions non fournies par Microsoft. Par exemple, vous pouvez créer une image avec ASP.NET Core s’exécutant sur le .NET Framework classique et Windows Server Core, ce qui n’est pas un scénario très courant pour Docker.

Au moment d’ajouter le nom de l’image à votre fichier Dockerfile, vous pouvez sélectionner le système d’exploitation et la version en fonction de la balise que vous utilisez, comme dans les exemples suivants :

<table>
<thead>
<tr class="header">
<th>Image</th>
<th>Commentaires</th>
</tr>
</thead>
<tbody>
<tr>
<td>microsoft/dotnet:2.1-runtime</td>
<td>Multi-architecture .NET Core 2.1 : prend en charge Linux et Windows Nano Server en fonction de l’hôte Docker.</td>
</tr>
<tr class="odd">
<td>microsoft/dotnet:2.1-aspnetcore-runtime</td>
<td><p>Multi-architecture ASP.NET Core 2.1 : prend en charge Linux et Windows Nano Server en fonction de l’hôte Docker.</p>
<p>L’image aspnetcore a quelques optimisations pour ASP.NET Core.</p></td>
</tr>
<tr class="even">
<td>microsoft/dotnet:2.1-aspnetcore-runtime-alpine</td>
<td>Runtime .NET Core 2.1 uniquement sur la distribution Linux Alpine</td>
</tr>
<tr class="odd">
<td>microsoft/dotnet:2.1-aspnetcore-runtime-nanoserver-1803</td>
<td>Runtime .NET Core 2.1 uniquement sur Windows Nano Server (Windows Server version 1803)</td>
</tr>
</tbody>
</table>

>[!div class="step-by-step"]
[Précédent](container-framework-choice-factors.md)
[Suivant](official-net-docker-images.md)
