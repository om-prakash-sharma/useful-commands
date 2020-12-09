## To check if port is available
- sudo netstat -nlp | grep :80

## To kill process on specfic port 
- sudo kill -9 process_id

## To connect with server
- ssh user_name@IP_ADDRESS

## To connect with server using pem file
- ssh -i __PEM_FILE__.pem user_name@IP_ADDRESS

## Copy file from one server to other server
- scp -i __PEM_FILE__.pem __SOURCE_FILE_PATH__ user_name@IP_ADDRESS:__OUTPUT_PATH__

