# pypetter_grafana_download_csv Configuration 
# All Configuration variable are from .env file
## env variable

### LOGIN
    Syntax
    LOGIN="admin"
    This variable is grafana_user username
    Default value = "admin"
    Required if NO_LOGIN = 0 (False)

### MULTI_SERVER
    Syntax
    MULTI_SERVER="0"
    OR
    MULTI_SERVER="1"
    This variable choose if the panel will be fetch from one grafana server ot not
    when true LINK_PANNEL will include url 
    Default value = "0"
    Required 
### MULTI_SERVER_CREDENTIAL ()
    Syntax
    MULTI_SERVER_CREDENTIAL="0"
    OR
    MULTI_SERVER_CREDENTIAL="1"
    This variable choose if the for each grafana server the app should expect one credential (localhost:3000|admin|admin)
    when true LINK_PANNEL will include url 
    Default value = "0"
    Required 

### PASSWORD
    Syntax
    PASSWORD="admin"
    This variable is grafana_user password
    Default value = "admin"
    Required if NO_LOGIN = 0 (False)

### NO_LOGIN
    Syntax
    NO_LOGIN="1" # Do not use login information to access grafana 
    EX for url="https://play.grafana.org"
    OR
    NO_LOGIN="0"
    This variable chooses if this app should use login information to access grafana or not
    Default value = 0
    Required
### SAVE_LOCAL
    Syntax
    SAVE_LOCAL="1"  #Save the panel data on filesystem
    OR
    SAVE_LOCAL="0" 
    This variable  chooses if this app should save the panel data on filesystem or not
    Default value = 0
    Required
### Req_time_out_s
    Syntax
    Req_time_out_s="30"  
    This variable set how many time the app should wait page for load (increase it for heavy query panel)
    Default value = 30
    special value 0 disable timeout
    Required
### URL
    Syntax
    URL="https://play.grafana.org"  #grafana demo server url
    URL="http://localhost:3000"     # grafana localhost server url
    This variable is the grafana server url 
    Default value = "http://localhost:3000"
    Required 
### Download_PATH
    Syntax
    Download_PATH="./csv/" 
    This variable is the download file path on the filesystem 
    Default value = "./csv/"
    Required 
### TRACE (Not yet implemented)
    Syntax
    TRACE="0" 
    TRACE="1" 
    This variable is for logging download information such as server , link panel (which can contain variable info also),dashboard name,folder name and time 
    Default value = "0"
    Required 
### LINK_PANNEL
    Syntax
    LINK_PANNEL="/d/000000012/grafana-play-home?orgId=1&viewPanel=5" 
    This variable is for Setting the URI of the panel which contain the data you want
        - Go to the dashboard in grafana
        - select one panel in dashboard
        -View the panel 
        - then select the right variable value if you want to
        - then Copy the url (CTRL + L then CTRL + C )
        - Drop the server url part
        - be sure there is  "&viewPanel=" in the link query param

    No Default value
    Required 
Download_PATH="./csv2/"
#FOLDER="25"

#### Notes
    Most binary variable has 0 as false and 1 as true