#accounttoken 
#Generateaccess_token
GET/POST/auth/token/create
## Parameter

| Name | Type   | Required or not | Description                           |
| ---- | ------ | --------------- | ------------------------------------- |
| code | String | Yes             | oauth code, get from app callback URL |

## Response Parameters

| Name               | Type   | Description                                                               |
| ------------------ | ------ | ------------------------------------------------------------------------- |
| expires_in         | Number | The expiring time of the access token, in seconds                         |
| account_id         | String | Account ID，Allow null. if(account_platform=seller_center) account_id=null |
| seller_id          | String | Seller id                                                                 |
| user_id            | String | User id                                                                   |
| short_code         | String | Seller short code                                                         |
| account_platform   | String | Account platform                                                          |
| access_token       | String | Access token                                                              |
| account            | String | User account(login user)                                                  |
| refresh_token      | String | Refresh token, used to refresh the token when “refresh_expires_in”>0.     |
| refresh_expires_in | Number | The expiring time of th refresh token                                     |
 #Generateaccess_token JAVA
"IopClient client = new IopClientImpl(UrlConstants.API_GATEWAY_URL_TW, appkey, appSecret); IopRequest request = new IopRequest(); request.setApiName("/auth/token/create"); request.addApiParameter("code", "2_2DL4DV3jcU1UOT7WGI1A4rY91"); IopResponse response = client.execute(request); System.out.println(response.getBody()); Thread.sleep(10);"

#Generateaccess_token PHP
"$c = new IopClient(UrlConstants::$api_gateway_url_tw,appkey,appSecret); $request = new IopRequest('/auth/token/create'); $request->addApiParam('code','2_2DL4DV3jcU1UOT7WGI1A4rY91'); var_dump($c->execute($request));"

#Generateaccess_token .NET
"IIopClient client = new IopClient(UrlConstants.API_GATEWAY_URL_TW, appkey, appSecret); IopRequest request = new IopRequest(); request.SetApiName("/auth/token/create"); request.AddApiParameter("code", "2_2DL4DV3jcU1UOT7WGI1A4rY91"); IopResponse response = client.Execute(request); Console.WriteLine(response.IsError()); Console.WriteLine(response.Body);"

#Generateaccess_token PYTHON
"client = iop.IopClient(url, appkey ,appSecret) request = iop.IopRequest('/auth/token/create') request.add_api_param('code', '2_2DL4DV3jcU1UOT7WGI1A4rY91') response = client.execute(request) print(response.type) print(response.body)"

#Generateaccess_token Streamlined Return
"{ "access_token": "50000601c30atpedfgu3LVvik87Ixlsvle3mSoB7701ceb156fPunYZ43GBg", "refresh_token": "500016000300bwa2WteaQyfwBMnPxurcA0mXGhQdTt18356663CfcDTYpWoi", "account_id": "7063844", "code": "0", "user_id": "100001", "account_platform": "seller_center", "refresh_expires_in": "60", "expires_in": "10", "request_id": "0ba2887315178178017221014", "seller_id": "1001", "account": "xxx@gmail.com", "short_code": "TW1001" }"


