---
title: Liaisons WS-MetadataExchange
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 384e5bb05ba4263f245f6901b84e2388ea19bd73
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33488622"
---
# <a name="ws-metadataexchange-bindings"></a><span data-ttu-id="0ae1c-102">Liaisons WS-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="0ae1c-102">WS-MetadataExchange Bindings</span></span>
<span data-ttu-id="0ae1c-103">Cette rubrique décrit comment les liaisons d’échange de métadonnées par défaut sont construites pour les divers transports.</span><span class="sxs-lookup"><span data-stu-id="0ae1c-103">This topic describes how the default metadata exchange bindings are constructed for various transports.</span></span>  
  
## <a name="the-default-bindings"></a><span data-ttu-id="0ae1c-104">Liaisons par défaut</span><span class="sxs-lookup"><span data-stu-id="0ae1c-104">The Default Bindings</span></span>  
  
|<span data-ttu-id="0ae1c-105">Nom de la liaison par défaut</span><span class="sxs-lookup"><span data-stu-id="0ae1c-105">Default Binding Name</span></span>|<span data-ttu-id="0ae1c-106">Construction de la liaison</span><span class="sxs-lookup"><span data-stu-id="0ae1c-106">How the binding is constructed</span></span>|  
|--------------------------|------------------------------------|  
|<span data-ttu-id="0ae1c-107">MexHttpBinding</span><span class="sxs-lookup"><span data-stu-id="0ae1c-107">MexHttpBinding</span></span>|<span data-ttu-id="0ae1c-108"><xref:System.ServiceModel.WSHttpBinding> avec la sécurité au niveau du transport désactivée.</span><span class="sxs-lookup"><span data-stu-id="0ae1c-108">A <xref:System.ServiceModel.WSHttpBinding> with transport-level security disabled.</span></span>|  
|<span data-ttu-id="0ae1c-109">MexHttpsBinding</span><span class="sxs-lookup"><span data-stu-id="0ae1c-109">MexHttpsBinding</span></span>|<span data-ttu-id="0ae1c-110"><xref:System.ServiceModel.WSHttpBinding> qui prend en charge la sécurité au niveau du transport.</span><span class="sxs-lookup"><span data-stu-id="0ae1c-110">A <xref:System.ServiceModel.WSHttpBinding> that supports transport-level security.</span></span>|  
|<span data-ttu-id="0ae1c-111">MexNamedPipeBinding</span><span class="sxs-lookup"><span data-stu-id="0ae1c-111">MexNamedPipeBinding</span></span>|<span data-ttu-id="0ae1c-112"><xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> en utilisant les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="0ae1c-112">A  <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> using the default values.</span></span>|  
|<span data-ttu-id="0ae1c-113">MexTcpBinding</span><span class="sxs-lookup"><span data-stu-id="0ae1c-113">MexTcpBinding</span></span>|<span data-ttu-id="0ae1c-114"><xref:System.ServiceModel.Channels.CustomBinding> avec <xref:System.ServiceModel.Channels.TcpTransportBindingElement> en utilisant les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="0ae1c-114">A <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.TcpTransportBindingElement> using default values.</span></span>|
