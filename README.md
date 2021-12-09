# CSharp_AsyncWebScrape
## Reads web async in a Task
###### Previev
** Requires **
> System.Threading.Tasks
> System.IO
> System.Net


1. | var scrape= Task.Run( async () =>{
2. | WebRequest request = HttpWebRequest.Create(new Uri("URL"));
WebResponse response = await request.GetResponseAsync();
StreamReader reader=new StreamReader(response.GetResponseStream());
return await reader.ReadToEndAsync();
});
// scrape.Result;


