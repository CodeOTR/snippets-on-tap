# Download a Public File

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/401)
  
  ## Code Snippet
  ```
  const { data } = supabase
.storage
.from('public-bucket')
.getPublicUrl('folder/avatar1.png', {
  download: true,
})
  ```
  
  ## Description
  This code snippet demonstrates how to download a public file from a Supabase storage bucket using the Supabase JavaScript client.

The code first imports the `data` object from the Supabase client instance. It then uses the `storage` property to access the storage API and specifies the name of the storage bucket ('public-bucket') using the `from` method.

The `getPublicUrl` method is called to retrieve the public URL of the file 'folder/avatar1.png'. The `download` option is set to `true` to indicate that the file should be downloaded.

The resulting public URL can be used to download the file directly or displayed to the user for download.
  
  ## Tags
  supabase, storage, download, public-file, javascript
