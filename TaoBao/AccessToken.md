#accounttoken 
#AccessToken 
GET/POST/auth/token/refresh
 
Parameter

|Name|Type|Required or not|Description|
|---|---|---|---|
|refresh_token|String|Yes|refresh_token|

## Response Parameters

| Name               | Type   | Description                                                               |
| ------------------ | ------ | ------------------------------------------------------------------------- |
| expires_in         | Number | The expiring time of the access token, in seconds                         |
| account_id         | String | Account ID，Allow null. if(account_platform=seller_center) account_id=null |
| user_Id            | String | User ID                                                                   |
| seller_Id          | String | Seller ID                                                                 |
| short_code         | String | The short code that is assigned to each seller ID by TW Seller Center     |
| account_platform   | String | Account platform                                                          |
| access_token       | String | Access token                                                              |
| account            | String | User account(login user)                                                  |
| refresh_token      | String | Refresh token, used to refresh the token when “refresh_expires_in”>0.     |
| refresh_expires_in | Number | The expiring time of th refresh token                                     |
| error_code         | String | error_code                                                                |
#AccessToken GET/POST/auth/token/refresh : 
JAVA
"IopClient client = new IopClientImpl(UrlConstants.API_GATEWAY_URL_TW, appkey, appSecret); IopRequest request = new IopRequest(); request.setApiName("/auth/token/refresh"); request.addApiParameter("refresh_token", "50001600212wcwiOabwyjtEH11acc19aBOvQr9ZYkYDlr987D8BB88LIB8bj"); IopResponse response = client.execute(request); System.out.println(response.getBody()); Thread.sleep(10);"

#AccessToken PHP
"$c = new IopClient(UrlConstants::$api_gateway_url_tw,appkey,appSecret); $request = new IopRequest('/auth/token/refresh'); $request->addApiParam('refresh_token','50001600212wcwiOabwyjtEH11acc19aBOvQr9ZYkYDlr987D8BB88LIB8bj'); var_dump($c->execute($request));"

#AccessToken .NET
"IIopClient client = new IopClient(UrlConstants.API_GATEWAY_URL_TW, appkey, appSecret); IopRequest request = new IopRequest(); request.SetApiName("/auth/token/refresh"); request.AddApiParameter("refresh_token", "50001600212wcwiOabwyjtEH11acc19aBOvQr9ZYkYDlr987D8BB88LIB8bj"); IopResponse response = client.Execute(request); Console.WriteLine(response.IsError()); Console.WriteLine(response.Body);"

#AccessToken PYTHON
"client = iop.IopClient(url, appkey ,appSecret) request = iop.IopRequest('/auth/token/refresh') request.add_api_param('refresh_token', '50001600212wcwiOabwyjtEH11acc19aBOvQr9ZYkYDlr987D8BB88LIB8bj') response = client.execute(request) print(response.type) print(response.body)"

#AccessToken Streamlined Return
"{ "code": "0", "access_token": "50000601c30atpedfgu3LVvik87Ixlsvle3mSoB7701ceb156fPunYZ43GBg", "refresh_token": "500016000300bwa2WteaQyfwBMnPxurcA0mXGhQdTt18356663CfcDTYpWoi", "account_id": "7063844", "user_Id": "1001", "account_platform": "seller_center", "refresh_expires_in": "60", "error_code": "error_code", "expires_in": "10", "request_id": "0ba2887315178178017221014", "seller_Id": "10011", "account": "xxx@126.com", "short_code": "HK001" }"

