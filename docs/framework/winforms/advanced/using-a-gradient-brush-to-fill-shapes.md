---
title: Utilisation d'un pinceau à dégradé pour remplir des formes
ms.date: 03/30/2017
helpviewer_keywords:
- brushes [Windows Forms], gradient brushes
- gradient brushes
- examples [Windows Forms], gradient brushes
ms.assetid: 2c6037b9-05bd-44c0-a22a-19584b722524
ms.openlocfilehash: 5771aaabd283d71f5fa6934f86a1c24a57f38dca
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61954470"
---
# <a name="using-a-gradient-brush-to-fill-shapes"></a>Utilisation d'un pinceau à dégradé pour remplir des formes
Vous pouvez utiliser un pinceau de dégradé pour remplir une forme avec une couleur. Par exemple, vous pouvez utiliser un dégradé horizontal pour remplir une forme avec une couleur qui change graduellement à mesure que vous déplacez le bord gauche de la forme vers le bord droit. Imaginez un rectangle avec un bord gauche qui est noir (représenté par les composants rouges, vert et bleus 0, 0, 0) et un bord droit de rouge (représenté par 255, 0, 0). Si le rectangle est 256 pixels de large, le composant rouge d’un pixel donné sera égale à celle de la composante rouge de pixel à sa gauche. Le pixel de gauche dans une ligne a des composants de couleur (0, 0, 0), le deuxième pixel a (1, 0, 0), le troisième pixel (2, 0, 0) et ainsi de suite, jusqu'à ce que vous arriviez au pixel plus à droite, ce qui a des composants de couleur (255, 0, 0). Ces valeurs de couleur interpolée composent le dégradé de couleur.  
  
 Un dégradé linéaire change de couleur quand vous déplacez horizontalement, verticalement ou parallèlement à une ligne inclinée spécifiée. Un dégradé de tracé change de couleur quand vous déplacez sur l’intérieur et de la limite d’un chemin d’accès. Vous pouvez personnaliser les dégradés de chemin d’accès pour obtenir une grande variété d’effets.  
  
 L’illustration suivante montre un rectangle rempli avec un pinceau dégradé linéaire et une ellipse remplie avec un pinceau de dégradé de chemin d’accès.  
  
 ![Gradient](./media/gradient2.png "gradient2")  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Créer un dégradé linéaire](how-to-create-a-linear-gradient.md)  
 Montre comment créer un dégradé linéaire en utilisant la <xref:System.Drawing.Drawing2D.LinearGradientBrush> classe.  
  
 [Guide pratique pour Créer un dégradé de tracé](how-to-create-a-path-gradient.md)  
 Décrit comment créer un dégradé de chemin d’accès à l’aide la <xref:System.Drawing.Drawing2D.PathGradientBrush> classe.  
  
 [Guide pratique pour Appliquer une Correction Gamma à un dégradé](how-to-apply-gamma-correction-to-a-gradient.md)  
 Explique comment utiliser la correction gamma avec un pinceau de dégradé.  
  
## <a name="reference"></a>Référence  
 <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>  
 Contient une description de cette classe et propose des liens vers tous ses membres.  
  
 <xref:System.Drawing.Drawing2D.PathGradientBrush?displayProperty=nameWithType>  
 Contient une description de cette classe et propose des liens vers tous ses membres.
