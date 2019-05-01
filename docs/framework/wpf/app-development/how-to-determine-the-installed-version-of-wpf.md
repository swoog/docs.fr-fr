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
# <a name="how-to-determine-the-installed-version-of-wpf"></a>Procédure : Déterminer la version installée de WPF
Le numéro de version pour la version actuellement installée de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] se trouve dans le **Registre**.  
  
 Pour trouver le numéro de version :  
  
1. Dans le menu **Démarrer** , cliquez sur **Exécuter**.  
  
2. Dans **Open**, type **regedit.exe**.  
  
3. Ouvrez la clé suivante :  
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v3.0\Setup\Windows Presentation Foundation`  
  
 Le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] numéro de version est stocké dans le **Version** valeur.
