---
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 334bab97a04ed464dce6944692b04a9ed1295296
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54613820"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="90b3f-102">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="90b3f-102">MustUnderstandBehavior</span></span>
<span data-ttu-id="90b3f-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="90b3f-103">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90b3f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90b3f-104">Syntax</span></span>  
  
```csharp
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="90b3f-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="90b3f-105">Methods</span></span>  
 <span data-ttu-id="90b3f-106">La classe MustUnderstandBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="90b3f-106">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="90b3f-107">Properties</span><span class="sxs-lookup"><span data-stu-id="90b3f-107">Properties</span></span>  
 <span data-ttu-id="90b3f-108">La classe MustUnderstandBehavior a la propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="90b3f-108">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="90b3f-109">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="90b3f-109">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="90b3f-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="90b3f-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="90b3f-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="90b3f-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="90b3f-112">Lorsque cette propriété a la valeur `true`, tous les en-têtes SOAP avec l'attribut `MustUnderstand` qui ne sont pas gérés font en sorte que le comportement lève une exception.</span><span class="sxs-lookup"><span data-stu-id="90b3f-112">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90b3f-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="90b3f-113">Requirements</span></span>  
  
|<span data-ttu-id="90b3f-114">MOF</span><span class="sxs-lookup"><span data-stu-id="90b3f-114">MOF</span></span>|<span data-ttu-id="90b3f-115">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="90b3f-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="90b3f-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90b3f-116">Namespace</span></span>|<span data-ttu-id="90b3f-117">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="90b3f-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="90b3f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90b3f-118">See also</span></span>
- <xref:System.ServiceModel.Description.MustUnderstandBehavior>
