# Access to GPU workstations for class project 

* Email instructor for the account request
* You will receive an email when access is granted 
  * use your University wide netID and pass to loging
  * remote access: 
```
>>ssh netID@zeus.cs.txstate.edu
```
then
```
ssh <workstation>.cs.txstate.edu 
```

## Package installs 

* Start with: 
```
python -m pip install --user pipenv
```
	* if it fails, email cs_helpdesk@txstate.edu and CC me

* Create environment
```
python3 -m venv cs7311_env
```
  * for a python3 venv with a name "cs7311_env "
  
* activate environment 
```
source cs7311_env/bin/activate
```
*Install all the required python packages for the project in this new environment
  * use pip install. 

*To come out of the virtual env use :
```
>deactivate 
```

# Access to LEAP account for class project 

* Email instructor for account request

* you will hear back from Shane or leap@txstate.edu once account is setup
* follow instructions
* Questions on setup: 
  * leap@txstate.edu 
  