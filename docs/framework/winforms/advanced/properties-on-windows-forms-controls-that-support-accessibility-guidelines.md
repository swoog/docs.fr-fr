---
title: Propriétés des contrôles Windows Forms que prennent en charge les instructions relatives à l'accessibilité
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, accessibility properties of controls
- accessibility [Windows Forms], Windows Forms control properties
ms.assetid: ad3567a6-313b-4708-9e15-f487a831f049
ms.openlocfilehash: eee7499373809538355227633ab9a1a66aedb9ed
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716398"
---
# <a name="properties-on-windows-forms-controls-that-support-accessibility-guidelines"></a>Propriétés des contrôles Windows Forms que prennent en charge les instructions relatives à l'accessibilité
Contrôles sur la boîte à outils standard pour les Windows Forms prennent en charge de nombreuses règles d’accessibilité, y compris l’exposition du focus clavier et l’exposition des éléments de l’écran.  
  
## <a name="planning-ahead-for-accessibility"></a>Planification de l’accessibilité  
 Les propriétés des contrôles peuvent être utilisées pour prendre en charge d’autres règles d’accessibilité comme indiqué dans le tableau suivant. En outre, vous devez utiliser des menus pour fournir l’accès aux composants du programme.  
  
|Propriété du contrôle|Considérations d’accessibilité|  
|----------------------|--------------------------------------|  
|AccessibleDescription|La description est signalée à l’accessibilité, notamment des lecteurs d’écran. Les aides à l’accessibilité sont des programmes et des dispositifs spécialisés qui aident les personnes handicapées à utiliser plus efficacement les ordinateurs.|  
|AccessibleName|Le nom qui sera signalé pour les options d’accessibilité.|  
|AccessibleRole|Décrit l’utilisation de l’élément dans l’interface utilisateur.|  
|TabIndex|Crée un chemin de navigation cohérent dans le formulaire. Il est important pour les contrôles sans les étiquettes intrinsèques, tels que les zones de texte, pour que leur étiquette associée les précède immédiatement dans l’ordre de tabulation.|  
|Texte|Utilisez le caractère « & » pour créer des clés d’accès. À l’aide de clés d’accès est la partie de l’accès clavier documenté aux fonctionnalités.|  
|Taille de police|Si la taille de police n’est pas réglable, elle doit être la valeur à 10 points ou plus. Une fois que la taille de police du formulaire est définie, tous les contrôles ajoutés au formulaire par la suite auront la même taille.|  
|ForeColor|Si cette propriété est définie à la valeur par défaut, puis Préférences de couleur de l’utilisateur seront utilisés sur le formulaire.|  
|BackColor|Si cette propriété est définie à la valeur par défaut, puis Préférences de couleur de l’utilisateur seront utilisés sur le formulaire.|  
|BackgroundImage|Ne renseignez pas cette propriété pour rendre le texte plus lisible.|  
  
## <a name="see-also"></a>Voir aussi
- [Procédure pas à pas : Création d’une Application Windows Accessible](walkthrough-creating-an-accessible-windows-based-application.md)
