# <a name="using-dotnet-svcutilxmlserializer-on-net-core"></a>Utiliser dotnet-svcutil.xmlserializer sur .NET Core

## <a name="prerequisites"></a>Prérequis

Les éléments suivants sont nécessaires pour faire fonctionner dotnet-svcutil.xmlserializer. 

* [SDK .NET Core 2.1 ou version ultérieure](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300)
* [Runtime .NET Core 2.1 (ou version ultérieure)](https://www.microsoft.com/net/download/dotnet-core/runtime-2.1.0)

Vous pouvez utiliser la commande `dotnet --info` pour savoir quelles versions du runtime et du kit SDK .NET Core sont déjà installées.

Pour utiliser dotnet-svcutil.xmlserializer dans une application console .NET Core :

1. Créez un service WCF nommé « MyWCFService » selon le modèle par défaut « WCF Service Application » dans .NET Framework.  Ajoutez l’attribut ```[XmlSerializerFormat]``` sur la méthode de service :
    ```c#
    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
2. Créez une application de console .NET Core comme application cliente WCF qui cible netcoreapp 2.1 ; par exemple, créez une application nommée « MyWCFClient » avec la commande :
    ```
    dotnet new console --name MyWCFClient
    ```
    Vérifiez que votre csproj cible netcoreapp 2.1. Pour cela, utilisez l’élément XML suivant dans votre fichier .csproj :
    ```xml
    <TargetFramework>netcoreapp2.1</TargetFramework>
    ```
3. Ajoutez une référence de package à System.ServiceModel.Http en exécutant la commande suivante :
   
   ```dotnet add package System.ServiceModel.Http -v 4.5.0```

4. Ajoutez le code du client WCF :
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
5. Modifiez le fichier .csproj et ajoutez une référence au package dotnet-svcutil.xmlserializer. Exemple :

    i. Exécutez la commande : `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0`.

    ii. Ajoutez les lignes suivantes dans MyWCFClient.csproj :
    ```xml
    <ItemGroup>
      <DotNetCliToolReference Include="dotnet-svcutil.xmlserializer" Version="1.0.0" />
    </ItemGroup>
    ```

6. Générez l’application en exécutant `dotnet build`. Si tout fonctionne, un assembly nommé MyWCFClient.XmlSerializers.dll est généré dans le dossier de sortie. Des avertissements s’affichent dans la sortie de build si l’outil n’est pas parvenu à générer l’assembly.

7. Démarrez le service WCF, par exemple, en exécutant http://localhost:2561/Service1.svc dans le navigateur. Lancez ensuite l’application cliente, qui chargera et utilisera automatiquement les sérialiseurs prégénérés à l’exécution.
