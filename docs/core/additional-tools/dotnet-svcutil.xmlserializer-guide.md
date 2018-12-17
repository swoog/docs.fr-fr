# <a name="using-dotnet-svcutilxmlserializer-on-net-core"></a><span data-ttu-id="a7f57-101">Utiliser dotnet-svcutil.xmlserializer sur .NET Core</span><span class="sxs-lookup"><span data-stu-id="a7f57-101">Using dotnet-svcutil.xmlserializer on .NET Core</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a7f57-102">Prérequis</span><span class="sxs-lookup"><span data-stu-id="a7f57-102">Prerequisites</span></span>

<span data-ttu-id="a7f57-103">Les éléments suivants sont nécessaires pour faire fonctionner dotnet-svcutil.xmlserializer.</span><span class="sxs-lookup"><span data-stu-id="a7f57-103">The following is required for dotnet-svcutil.xmlserializer to work.</span></span> 

* [<span data-ttu-id="a7f57-104">SDK .NET Core 2.1 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a7f57-104">.NET Core 2.1 SDK or later</span></span>](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300)
* [<span data-ttu-id="a7f57-105">Runtime .NET Core 2.1 (ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="a7f57-105">.NET Core Runtime 2.1 or later</span></span>](https://www.microsoft.com/net/download/dotnet-core/runtime-2.1.0)

<span data-ttu-id="a7f57-106">Vous pouvez utiliser la commande `dotnet --info` pour savoir quelles versions du runtime et du kit SDK .NET Core sont déjà installées.</span><span class="sxs-lookup"><span data-stu-id="a7f57-106">You can use the command `dotnet --info` to check which versions of .NET Core SDK and runtime you already have installed.</span></span>

<span data-ttu-id="a7f57-107">Pour utiliser dotnet-svcutil.xmlserializer dans une application console .NET Core :</span><span class="sxs-lookup"><span data-stu-id="a7f57-107">To use dotnet-svcutil.xmlserializer in a .NET Core console application:</span></span>

1. <span data-ttu-id="a7f57-108">Créez un service WCF nommé « MyWCFService » selon le modèle par défaut « WCF Service Application » dans .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a7f57-108">Create a WCF Service named 'MyWCFService' using the default template 'WCF Service Application' in .NET Framework.</span></span>  <span data-ttu-id="a7f57-109">Ajoutez l’attribut ```[XmlSerializerFormat]``` sur la méthode de service :</span><span class="sxs-lookup"><span data-stu-id="a7f57-109">Add ```[XmlSerializerFormat]``` attribute on the service method like the following</span></span>
    ```c#
    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
2. <span data-ttu-id="a7f57-110">Créez une application de console .NET Core comme application cliente WCF qui cible netcoreapp 2.1 ; par exemple, créez une application nommée « MyWCFClient » avec la commande :</span><span class="sxs-lookup"><span data-stu-id="a7f57-110">Create a .NET Core console application as WCF client application that targets at netcoreapp 2.1, e.g. create an app named 'MyWCFClient' with the command,</span></span>
    ```
    dotnet new console --name MyWCFClient
    ```
    <span data-ttu-id="a7f57-111">Vérifiez que votre csproj cible netcoreapp 2.1.</span><span class="sxs-lookup"><span data-stu-id="a7f57-111">Make sure your csproj targets a netcoreapp 2.1.</span></span> <span data-ttu-id="a7f57-112">Pour cela, utilisez l’élément XML suivant dans votre fichier .csproj :</span><span class="sxs-lookup"><span data-stu-id="a7f57-112">This is done using the following XML element in your .csproj file</span></span>
    ```xml
    <TargetFramework>netcoreapp2.1</TargetFramework>
    ```
3. <span data-ttu-id="a7f57-113">Ajoutez une référence de package à System.ServiceModel.Http en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a7f57-113">Add a package reference to System.ServiceModel.Http by running the following command:</span></span>
   
   ```dotnet add package System.ServiceModel.Http -v 4.5.0```

4. <span data-ttu-id="a7f57-114">Ajoutez le code du client WCF :</span><span class="sxs-lookup"><span data-stu-id="a7f57-114">Add the WCF Client code:</span></span>
    ```csharp
    using System.ServiceModel;
    
    class Program
    {
        static void Main(string[] args)
        {
            var myBinding = new BasicHttpBinding();
            var myEndpoint = new EndpointAddress("http://localhost:2561/Service1.svc"); //Fill your service url here
            var myChannelFactory = new ChannelFactory<IService1>(myBinding, myEndpoint);
            IService1 client = myChannelFactory.CreateChannel();
            string s = client.GetData(1);
            ((ICommunicationObject)client).Close();
        }
    }

    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
5. <span data-ttu-id="a7f57-115">Modifiez le fichier .csproj et ajoutez une référence au package dotnet-svcutil.xmlserializer.</span><span class="sxs-lookup"><span data-stu-id="a7f57-115">Edit the .csproj file and add a reference to the dotnet-svcutil.xmlserializer package.</span></span> <span data-ttu-id="a7f57-116">Exemple :</span><span class="sxs-lookup"><span data-stu-id="a7f57-116">For example:</span></span>

    <span data-ttu-id="a7f57-117">i.</span><span class="sxs-lookup"><span data-stu-id="a7f57-117">i.</span></span> <span data-ttu-id="a7f57-118">Exécutez la commande : `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0`.</span><span class="sxs-lookup"><span data-stu-id="a7f57-118">Run command: `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0`</span></span>

    <span data-ttu-id="a7f57-119">ii.</span><span class="sxs-lookup"><span data-stu-id="a7f57-119">ii.</span></span> <span data-ttu-id="a7f57-120">Ajoutez les lignes suivantes dans MyWCFClient.csproj :</span><span class="sxs-lookup"><span data-stu-id="a7f57-120">Add the following lines in MyWCFClient.csproj,</span></span>
    ```xml
    <ItemGroup>
      <DotNetCliToolReference Include="dotnet-svcutil.xmlserializer" Version="1.0.0" />
    </ItemGroup>
    ```

6. <span data-ttu-id="a7f57-121">Générez l’application en exécutant `dotnet build`.</span><span class="sxs-lookup"><span data-stu-id="a7f57-121">Build the application by running `dotnet build`.</span></span> <span data-ttu-id="a7f57-122">Si tout fonctionne, un assembly nommé MyWCFClient.XmlSerializers.dll est généré dans le dossier de sortie.</span><span class="sxs-lookup"><span data-stu-id="a7f57-122">If everything succeeds, an assembly named MyWCFClient.XmlSerializers.dll will be generated in the output folder.</span></span> <span data-ttu-id="a7f57-123">Des avertissements s’affichent dans la sortie de build si l’outil n’est pas parvenu à générer l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a7f57-123">You will see warnings in the build output if the tool failed to generate the assembly.</span></span>

7. <span data-ttu-id="a7f57-124">Démarrez le service WCF, par exemple, en exécutant http://localhost:2561/Service1.svc dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="a7f57-124">Start the WCF service e.g. by running http://localhost:2561/Service1.svc in the browser.</span></span> <span data-ttu-id="a7f57-125">Lancez ensuite l’application cliente, qui chargera et utilisera automatiquement les sérialiseurs prégénérés à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a7f57-125">Then start the client application, and it will automatically load and use the pre-generated serializers at runtime.</span></span>
