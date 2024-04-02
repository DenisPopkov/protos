## Proto auth file

``` text
service Auth {
  rpc Register (RegisterRequest) returns (RegisterResponse);
  rpc Login (LoginRequest) returns (LoginResponse);
}

message RegisterRequest {
  string phone = 1; // phone number of the user to register
  string password = 2; // password of the user to register
  int64 feed = 3; // feed id
  string name = 4; // user name
  string image = 5; // user image
}

message RegisterResponse {
  int64 user_id = 1; // user ID of the registered user
  string user_name = 2; // user name of the registered user
  string user_image = 3; // user image of the registered user
}

message LoginRequest {
  string phone = 1; // phone number of the user to register
  string password = 2; // password of the user to register
  int32  app_id = 3; // ID of the app to login to
}

message LoginResponse {
  string token = 1; // auth jwt token of the logged in user
}
```
