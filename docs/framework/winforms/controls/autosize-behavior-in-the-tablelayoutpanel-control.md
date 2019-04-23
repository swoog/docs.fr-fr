---
title: Comportement du redimensionnement automatique dans le contrôle TableLayoutPanel
ms.date: 03/30/2017
helpviewer_keywords:
- AutoSize property [Windows Forms], tableLayoutPanel control
- controls [Windows Forms], sizing
- localizing forms
- layout [Windows Forms], AutoSize
- sizing [Windows Forms], automatic
- TableLayoutPanel control [Windows Forms], AutoSize behavior
- automatic sizing
- AutoSizeMode property
ms.assetid: 9233e0c3-2fa6-405e-8701-959479b1250e
ms.openlocfilehash: 466edeee5f45ec72ef265ef4855049c7852641b0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59164968"
---
# <a name="autosize-behavior-in-the-tablelayoutpanel-control"></a>Comportement du redimensionnement automatique dans le contrôle TableLayoutPanel
## <a name="distinct-autosize-behaviors"></a>Comportements de redimensionnement automatique distincts  
 Le <xref:System.Windows.Forms.TableLayoutPanel> contrôle prend en charge le comportement de dimensionnement automatique de plusieurs manières :  
  
-   Via le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété ;  
  
-   Via le <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> propriété sur le <xref:System.Windows.Forms.TableLayoutPanel> les styles de ligne et de colonne du contrôle.  
  
### <a name="the-autosize-property-with-row-and-column-styles"></a>La propriété AutoSize avec les Styles de colonne et de ligne  
 Le tableau suivant décrit l’interaction entre le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété et le <xref:System.Windows.Forms.TableLayoutPanel> les styles de ligne et de colonne du contrôle.  
  
|Paramètre de redimensionnement automatique|Interaction de style|  
|----------------------|-----------------------|  
|`false`|Le <xref:System.Windows.Forms.TableLayoutPanel> contrôle opère de gauche à droite et alloue de l’espace pour la colonne ou ligne ou dans l’ordre suivant.<br /><br /> 1.  Si le <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> propriété est définie sur <xref:System.Windows.Forms.SizeType.Absolute>, le nombre de pixels spécifié par <xref:System.Windows.Forms.ColumnStyle.Width%2A> ou <xref:System.Windows.Forms.RowStyle.Height%2A> est allouée.<br />2.  Si le <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> propriété est définie sur <xref:System.Windows.Forms.SizeType.AutoSize>, le nombre de pixels retourné par le contrôle enfant <xref:System.Windows.Forms.Control.GetPreferredSize%2A> méthode est allouée.<br />3.  Après avoir d’espace pour tous les <xref:System.Windows.Forms.SizeType.Absolute> et <xref:System.Windows.Forms.SizeType.AutoSize> colonnes ou lignes est allouée, des colonnes ou des lignes avec <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> la valeur <xref:System.Windows.Forms.SizeType.Percent> sont utilisés pour répartir proportionnellement l’espace libre restant|  
|`true`|Similaire à l’interaction précédente, avec l’exception qui <xref:System.Windows.Forms.SizeType.Percent> lignes ou colonnes acquièrent un aspect de dimensionnement automatique.<br /><br /> Le <xref:System.Windows.Forms.TableLayoutPanel> contrôle s’agrandit la colonne ou ligne pour créer l’espace libre adéquat, afin qu’aucune colonne ou ligne avec <xref:System.Windows.Forms.SizeType.Percent> style fait coïncider son contenu. Le <xref:System.Windows.Forms.TableLayoutPanel> contrôle alloue le nouvel espace proportionnellement en fonction de la <xref:System.Windows.Forms.ColumnStyle.Width%2A> ou <xref:System.Windows.Forms.RowStyle.Height%2A> propriété.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.TableLayoutPanel>
- [Vue d’ensemble du contrôle TableLayoutPanel](tablelayoutpanel-control-overview.md)
