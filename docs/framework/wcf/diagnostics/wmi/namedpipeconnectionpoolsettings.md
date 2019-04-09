---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 8c2d4bfc08a503a8d6eb0e8abf6f1e798b90bc83
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59095332"
---
# <a name="namedpipeconnectionpoolsettings"></a><span data-ttu-id="f4343-102">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="f4343-102">NamedPipeConnectionPoolSettings</span></span>
<span data-ttu-id="f4343-103">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="f4343-103">NamedPipeConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4343-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4343-104">Syntax</span></span>  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f4343-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f4343-105">Methods</span></span>  
 <span data-ttu-id="f4343-106">La classe NamedPipeConnectionPoolSettings ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="f4343-106">The NamedPipeConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f4343-107">Properties</span><span class="sxs-lookup"><span data-stu-id="f4343-107">Properties</span></span>  
 <span data-ttu-id="f4343-108">La classe NamedPipeConnectionPoolSettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4343-108">The NamedPipeConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="f4343-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="f4343-109">GroupName</span></span>  
 <span data-ttu-id="f4343-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f4343-110">Data type: string</span></span>  
  
 <span data-ttu-id="f4343-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4343-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f4343-112">Nom de groupe du pool de connexions utilisé par l'élément de liaison.</span><span class="sxs-lookup"><span data-stu-id="f4343-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="f4343-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="f4343-113">IdleTimeout</span></span>  
 <span data-ttu-id="f4343-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="f4343-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="f4343-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4343-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f4343-116">Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="f4343-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="f4343-117">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4343-117">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="f4343-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="f4343-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="f4343-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4343-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f4343-120">Nombre maximal de connexions sortantes pour chaque point de terminaison sur le client.</span><span class="sxs-lookup"><span data-stu-id="f4343-120">The maximum number of outbound connections for each endpoint on the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4343-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4343-121">Requirements</span></span>  
  
|<span data-ttu-id="f4343-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f4343-122">MOF</span></span>|<span data-ttu-id="f4343-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="f4343-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f4343-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4343-124">Namespace</span></span>|<span data-ttu-id="f4343-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f4343-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f4343-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4343-126">See also</span></span>

- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
