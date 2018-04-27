### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection ne peut plus se connecter à SQL Server 1997 ou des bases de données à l’aide de l’adaptateur VIA

|   |   |
|---|---|
|Détails|Les connexions aux bases de données SQL Server à l’aide du [protocole VIA (Virtual Interface Adapter)](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) ne sont plus prises en charge. Le protocole utilisé pour se connecter à une base de données SQL Server est visible dans la chaîne de connexion. Une connexion VIA contiendra via:&lt;nom_serveur&gt;. Si cette application se connecte à SQL via un protocole autre que le protocole VIA (tcp: ou np:, par exemple), aucune modification avec rupture n’est détectée. De plus, les connexions à SQL Server 7 (1997) ne sont plus prises en charge.|
|Suggestion|Comme le protocole VIA est déprécié, un autre protocole doit être utilisé pour se connecter aux bases de données SQL. Le protocole utilisé le plus courant est TCP/IP. Les instructions pour l’activation du protocole TCP/IP sont accessibles [ici](https://msdn.microsoft.com/library/bb909712.aspx). Si la base de données est accessible uniquement à partir d’un intranet, le protocole des canaux nommés peut offrir de meilleures performances en cas de réseau lent.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

