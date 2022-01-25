# Create API Service

### Step 1
create enviroment file and add **main** url end point
file name **enviroment.js**
```
let apiUrl = "http://api.example.com";
let apiAuthUrl = "http://api.example.com";

const URLs = {
  apiUrl,
  apiAuthUrl
};

export default URLs;
```
**Use like this**
```
import URLs from "config/environment";
```

## Step 2
Create new url file to store all sub endpoint seperately for all pages
file name **url.js**
```
export const SignUrl = {
  SIGN_UP: URLs.apiUrl + "/api/v1/vendor-register"
};
````

## Step 3
Create new resusable service for different methods and functionality
file name **signup-service.js** inside **service** folder
```
import axios from "axios";
import { SignUrl } from "./url";

const signup = (request, headers = {}, params = {}) => {
  return axios.post(SignUrl.SIGN_UP, request, {
    headers: headers,
    params: params
  });
};

const SignupService = {
  signup
};  

export default SignupService;
```
**use like this**
```
SignupService.signup(data)
.then()
.catch()
```
