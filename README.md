# Getting start with the MoonPay Login demo

## Getting Started guide
[MoonPay Wallets SDK Step-by-Step Guide](https://docs.moonpay.com/login-sdk/jxM5rh5T22VMnnSFRdS7/wallets-sdk/wallets-sdk-step-by-step-guide)

## Introduction

```bash
git clone https://github.com/moonpay/login-sdk-demo.git
cd login-sdk-demo
npm install
```

Next you need to import the SDK in your project. Add the following line to your code, and replace them with the API_KEY we provided.

```javascript
const sdk = new MoonpayWalletSDK({
  loginDomain: "https://buy-sandbox.moonpay.com",
  secureWalletDomain: "https://web3.moonpay.com",
  apiKey: "pk_test_123",
});
```

Now all you need to do is `init()` the SDK and you're ready to go!

```javascript
  // In this example we use React hooks
  // so we can use the provider in our app
  // when the component is mounted
  useEffect(() => {
    sdk.init().then(() => {
      setProvider(sdk.provider!);
    });
  }, []);
```

## Usage

Run the following command to start the demo:

```bash
npm start
```
