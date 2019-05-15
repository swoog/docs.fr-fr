---
title: Sérialisation JSON
ms.date: 03/30/2017
ms.assetid: 3c2c4747-7510-4bdf-b4fe-64f98428ef4a
ms.openlocfilehash: c44dd71c3903e5c4d3d37b89881896c65c664262
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591868"
---
# <a name="json-serialization"></a><span data-ttu-id="f82ab-102">Sérialisation JSON</span><span class="sxs-lookup"><span data-stu-id="f82ab-102">JSON Serialization</span></span>
<span data-ttu-id="f82ab-103">Cet exemple montre comment utiliser le <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> pour sérialiser et désérialiser des données au format JSON (JavaScript Objet Notation).</span><span class="sxs-lookup"><span data-stu-id="f82ab-103">This sample demonstrates how to use the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> to serialize and deserialize data in the JavaScript Object Notation (JSON) format.</span></span> <span data-ttu-id="f82ab-104">Ce moteur de sérialisation convertit des données JSON en instances de types .NET Framework et la remettre en données JSON.</span><span class="sxs-lookup"><span data-stu-id="f82ab-104">This serialization engine converts JSON data into instances of .NET Framework types and back into JSON data.</span></span> <span data-ttu-id="f82ab-105"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> prend en charge les mêmes types que <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="f82ab-105"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> supports the same types as <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="f82ab-106">Le format de données JSON est particulièrement utile lors de l'écriture d'applications Web de style JavaScript et XML (AJAX) asynchrones.</span><span class="sxs-lookup"><span data-stu-id="f82ab-106">The JSON data format is especially useful when writing Asynchronous JavaScript and XML (AJAX)-style Web applications.</span></span> <span data-ttu-id="f82ab-107">Prise en charge AJAX dans Windows Communication Foundation (WCF) est optimisé pour une utilisation avec ASP.NET AJAX via le contrôle ScriptManager.</span><span class="sxs-lookup"><span data-stu-id="f82ab-107">AJAX support in Windows Communication Foundation (WCF) is optimized for use with ASP.NET AJAX through the ScriptManager control.</span></span> <span data-ttu-id="f82ab-108">Pour obtenir des exemples montrant comment utiliser Windows Communication Foundation (WCF) avec ASP.NET AJAX, consultez le [exemples AJAX](ajax.md).</span><span class="sxs-lookup"><span data-stu-id="f82ab-108">For examples of how to use Windows Communication Foundation (WCF) with ASP.NET AJAX, see the [AJAX Samples](ajax.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f82ab-109">La procédure d'installation ainsi que les instructions de génération correspondant à cet exemple figurent en fin de rubrique.</span><span class="sxs-lookup"><span data-stu-id="f82ab-109">The set-up procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="f82ab-110">L'exemple utilise un contrat de données `Person` pour illustrer la sérialisation et la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="f82ab-110">The sample uses a `Person` data contract to demonstrate serialization and deserialization.</span></span>  

```csharp
[DataContract]
class Person
{
    [DataMember]
    internal string name;

    [DataMember]
    internal int age;
}
```

 <span data-ttu-id="f82ab-111">Pour sérialiser une instance du type `Person` en JSON, créez d'abord le <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> et utilisez la méthode `WriteObject` pour écrire des données JSON dans un flux.</span><span class="sxs-lookup"><span data-stu-id="f82ab-111">To serialize an instance of the `Person` type to JSON, create the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> first and use the `WriteObject` method to write JSON data to a stream.</span></span>  

```csharp
Person p = new Person();
//Set up Person object...
MemoryStream stream1 = new MemoryStream();
DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(Person));
ser.WriteObject(stream1, p);
```

 <span data-ttu-id="f82ab-112">Le flux de mémoire contient des données JSON valides.</span><span class="sxs-lookup"><span data-stu-id="f82ab-112">The memory stream contains valid JSON data.</span></span>
  
```json  
{"age":42,"name":"John"}  
```  
  
 <span data-ttu-id="f82ab-113">L'exemple illustre la désérialisation de données JSON dans un objet.</span><span class="sxs-lookup"><span data-stu-id="f82ab-113">The sample demonstrates deserializing from JSON data into an object.</span></span> <span data-ttu-id="f82ab-114">Ensuite, vous rembobinez le flux et appelez `ReadObject`.</span><span class="sxs-lookup"><span data-stu-id="f82ab-114">You then rewind the stream and call `ReadObject`.</span></span>  

```csharp
Person p2 = (Person)ser.ReadObject(stream1);
```

 <span data-ttu-id="f82ab-115">L'examen de l'objet `p2` révèle que les données JSON ont été correctement désérialisées.</span><span class="sxs-lookup"><span data-stu-id="f82ab-115">Examining the `p2` object reveals that the JSON data has been deserialized correctly.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="f82ab-116">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f82ab-116">The samples may already be installed on your machine.</span></span> <span data-ttu-id="f82ab-117">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="f82ab-117">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="f82ab-118">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="f82ab-118">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="f82ab-119">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="f82ab-119">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\JsonSerialization`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="f82ab-120">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="f82ab-120">To set up, build and run the sample</span></span>  
  
1. <span data-ttu-id="f82ab-121">Générez la solution JsonSerialization.sln comme décrit dans [génération des exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f82ab-121">Build the solution JsonSerialization.sln as described in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
2. <span data-ttu-id="f82ab-122">Exécutez l'application console qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="f82ab-122">Run the resulting console application.</span></span>  
