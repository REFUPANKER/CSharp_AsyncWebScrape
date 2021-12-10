# CSharp_AsyncWebScrape
## Reads web async in a Task
###### Previev
**Requires**
- > System.Threading.Tasks
 System.IO
 System.Net



``` var scrape= Task.Run( async () =>{ <br />
WebRequest request = HttpWebRequest.Create(new Uri("URL")); <br />
WebResponse response = await request.GetResponseAsync(); <br />
StreamReader reader=new StreamReader(response.GetResponseStream()); <br />
return await reader.ReadToEndAsync(); <br />
}); <br/>
// scrape.Result; <br/>
```


