# points-exercise
Go Lang Points exercise


*renamed project to points-exercise, due to points application in linux*
# Install 
* to download source code
```
go get github.com/pwarmuz/points-exercise
```
> * understand where source code is located
> * this depends on where your gopath is configured, The general path would be as follows
> * for source code: {root of wherever gopath configuration}/src/github.com/pwarmuz/points
> * for binary: {root of wherever gopath configuration}/bin/points(<-Executable>)
> * There is an option to recompile it from source under the run heading below if there are any running issues


# Run
## Notes
* source code uses Port 8080 for http serving
* to change this, change `const PORT string = ":8080"` to `const PORT string = ":XXXX"` within `routing.go`, where XXXX is the port number, making sure to leave it as a string with `:` prepended

## **Quick run**
*In command* 
```
points-exercise
```

## *Re-compile and run (if all else fails due to configuration or your source code changes)*
*In command, with source code location as directory* 
```
cd {root of wherever gopath configuration}/src/github.com/pwarmuz/points-exercise
go build && go run .
```

# Interacting with server
* use any browser
* type `http://localhost:8080/` where 8080 is the port number, if you decided to change this then adjust accordingly
* to play out the scenario in the exercise, type in 5000 within the "Deduct field" and submit
## Valid URLS
* `http://localhost:8080/`
* `http://localhost:8080/balance`
## To add points
use the Add field, insert required fields and submit
## To deduct points
use the Deduct field, insert points to deduct and submit
## To add user/ change current user
use the Add User/ Change User field, insert a username and submit
## To delete a user
use the Delete User field, insert username and submit


# Testing
```
cd {root of wherever gopath configuration}/src/github.com/pwarmuz/points-exercise
go test -cover
```
[response] PASS coverage: 48.1% of statements