---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 8c2d4bfc08a503a8d6eb0e8abf6f1e798b90bc83
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59773699"
---
# <a name="namedpipeconnectionpoolsettings"></a><span data-ttu-id="255a0-102">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="255a0-102">NamedPipeConnectionPoolSettings</span></span>
<span data-ttu-id="255a0-103">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="255a0-103">NamedPipeConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="255a0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="255a0-104">Syntax</span></span>  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="255a0-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="255a0-105">Methods</span></span>  
 <span data-ttu-id="255a0-106">La classe NamedPipeConnectionPoolSettings ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="255a0-106">The NamedPipeConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="255a0-107">Properties</span><span class="sxs-lookup"><span data-stu-id="255a0-107">Properties</span></span>  
 <span data-ttu-id="255a0-108">La classe NamedPipeConnectionPoolSettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="255a0-108">The NamedPipeConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="255a0-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="255a0-109">GroupName</span></span>  
 <span data-ttu-id="255a0-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="255a0-110">Data type: string</span></span>  
  
 <span data-ttu-id="255a0-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="255a0-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="255a0-112">Nom de groupe du pool de connexions utilisé par l'élément de liaison.</span><span class="sxs-lookup"><span data-stu-id="255a0-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="255a0-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="255a0-113">IdleTimeout</span></span>  
 <span data-ttu-id="255a0-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="255a0-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="255a0-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="255a0-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="255a0-116">Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="255a0-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="255a0-117">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="255a0-117">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="255a0-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="255a0-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="255a0-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="255a0-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="255a0-120">Nombre maximal de connexions sortantes pour chaque point de terminaison sur le client.</span><span class="sxs-lookup"><span data-stu-id="255a0-120">The maximum number of outbound connections for each endpoint on the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="255a0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="255a0-121">Requirements</span></span>  
  
|<span data-ttu-id="255a0-122">MOF</span><span class="sxs-lookup"><span data-stu-id="255a0-122">MOF</span></span>|<span data-ttu-id="255a0-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="255a0-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="255a0-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="255a0-124">Namespace</span></span>|<span data-ttu-id="255a0-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="255a0-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="255a0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="255a0-126">See also</span></span>

- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
