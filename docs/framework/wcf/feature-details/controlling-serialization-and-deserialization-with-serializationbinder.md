---
title: Contrôle de la sérialisation et de la désérialisation avec SerializationBinder
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ba8dcecf-acc7-467c-939d-021bbac797d4
caps.latest.revision: 5
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: e41308de617fc02471ac2cb9769ec6e90e665e0b
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="controlling-serialization-and-deserialization-with-serializationbinder"></a><span data-ttu-id="e0be6-102">Contrôle de la sérialisation et de la désérialisation avec SerializationBinder</span><span class="sxs-lookup"><span data-stu-id="e0be6-102">Controlling Serialization and Deserialization with SerializationBinder</span></span>
<span data-ttu-id="e0be6-103">Au cours de la sérialisation, un formateur transmet les informations requises pour créer une instance d'un objet de type et de version corrects.</span><span class="sxs-lookup"><span data-stu-id="e0be6-103">During serialization, a formatter transmits the information required to create an instance of an object of the correct type and version.</span></span> <span data-ttu-id="e0be6-104">Ces informations comprennent généralement le nom de type et le nom d'assembly complets de l'objet.</span><span class="sxs-lookup"><span data-stu-id="e0be6-104">This information generally includes the full type name and assembly name of the object.</span></span> <span data-ttu-id="e0be6-105">Par défaut, la désérialisation utilise ces informations pour créer une instance d'un objet identique.</span><span class="sxs-lookup"><span data-stu-id="e0be6-105">By default, deserialization uses this information to create an instance of an identical object.</span></span> <span data-ttu-id="e0be6-106">Certains utilisateurs auront peut-être besoin de vérifier quelle classe sérialiser et désérialiser, pour les raisons suivantes : la classe d’origine n’existe pas sur l’ordinateur qui effectue la désérialisation, la classe d’origine a été déplacée entre des assemblys ou une version différente de la classe est requise sur le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="e0be6-106">Some users may need to control which class to serialize and deserialize, either because the original class may not exist on the machine performing deserialization, the original class has moved between assemblies, or a different version of the class is required on the server and client.</span></span> <span data-ttu-id="e0be6-107">Pour plus d’informations, consultez [d’utilisation de Binder de sérialisation](../../../../docs/framework/wcf/samples/usage-of-serialization-binder.md).</span><span class="sxs-lookup"><span data-stu-id="e0be6-107">For more information, see [Usage of Serialization Binder](../../../../docs/framework/wcf/samples/usage-of-serialization-binder.md).</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="e0be6-108">Ces fonctionnalités sont disponibles uniquement lors de l'utilisation de l'objet <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> ou <xref:System.Runtime.Serialization.NetDataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="e0be6-108">This functionality is only available when using the <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> or the <xref:System.Runtime.Serialization.NetDataContractSerializer>.</span></span>  
  
## <a name="using-serializationbinder"></a><span data-ttu-id="e0be6-109">Utilisation de SerializationBinder</span><span class="sxs-lookup"><span data-stu-id="e0be6-109">Using SerializationBinder</span></span>  
 <span data-ttu-id="e0be6-110"><xref:System.Runtime.Serialization.SerializationBinder> est une classe abstraite utilisée pour contrôler les types réels utilisés lors de la sérialisation et de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="e0be6-110"><xref:System.Runtime.Serialization.SerializationBinder> is an abstract class used to control the actual types used during serialization and deserialization.</span></span> <span data-ttu-id="e0be6-111">Pour contrôler les types utilisés pendant la sérialisation et la désérialisation, dérivez une classe à partir de <xref:System.Runtime.Serialization.SerializationBinder> et substituez les méthodes <xref:System.Runtime.Serialization.SerializationBinder.BindToName(System.Type,System.String@,System.String@)> et <xref:System.Runtime.Serialization.SerializationBinder.BindToType(System.String,System.String)>.</span><span class="sxs-lookup"><span data-stu-id="e0be6-111">To control the types used during serialization and deserialization, derive a class from <xref:System.Runtime.Serialization.SerializationBinder> and override the <xref:System.Runtime.Serialization.SerializationBinder.BindToName(System.Type,System.String@,System.String@)> and <xref:System.Runtime.Serialization.SerializationBinder.BindToType(System.String,System.String)> methods.</span></span> <span data-ttu-id="e0be6-112">La méthode <xref:System.Runtime.Serialization.SerializationBinder.BindToName(System.Type,System.String@,System.String@)> prend un <xref:System.Type> et retourne un assembly et un type de nom.</span><span class="sxs-lookup"><span data-stu-id="e0be6-112">The <xref:System.Runtime.Serialization.SerializationBinder.BindToName(System.Type,System.String@,System.String@)> method takes a <xref:System.Type> and returns an assembly and type name.</span></span> <span data-ttu-id="e0be6-113">La méthode <xref:System.Runtime.Serialization.SerializationBinder.BindToType(System.String,System.String)> prend un assembly et un type de nom et retourne un <xref:System.Type>.</span><span class="sxs-lookup"><span data-stu-id="e0be6-113">The <xref:System.Runtime.Serialization.SerializationBinder.BindToType(System.String,System.String)> method takes an assembly and type name and returns a <xref:System.Type>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0be6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0be6-114">See Also</span></span>  
 [<span data-ttu-id="e0be6-115">Sérialisation et désérialisation</span><span class="sxs-lookup"><span data-stu-id="e0be6-115">Serialization and Deserialization</span></span>](../../../../docs/framework/wcf/feature-details/serialization-and-deserialization.md)  
 [<span data-ttu-id="e0be6-116">Utilisation du binder de sérialisation</span><span class="sxs-lookup"><span data-stu-id="e0be6-116">Usage of Serialization Binder</span></span>](../../../../docs/framework/wcf/samples/usage-of-serialization-binder.md)
