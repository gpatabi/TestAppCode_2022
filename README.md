var client = new RestClient("https://host.my.salesforce.com/services/oauth2/token");
client.Timeout = -1;
var request = new RestRequest(Method.POST);
request.AddHeader("Content-Type", "application/x-www-form-urlencoded");
request.AddParameter("grant_type", "client_credentials");
request.AddParameter("client_id", "<<>>");
request.AddParameter("client_secret", "<<>>");
IRestResponse response = client.Execute(request);
Console.WriteLine(response.Content);
