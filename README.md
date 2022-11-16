# FileSpaces

FileSpaces is a Blazor Server ASP.net cross-platform web application to ease the creation and maintenance of file Upload, Review and Presentation / Download spaces.

## Modules

* Administration
  * Creation of a Space with given Name as a Subfolder under configured Spaces folder
  * Per space:
    * Start uploads - creates new unique upload url if not existing 
    * Pause uploads - disables uploading without creating unique upload url
    * Stop uploads - clears unique upload url

* Uploading
  * Anyone with the unique upload url of a space can upload to it
  * Multiple files can be uploaded at a time, with upload progress shown
    * If a filename already exists:
      * uploaded item is skipped
      * user is informed the file exists, with extra information about it:
        * filesize 
        * last modified date
      * User can rename that specific file locally in their system and retry the upload, or skip it if they realize it's a file they had uploaded themselves and doesn't need updating. If they want to upload an updated file they have to upload a new copy with a different "version" in its filename (say xx_20220530.png) 

* Reviewing

* Presentation / Download

# Install input file component
dotnet add package BlazorInputFile --version 0.2.0
