---
title: 'Procédure : Déterminer la version installée de WPF'
ms.date: 03/30/2017
helpviewer_keywords:
- version [WPF], finding
ms.assetid: 99971cef-e218-4f9f-a4c1-350332741860
ms.openlocfilehash: ffbd9a4c7f66dff9c8773dff4259551e20aa963d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052454"
---
# <a name="how-to-determine-the-installed-version-of-wpf"></a><span data-ttu-id="dabb3-102">Procédure : Déterminer la version installée de WPF</span><span class="sxs-lookup"><span data-stu-id="dabb3-102">How to: Determine the Installed Version of WPF</span></span>
<span data-ttu-id="dabb3-103">Le numéro de version pour la version actuellement installée de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] se trouve dans le **Registre**.</span><span class="sxs-lookup"><span data-stu-id="dabb3-103">The version number for the current installed version of [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] is located in the **Registry**.</span></span>  
  
 <span data-ttu-id="dabb3-104">Pour trouver le numéro de version :</span><span class="sxs-lookup"><span data-stu-id="dabb3-104">To find the version number:</span></span>  
  
1. <span data-ttu-id="dabb3-105">Dans le menu **Démarrer** , cliquez sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="dabb3-105">On the **Start** menu, click **Run**.</span></span>  
  
2. <span data-ttu-id="dabb3-106">Dans **Open**, type **regedit.exe**.</span><span class="sxs-lookup"><span data-stu-id="dabb3-106">In **Open**, type **regedit.exe**.</span></span>  
  
3. <span data-ttu-id="dabb3-107">Ouvrez la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="dabb3-107">Open the following key:</span></span>  
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v3.0\Setup\Windows Presentation Foundation`  
  
 <span data-ttu-id="dabb3-108">Le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] numéro de version est stocké dans le **Version** valeur.</span><span class="sxs-lookup"><span data-stu-id="dabb3-108">The [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] version number is stored in the **Version** value.</span></span>
