Umbraco version: 13.9.3
uSync version: 13.3.1

🗂 uSync Files
Check out the files in the uSync_example folder to learn how to create a valid uSync file.
Important: GUIDs in uSync files must be exactly 32 hexadecimal characters, formatted like this:
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Example: a1b2c3d4-e5f6-7890-abcd-1234567890ef
<n></n> is invalid. it must be <Name></Name>
When generating sample content (uSync files) from a document type, if the document type includes media picker properties, reference existing media items in the generated uSync files.

📁 static_html Folder
The static_html folder contains static HTML files. These are used when generating .cshtml files that are linked to templates in Umbraco CMS.

🧠 Razor View Rendering
When rendering content in razor view (.cshtml files) don't use Model-Based Rendering, use Dynamic Rendering  