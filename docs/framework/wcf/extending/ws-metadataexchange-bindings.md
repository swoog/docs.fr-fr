---
title: Liaisons WS-MetadataExchange
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 03e6e6d5ee7e69b397acd0f51b8037f02c1804ec
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61795471"
---
# <a name="ws-metadataexchange-bindings"></a><span data-ttu-id="6ce27-102">Liaisons WS-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="6ce27-102">WS-MetadataExchange Bindings</span></span>
<span data-ttu-id="6ce27-103">Cette rubrique décrit comment les liaisons d’échange de métadonnées par défaut sont construites pour les divers transports.</span><span class="sxs-lookup"><span data-stu-id="6ce27-103">This topic describes how the default metadata exchange bindings are constructed for various transports.</span></span>  
  
## <a name="the-default-bindings"></a><span data-ttu-id="6ce27-104">Liaisons par défaut</span><span class="sxs-lookup"><span data-stu-id="6ce27-104">The Default Bindings</span></span>  
  
|<span data-ttu-id="6ce27-105">Nom de la liaison par défaut</span><span class="sxs-lookup"><span data-stu-id="6ce27-105">Default Binding Name</span></span>|<span data-ttu-id="6ce27-106">Construction de la liaison</span><span class="sxs-lookup"><span data-stu-id="6ce27-106">How the binding is constructed</span></span>|  
|--------------------------|------------------------------------|  
|<span data-ttu-id="6ce27-107">mexHttpBinding</span><span class="sxs-lookup"><span data-stu-id="6ce27-107">mexHttpBinding</span></span>|<span data-ttu-id="6ce27-108"><xref:System.ServiceModel.WSHttpBinding> avec la sécurité au niveau du transport désactivée.</span><span class="sxs-lookup"><span data-stu-id="6ce27-108">A <xref:System.ServiceModel.WSHttpBinding> with transport-level security disabled.</span></span>|  
|<span data-ttu-id="6ce27-109">mexHttpsBinding</span><span class="sxs-lookup"><span data-stu-id="6ce27-109">mexHttpsBinding</span></span>|<span data-ttu-id="6ce27-110"><xref:System.ServiceModel.WSHttpBinding> qui prend en charge la sécurité au niveau du transport.</span><span class="sxs-lookup"><span data-stu-id="6ce27-110">A <xref:System.ServiceModel.WSHttpBinding> that supports transport-level security.</span></span>|  
|<span data-ttu-id="6ce27-111">mexNamedPipeBinding</span><span class="sxs-lookup"><span data-stu-id="6ce27-111">mexNamedPipeBinding</span></span>|<span data-ttu-id="6ce27-112"><xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> en utilisant les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ce27-112">A  <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> using the default values.</span></span>|  
|<span data-ttu-id="6ce27-113">mexTcpBinding</span><span class="sxs-lookup"><span data-stu-id="6ce27-113">mexTcpBinding</span></span>|<span data-ttu-id="6ce27-114"><xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.TcpTransportBindingElement> en utilisant les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ce27-114">A <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.TcpTransportBindingElement> using default values.</span></span>|
