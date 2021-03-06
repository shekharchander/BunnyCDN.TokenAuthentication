# BunnyCDN.TokenAuthentication
## Java Version
### Introduction
This requires _Java 7_ or _Java 8_ to run.

To begin, add `TokenSigner.java` file to your project. Make sure to include `lib` as it contains dependencies required by the library.

Alternatively, a compiled version is available in `build`.

Once you've done so, import it in the class in which you require a signed URL.

### Usage
Before usage, import the module:

	import BunnyCDN.TokenSigner;

For simplicity of use, the initializer object _does not do anything_. It merely provides access to the `.signUrl()` method which returns a string (URL).

For example, 

	TokenSigner temp = new TokenSigner();
	System.out.println(temp.signUrl("https://token-tester.b-cdn.net/300kb.jpg", "YOUR_SECURITY_TOKEN", "3600", null, false, "/", "CA", null));

The above should return a fully assembled URL:

	https://token-tester.b-cdn.net/300kb.jpg?token=D_TzYipa3d4pNEFKhLMFxMeNq7Ve_-es4H411dQIzDo&token_countries=CA&token_path=%2F&expires=1917511595

An example is available in `/EXAMPLES`.
