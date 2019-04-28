---
title: Entrée d'utilisateur dans une application Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, user input
ms.assetid: 9d61fa96-70f7-4754-885a-49a4a6316bdb
ms.openlocfilehash: 0eb39f0ecd8fcd12918b38bd77fed2ff32cac1d8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61800137"
---
# <a name="user-input-in-a-windows-forms-application"></a>Entrée d'utilisateur dans une application Windows Forms
Dans les Windows Forms, l’entrée d’utilisateur est envoyée aux applications sous la forme de messages de Windows. Une série de méthodes substituables traiter ces messages au niveau de l’application, le formulaire et contrôler le niveau. Lorsque ces méthodes reçoivent des messages de clavier et de la souris, ils déclenchent des événements qui peuvent être gérés pour obtenir des informations sur la souris ou clavier d’entrée. Dans de nombreux cas, les applications Windows Forms seront en mesure de traiter toutes les entrées utilisateur simplement en gérant ces événements. Dans d’autres cas, une application devrez peut-être substituer l’une des méthodes qui traitent les messages afin d’intercepter un message particulier avant sa réception par l’application, un formulaire ou un contrôle.  
  
## <a name="mouse-and-keyboard-events"></a>Événements de souris et clavier  
 Tous les contrôles Windows Forms héritent d’un ensemble d’événements liés à la souris et clavier. Par exemple, un contrôle peut gérer le <xref:System.Windows.Forms.Control.KeyPress> événement pour déterminer le code de caractère d’une clé qui a été enfoncée, ou un contrôle peut gérer le <xref:System.Windows.Forms.Control.MouseClick> événement pour déterminer l’emplacement de la souris, cliquez sur. Pour plus d’informations sur les événements de souris et clavier, consultez [à l’aide des événements de clavier](using-keyboard-events.md) et [des événements de souris dans les Windows Forms](mouse-events-in-windows-forms.md).  
  
## <a name="methods-that-process-user-input-messages"></a>Méthodes qui traitent les Messages d’entrée utilisateur  
 Formulaires et contrôles ont accès à la <xref:System.Windows.Forms.IMessageFilter> interface et un ensemble de méthodes substituables qui traitent les messages Windows à différents moments dans la file d’attente. Ces méthodes ont toutes un <xref:System.Windows.Forms.Message> paramètre, qui encapsule les détails de bas niveau des messages de Windows. Vous pouvez implémenter ou substituer ces méthodes pour examiner le message, puis consommer le message ou passez-le au consommateur suivant dans la file d’attente. Le tableau suivant présente les méthodes qui traitent tous les messages Windows dans Windows Forms.  
  
|Méthode|Notes|  
|------------|-----------|  
|<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A>|Cette méthode intercepte en file d’attente des messages Windows (également appelé validées) au niveau de l’application.|  
|<xref:System.Windows.Forms.Control.PreProcessMessage%2A>|Cette méthode intercepte les messages Windows au niveau du formulaire et de contrôle avant qu’ils ont été traités.|  
|<xref:System.Windows.Forms.Control.WndProc%2A>|Cette méthode traite les messages Windows au niveau du formulaire et de contrôle.|  
|<xref:System.Windows.Forms.Control.DefWndProc%2A>|Cette méthode effectue le traitement par défaut des messages Windows au niveau du formulaire et de contrôle. Cela fournit les fonctionnalités minimales d’une fenêtre.|  
|<xref:System.Windows.Forms.Control.OnNotifyMessage%2A>|Cette méthode intercepte les messages au niveau du formulaire et de contrôle, une fois qu’ils ont été traités. Le <xref:System.Windows.Forms.ControlStyles.EnableNotifyMessage> bit de style doit être définie pour cette méthode à appeler.|  
  
 Les messages de clavier et souris sont également traitées par un jeu supplémentaire de méthodes substituables qui sont spécifiques à ces types de messages. Pour plus d’informations, consultez [fonctionnement des entrées au clavier](how-keyboard-input-works.md) et [souris entrée fonctionnement dans les Windows Forms](how-mouse-input-works-in-windows-forms.md).  
  
## <a name="see-also"></a>Voir aussi

- [Entrées d’utilisateur dans les Windows Forms](user-input-in-windows-forms.md)
- [Entrée au clavier dans une application Windows Forms](keyboard-input-in-a-windows-forms-application.md)
- [Entrée de la souris dans une application Windows Forms](mouse-input-in-a-windows-forms-application.md)
