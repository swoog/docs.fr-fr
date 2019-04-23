---
title: TcpConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 19acfba3-c057-4dbc-bac7-8674d7844d83
ms.openlocfilehash: 6fa68eed241edaea40b66c31240a4201e05779f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59975341"
---
# <a name="tcpconnectionpoolsettings"></a><span data-ttu-id="3ae90-102">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="3ae90-102">TcpConnectionPoolSettings</span></span>
<span data-ttu-id="3ae90-103">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="3ae90-103">TcpConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ae90-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ae90-104">Syntax</span></span>  
  
```csharp
class TcpConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3ae90-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3ae90-105">Methods</span></span>  
 <span data-ttu-id="3ae90-106">La classe TcpConnectionPoolSettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="3ae90-106">The TcpConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3ae90-107">Properties</span><span class="sxs-lookup"><span data-stu-id="3ae90-107">Properties</span></span>  
 <span data-ttu-id="3ae90-108">La classe TcpConnectionPoolSettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ae90-108">The TcpConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="3ae90-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="3ae90-109">GroupName</span></span>  
 <span data-ttu-id="3ae90-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="3ae90-110">Data type: string</span></span>  
  
 <span data-ttu-id="3ae90-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ae90-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3ae90-112">Nom de groupe du pool de connexions utilisé par l'élément de liaison.</span><span class="sxs-lookup"><span data-stu-id="3ae90-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="3ae90-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="3ae90-113">IdleTimeout</span></span>  
 <span data-ttu-id="3ae90-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="3ae90-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="3ae90-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ae90-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3ae90-116">Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="3ae90-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="3ae90-117">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="3ae90-117">LeaseTimeout</span></span>  
 <span data-ttu-id="3ae90-118">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="3ae90-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="3ae90-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ae90-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3ae90-120">Période maximale d'exécution de l'opération de bail avant expiration du délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="3ae90-120">The maximum time for the lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="3ae90-121">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ae90-121">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="3ae90-122">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="3ae90-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="3ae90-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ae90-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3ae90-124">Nombre maximal de connexions sortantes pour chaque point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3ae90-124">The maximum outbound connections for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ae90-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ae90-125">Requirements</span></span>  
  
|<span data-ttu-id="3ae90-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3ae90-126">MOF</span></span>|<span data-ttu-id="3ae90-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="3ae90-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3ae90-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ae90-128">Namespace</span></span>|<span data-ttu-id="3ae90-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3ae90-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3ae90-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ae90-130">See also</span></span>

- <xref:System.ServiceModel.Channels.TcpConnectionPoolSettings>
