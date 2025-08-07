Below is the information about the project you should follow

Library Versions
- Umbraco version: 13.9.3
- uSync version: 13.3.1

Rules when generating uSync Files
- Check out the files in the uSync_example folder to learn how to create a valid uSync file.
- GUIDs in uSync files must be exactly 32 hexadecimal characters, formatted like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx and all of them can only be hex digits: 0–9 and a–f. Example: a1b2c3d4-e5f6-7890-abcd-1234567890ef
- In uSync content, <n></n> is invalid, it must be <Name></Name>
- Anytime when generating a document type with template. Do the following tasks:
+ Create a corresponding template and razor view (.cshtml)
+ Find a corresponding static html in static_html folder and implement rendering properties of the document type in razor view
+ Create a sample content from the document type including sample data. If the document type includes media picker properties, reference existing 1920x1080.config file in uSync folder


Rules when rendering properties in Razor Views
- Always add following referencesat the top of razor view
@using Umbraco.Cms.Web.Common.PublishedModels;
@using Umbraco.Cms.Core.Models.PublishedContent;
@using Umbraco.Extensions;
@inherits Umbraco.Cms.Web.Common.Views.UmbracoViewPage
- Don't use Model-Based Rendering, use Dynamic Rendering
+ Example: Use <h1>@Model.Value<string>("pageTitle")</h1> instead of using <h1>@Model.PageTitle</h1>