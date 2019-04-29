---
title: Exceptions d'hébergement
ms.date: 03/30/2017
ms.assetid: ad9e14f8-fa17-4d59-b365-fe0e7ec17c98
ms.openlocfilehash: f2bc7d0ca09faa2598990437295d1abf0cff3c45
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61934730"
---
# <a name="hosting-exceptions"></a>Exceptions d'hébergement
Cette rubrique répertorie toutes les exceptions générées par l'hébergement.  
  
## <a name="exception-list"></a>Liste des exceptions  
  
|Code de la ressource|Chaîne de la ressource|  
|-------------------|---------------------|  
|Hosting_AddressIsAbsoluteUri|L'URI complet n'est pas autorisé. Les URI complets ne sont pas pris en compte pour l'API ServiceHostingEnvironment.EnsureServiceAvailable. Utilisez un chemin d'accès virtuel pour le service correspondant.|  
|Hosting_BuildProviderCouldNotCreateType|Le type CLR spécifié ne peut pas être chargé pendant la compilation de service. Vérifiez que ce type n’est défini dans un fichier source situé dans l’application \\répertoire \App_Code, contenu dans un assembly compilé situé dans l’application \\\bin répertoire ou présent dans un assembly installé dans le Global Assembly Cache. Le nom du type respecte la casse. Les répertoires comme \\\App_Code et \\\bin doit se trouver dans le répertoire racine de l’application. Le \\\App_Code et \\\bin répertoires ne peuvent pas être imbriquées dans les sous-répertoires.|
