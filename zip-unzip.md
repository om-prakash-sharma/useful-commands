## To zip any folder in lunux
- zip -r __NEW_ZIP_FILE_NAME__.zip ./__OUTPUT_FILE_PATH__ -x '*.git*'
  - X : exclude any folder
  - r : include sub directory 

## To unzip any file in linux
- unzip -o /home/__FILE_PATH__.zip  -d /home/__OUTPUT_PATH__
  - O : zip file path 
  - d : destination path