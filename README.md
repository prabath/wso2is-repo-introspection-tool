# WSO2 Identity Server Git Repo Explorer (rEx)

## Initial Setup
* **Step:0** This relies on Docker, so make sure you have Docker running in your local environment.

* **Step:1** Copy rex.sh (from *wso2is-repo-explorer* directory) to a directory where you want to maintain Identity Server git repositories. Alway better to keep this readonly. Also make the script an executable.
```javascript
\> wget https://github.com/prabath/wso2is-repo-explorer/raw/master/rex.sh
\> chmod +x rex.sh
```
* **Step:2** Initialize git repository explorer. This will checkout all Identity Server repositories and will take some time.

```javascript
\> ./rex.sh init
```

## Usage 

* **Clone** all Identity Server related repositories. If you already performed init, you do not need to do this.

```javascript
\> ./rex.sh clone
```

* **List** out all Identity Server related repositories. You can do this, even without cloning or init.

```javascript
\> ./rex.sh list

Output:
Identity/Security repos under WSO2:
https://github.com/wso2/security-tools.git
https://github.com/wso2/carbon-identity-framework.git
https://github.com/wso2/carbon-security.git

.........

Identity/Security repos under WSO2 Extensions:
https://github.com/wso2-extensions/identity-outbound-auth-amazon.git
https://github.com/wso2-extensions/identity-outbound-auth-basecamp.git
https://github.com/wso2-extensions/identity-outbound-auth-dropbox.git
https://github.com/wso2-extensions/identity-outbound-auth-foursquare.git
https://github.com/wso2-extensions/identity-outbound-auth-github.git
```

* **Find** the git repo, by the name of a Jar file (without the version number)

```javascript
\> ./rex.sh find org.wso2.carbon.identity.authenticator.mutualssl

Output:
https://github.com/wso2-extensions/identity-carbon-auth-mutual-ssl/tree/master/components/org.wso2.carbon.identity.authenticator.mutualssl
```
