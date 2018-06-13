---
title: Operation, classe
ms.date: 03/30/2017
ms.assetid: b19d1496-ef06-4d0c-b2ae-e728ec00cca0
ms.openlocfilehash: d9256915afe9fdb8e4c91d186131fe41a7094c56
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33487566"
---
# <a name="operation-class"></a><span data-ttu-id="f5178-102">Operation, classe</span><span class="sxs-lookup"><span data-stu-id="f5178-102">Operation class</span></span>
<span data-ttu-id="f5178-103">Opération</span><span class="sxs-lookup"><span data-stu-id="f5178-103">Operation</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5178-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5178-104">Syntax</span></span>  
  
```  
class Operation  
{  
  string Action;  
  boolean AsyncPattern;  
  Behavior Behaviors[];  
  boolean IsCallback;  
  boolean IsInitiating;  
  boolean IsOneWay;  
  boolean IsTerminating;  
  string MethodSignature;  
  string Name;  
  string ParameterTypes[];  
  string ReplyAction;  
  string ReturnType;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f5178-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f5178-105">Methods</span></span>  
 <span data-ttu-id="f5178-106">La classe Operation ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="f5178-106">The Operation class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f5178-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5178-107">Properties</span></span>  
 <span data-ttu-id="f5178-108">La classe Operation a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5178-108">The Operation class has the following properties:</span></span>  
  
### <a name="action"></a><span data-ttu-id="f5178-109">Action</span><span class="sxs-lookup"><span data-stu-id="f5178-109">Action</span></span>  
 <span data-ttu-id="f5178-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f5178-110">Data type: string</span></span>  
  
 <span data-ttu-id="f5178-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-112">L'action WS-Addressing du message de demande.</span><span class="sxs-lookup"><span data-stu-id="f5178-112">The WS-Addressing action of the request message.</span></span>  
  
### <a name="asyncpattern"></a><span data-ttu-id="f5178-113">AsyncPattern</span><span class="sxs-lookup"><span data-stu-id="f5178-113">AsyncPattern</span></span>  
 <span data-ttu-id="f5178-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="f5178-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="f5178-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-116">Indique qu’une opération est implémentée à l’aide de façon asynchrone un `Begin`[Ouvrir/fermer les crochets pointus] et `End`paire de méthodes [ouverture/fermeture crochets] dans un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="f5178-116">Indicates that an operation is implemented asynchronously using a `Begin`[open/close angle brackets] and `End`[open/close angle brackets] method pair in a service contract.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="f5178-117">comportements</span><span class="sxs-lookup"><span data-stu-id="f5178-117">Behaviors</span></span>  
 <span data-ttu-id="f5178-118">Type de données : tableau de comportements</span><span class="sxs-lookup"><span data-stu-id="f5178-118">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="f5178-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-120">Comportements associés à cette opération.</span><span class="sxs-lookup"><span data-stu-id="f5178-120">The behaviors associated with this operation.</span></span>  
  
### <a name="iscallback"></a><span data-ttu-id="f5178-121">IsCallback</span><span class="sxs-lookup"><span data-stu-id="f5178-121">IsCallback</span></span>  
 <span data-ttu-id="f5178-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="f5178-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="f5178-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-124">True lorsque l'opération est une opération de rappel.</span><span class="sxs-lookup"><span data-stu-id="f5178-124">True when the operation is a callback operation.</span></span>  
  
### <a name="isinitiating"></a><span data-ttu-id="f5178-125">IsInitiating</span><span class="sxs-lookup"><span data-stu-id="f5178-125">IsInitiating</span></span>  
 <span data-ttu-id="f5178-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="f5178-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="f5178-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-128">Indique si la méthode implémente une opération qui peut initialiser une session sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f5178-128">Indicates whether the method implements an operation that can initiate a session on the server.</span></span>  
  
### <a name="isoneway"></a><span data-ttu-id="f5178-129">IsOneWay</span><span class="sxs-lookup"><span data-stu-id="f5178-129">IsOneWay</span></span>  
 <span data-ttu-id="f5178-130">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="f5178-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="f5178-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-132">Indique si une opération retourne un message de réponse.</span><span class="sxs-lookup"><span data-stu-id="f5178-132">Indicates whether an operation returns a reply message.</span></span>  
  
### <a name="isterminating"></a><span data-ttu-id="f5178-133">IsTerminating</span><span class="sxs-lookup"><span data-stu-id="f5178-133">IsTerminating</span></span>  
 <span data-ttu-id="f5178-134">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="f5178-134">Data type: boolean</span></span>  
  
 <span data-ttu-id="f5178-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-136">Indique si une opération retourne un message de réponse.</span><span class="sxs-lookup"><span data-stu-id="f5178-136">Indicates whether an operation returns a reply message.</span></span>  
  
### <a name="methodsignature"></a><span data-ttu-id="f5178-137">MethodSignature</span><span class="sxs-lookup"><span data-stu-id="f5178-137">MethodSignature</span></span>  
 <span data-ttu-id="f5178-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f5178-138">Data type: string</span></span>  
  
 <span data-ttu-id="f5178-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-140">Signature de méthode de l'opération.</span><span class="sxs-lookup"><span data-stu-id="f5178-140">The method signature of the operation.</span></span>  
  
### <a name="name"></a><span data-ttu-id="f5178-141">Name</span><span class="sxs-lookup"><span data-stu-id="f5178-141">Name</span></span>  
 <span data-ttu-id="f5178-142">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f5178-142">Data type: string</span></span>  
  
 <span data-ttu-id="f5178-143">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-144">Nom de l'opération.</span><span class="sxs-lookup"><span data-stu-id="f5178-144">The name of the operation.</span></span>  
  
### <a name="parametertypes"></a><span data-ttu-id="f5178-145">ParameterTypes</span><span class="sxs-lookup"><span data-stu-id="f5178-145">ParameterTypes</span></span>  
 <span data-ttu-id="f5178-146">Type de données : tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="f5178-146">Data type: string array</span></span>  
  
 <span data-ttu-id="f5178-147">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-148">Types des paramètres de l'opération.</span><span class="sxs-lookup"><span data-stu-id="f5178-148">The types of the parameters of the operation.</span></span>  
  
### <a name="replyaction"></a><span data-ttu-id="f5178-149">ReplyAction</span><span class="sxs-lookup"><span data-stu-id="f5178-149">ReplyAction</span></span>  
 <span data-ttu-id="f5178-150">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f5178-150">Data type: string</span></span>  
  
 <span data-ttu-id="f5178-151">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-152">Valeur de l'action SOAP pour le message de réponse de l'opération.</span><span class="sxs-lookup"><span data-stu-id="f5178-152">The value of the SOAP action for the reply message of the operation.</span></span>  
  
### <a name="returntype"></a><span data-ttu-id="f5178-153">ReturnType</span><span class="sxs-lookup"><span data-stu-id="f5178-153">ReturnType</span></span>  
 <span data-ttu-id="f5178-154">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f5178-154">Data type: string</span></span>  
  
 <span data-ttu-id="f5178-155">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5178-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5178-156">Type de retour de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f5178-156">The return type of the operation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5178-157">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f5178-157">Requirements</span></span>  
  
|<span data-ttu-id="f5178-158">MOF</span><span class="sxs-lookup"><span data-stu-id="f5178-158">MOF</span></span>|<span data-ttu-id="f5178-159">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="f5178-159">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f5178-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f5178-160">Namespace</span></span>|<span data-ttu-id="f5178-161">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f5178-161">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f5178-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5178-162">See Also</span></span>  
 <xref:System.ServiceModel.Description.OperationDescription>
