# 概要

[公式](https://stripe.com/docs/billing/quickstart)から react,node.js の設定にして持ってきたコード

# Prebuilt Checkout page with subscriptions

Explore a full, working code sample of an integration with Stripe Checkout and Customer Portal. The client- and server-side code redirects to a prebuilt payment page hosted on Stripe. Included are some basic build and run scripts you can use to start up the application.

## Running the sample

1. Build the application

```
npm install
```

2. Run the application

```
npm start
```

3. Go to [http://localhost:3000/checkout](http://localhost:3000/checkout)

4. lookup_key は自分で設定した、実際に使うものにしておく必要がある（以下のように設定）

```ts
// 参考記事：https://stripe.com/docs/api/prices/update#update_price-lookup_key

require("dotenv").config();

const stripe = require("stripe")("sk_XXXXXXXXXXX");

stripe.prices.update("price_XXXXXXXXXXX", {
  lookup_key: "lookup_keyの名前にしたい文字列",
});
```
