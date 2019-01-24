---
title: 'Procédure : Utiliser mailto : pour envoyer un courrier électronique à partir d’une Page'
ms.date: 03/30/2017
helpviewer_keywords:
- 'sending mail from pages with mailto:'
- mailto:, sending mail from pages
- mail [WPF], sending from pages
ms.assetid: b64b9518-df17-4232-94f2-455a4f77ee48
ms.openlocfilehash: 34571fd7df6c75cb5b71db0ccc5565ebaae5badb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710766"
---
# <a name="how-to-use-mailto-to-send-mail-from-a-page"></a><span data-ttu-id="5c08a-102">Procédure : Utiliser mailto : pour envoyer un courrier électronique à partir d’une Page</span><span class="sxs-lookup"><span data-stu-id="5c08a-102">How to: Use mailto: to Send Mail From a Page</span></span>
<span data-ttu-id="5c08a-103">Cet exemple montre comment utiliser <xref:System.Windows.Documents.Hyperlink> conjointement avec un **mailto :**[!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)].</span><span class="sxs-lookup"><span data-stu-id="5c08a-103">This example shows how to use <xref:System.Windows.Documents.Hyperlink> in conjunction with a **mailto:**[!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c08a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c08a-104">Example</span></span>  
 <span data-ttu-id="5c08a-105">Le code suivant montre comment utiliser un **mailto :** [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)] pour ouvrir une nouvelle fenêtre de messagerie qui contient une adresse e-mail et adresse de messagerie et un objet, une adresse de messagerie, de l’objet et corps.</span><span class="sxs-lookup"><span data-stu-id="5c08a-105">The following code shows how to use a **mailto:**[!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)] to open a new mail window that contains an email address, and email address and a subject, and an email address, subject, and body.</span></span>  
  
 [!code-xaml[HOWTONavigationMailToSnippet#MailToMARKUP](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationMailToSnippet/CS/HomePage.xaml#mailtomarkup)]  
  
## <a name="see-also"></a><span data-ttu-id="5c08a-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c08a-106">See also</span></span>
- [<span data-ttu-id="5c08a-107">URI à en-tête pack dans WPF</span><span class="sxs-lookup"><span data-stu-id="5c08a-107">Pack URIs in WPF</span></span>](../../../../docs/framework/wpf/app-development/pack-uris-in-wpf.md)
