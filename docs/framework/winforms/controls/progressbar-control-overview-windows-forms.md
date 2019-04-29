---
title: Vue d'ensemble du contrôle ProgressBar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ProgressBar
helpviewer_keywords:
- ProgressBar control [Windows Forms], about ProgressBar control
- progress controls [Windows Forms], about progress controls
ms.assetid: a05d9cba-3a6a-4f8f-94b8-8ec12799fb80
ms.openlocfilehash: 24b47669cdf8ed0a8f0f936b0b3b9c354e62445f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61666343"
---
# <a name="progressbar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle ProgressBar (Windows Forms)
> [!IMPORTANT]
>  Le contrôle <xref:System.Windows.Forms.ToolStripProgressBar> remplace le contrôle <xref:System.Windows.Forms.ProgressBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.ProgressBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.  
  
 Les formulaires Windows <xref:System.Windows.Forms.ProgressBar> contrôle indique la progression d’un processus en affichant un nombre approprié de rectangles dans une barre horizontale. Lorsque le processus est terminé, la barre est remplie. Barres de progression sont couramment utilisés pour donner à l’utilisateur une idée de l’attendre d’un processus s’achève ; par exemple, quand un fichier volumineux est en cours de chargement.  
  
> [!NOTE]
>  Le <xref:System.Windows.Forms.ProgressBar> contrôle peut uniquement être orienté horizontalement sur le formulaire.  
  
## <a name="key-properties-and-methods"></a>Méthodes et propriétés de clé  
 Les propriétés de clé de la <xref:System.Windows.Forms.ProgressBar> contrôle sont <xref:System.Windows.Forms.ProgressBar.Value%2A>, <xref:System.Windows.Forms.ProgressBar.Minimum%2A>, et <xref:System.Windows.Forms.ProgressBar.Maximum%2A>. Le <xref:System.Windows.Forms.ProgressBar.Minimum%2A> et <xref:System.Windows.Forms.ProgressBar.Maximum%2A> propriétés définissent les valeurs minimales et maximales, la barre de progression peut afficher. Le <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété représente la progression de l’opération. Étant donné que la barre s’affichée dans le contrôle est constituée de blocs, la valeur affichée par le <xref:System.Windows.Forms.ProgressBar> contrôle effectue uniquement une approximation du <xref:System.Windows.Forms.ProgressBar.Value%2A> valeur actuelle de la propriété. Selon la taille de la <xref:System.Windows.Forms.ProgressBar> contrôle, le <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété détermine à quel moment afficher le bloc suivant.  
  
 L’approche la plus courante pour mettre à jour la valeur de progression actuelle consiste à écrire du code pour définir le <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété. Dans l’exemple de chargement d’un fichier volumineux, vous pouvez définir la valeur maximale pour la taille du fichier en kilo-octets. Par exemple, si le <xref:System.Windows.Forms.ProgressBar.Maximum%2A> propriété est définie sur 100, le <xref:System.Windows.Forms.ProgressBar.Minimum%2A> propriété est définie sur 10 et le <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété est définie à 50, 5 rectangles seront affichés. C’est la moitié du nombre qui peut être affiché.  
  
 Toutefois, il existe des autres moyens de modifier la valeur affichée par le <xref:System.Windows.Forms.ProgressBar> contrôle, outre la définition du <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété directement. Le <xref:System.Windows.Forms.ProgressBar.Step%2A> propriété peut être utilisée pour spécifier une valeur à incrémenter le <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété par. Puis, en appelant le <xref:System.Windows.Forms.ProgressBar.PerformStep%2A> méthode incrémente la valeur. Pour faire varier la valeur d’incrément, vous pouvez utiliser la <xref:System.Windows.Forms.ProgressBar.Increment%2A> (méthode) et spécifiez une valeur d’incrémentation le <xref:System.Windows.Forms.ProgressBar.Value%2A> propriété.  
  
 Un autre contrôle graphique qui informe l’utilisateur sur une action en cours est la <xref:System.Windows.Forms.StatusBar> contrôle.  
  
> [!IMPORTANT]
>  Le <xref:System.Windows.Forms.StatusStrip> et <xref:System.Windows.Forms.ToolStripStatusLabel> contrôles remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôle ; Toutefois, le <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôles ont été conservés pour la compatibilité descendante et une utilisation ultérieure, si vous Choisissez.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ProgressBar>
- [ProgressBar, contrôle](progressbar-control-windows-forms.md)
