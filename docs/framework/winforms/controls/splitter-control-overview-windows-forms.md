---
title: Vue d'ensemble du contrôle Splitter (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Splitter
helpviewer_keywords:
- Splitter control [Windows Forms], about Splitter control
ms.assetid: e2b6ab83-dfdd-40ec-9762-850702c82dcb
ms.openlocfilehash: 2e3e46c9d4cf118bb846e5d9efefeb0d57fea567
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703190"
---
# <a name="splitter-control-overview-windows-forms"></a>Vue d'ensemble du contrôle Splitter (Windows Forms)
> [!IMPORTANT]
>  Bien que <xref:System.Windows.Forms.SplitContainer> remplace et ajoute des fonctionnalités au contrôle <xref:System.Windows.Forms.Splitter> des versions antérieures, <xref:System.Windows.Forms.Splitter> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.  
  
 Windows Forms <xref:System.Windows.Forms.Splitter> contrôles servent à redimensionner des contrôles ancrés au moment de l’exécution. Le <xref:System.Windows.Forms.Splitter> contrôle est souvent utilisé dans les formulaires avec des contrôles qui ont différentes longueurs de données à présenter, comme dans l’Explorateur Windows, dont les volets de données contiennent des informations de longueur différente à différents moments.  
  
## <a name="working-with-the-splitter-control"></a>Utilisation du contrôle Splitter  
 Lorsque l’utilisateur pointe le pointeur de la souris sur le bord non ancré d’un contrôle qui peut être redimensionné par un contrôle splitter, le pointeur change d’apparence pour indiquer que le contrôle peut être redimensionné. Avec le contrôle splitter, l’utilisateur peut redimensionner le contrôle ancré qui précède immédiatement. Par conséquent, pour permettre à l’utilisateur redimensionner un contrôle fixé au moment de l’exécution, le contrôle soit redimensionné à un bord d’un conteneur d’ancrage et puis ancrer un contrôle splitter sur le même côté de ce conteneur.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.SplitContainer>
- [Guide pratique pour Ancrer des contrôles aux Windows Forms](how-to-dock-controls-on-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
