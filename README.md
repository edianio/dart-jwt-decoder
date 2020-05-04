## JWT Decoder

This is a small library for decoding a json web token for dart / flutter. Since the header and payload is base64 encoded you can easily know the stored data with no password, you can also know if the token is expired or not.

If you like this library there's a version for Vue [here](https://github.com/gustavo0197/vue-easy-jwt).

## Getting Started

#### Decode a token
```dart
main() {
  String yourToken = "Your JWT";
  Map<String, dynamic> decodedToken = JwtDecoder.decode(yourToken);
  
  // If the token has a valid format, you will get a Map<String, dynamic>
  // Your decoded token can look like:
  // { 
  //    "sub": "1234567890", 
  //    "name": "Gustavo", 
  //    "iat": 1516239022, 
  //    "exp": 1516239022, 
  //    "randomKey": "something else" 
  // }
}
```

#### Know if the token is expired
```dart
main() {
  String yourToken = "Your JWT";
  bool hasExpired = JwtDecoder.isExpired(yourToken);
  
  // You will get a true / false response
  // true: if the token is already expired
  // false: if the token is not expired
}
```
