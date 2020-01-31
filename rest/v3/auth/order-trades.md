# Get order trades

### `GET` /orders/trades/{pair}

All data is limited to within 90 days.

### Parameters

| Header              | Path | Query  | Type    | Required | Description                                                                                                                 | Default | Range           | Example  |
| ------------------- | ---- | ------ | ------- | -------- | --------------------------------------------------------------------------------------------------------------------------- | ------- | --------------- | -------- |
| X-BITOPRO-APIKEY    |      |        | string  | Yes      | [API Key](../../authentication.md#api-key)                                                                                     |         |                 |          |
| X-BITOPRO-PAYLOAD   |      |        | string  | Yes      | [Payload](../../authentication.md#payload)                                                                                     |         |                 |          |
| X-BITOPRO-SIGNATURE |      |        | string  | Yes      | [Signature](../../authentication.md#signature)                                                                                 |         |                 |          |
|                     | pair |        | string  | Yes      | The trading pair in format ${BASE}_${QUOTE}, Please follow the [link](https://www.bitopro.com/fees) to check the pair list. |         |                 | bito_eth |
|                     |      | orderId   | integer | No       | The order id the get trade history for the specific order.                                                                                              | 1       |                 | 1        |
|                     |      | from   | integer | No       | The `from` (inclusive) unix timestamp for trade to get trade history. Will be ignored if orderId is given.                                                          |        |                 | 1570591525        |
|                     |      | to   | integer | No       | The `to` (inclusive) unix timestamp for trade to get trade history.  Will be ignored if orderId is given.                                                             |        |                 | 1570591525        |
|                     |      | page   | integer | No       | The page number for the query.                                                                                              | 1       |                 | 1        |


### Response sample

```js
{
    "data": [
        {
            "tradeId": "3679558352",
            "orderId": "4876858394",
            "price": "0.08574",
            "action": "BUY",
            "amount": "1",
            "fee": "129.5967742",
            "feeSymbol": "BITO",
            "isTaker": false,
            "timestamp": 1574151316226
        },
        {
            "tradeId": "9753716788",
            "orderId": "4876858394",
            "price": "0.08574",
            "action": "BUY",
            "amount": "1",
            "fee": "129.5967742",
            "feeSymbol": "BITO",
            "isTaker": false,
            "timestamp": 1574151522135
        },
        {
            "tradeId": "4630575183",
            "orderId": "6631583189",
            "price": "0.08574",
            "action": "BUY",
            "amount": "1",
            "fee": "129.5967742",
            "feeSymbol": "BITO",
            "isTaker": false,
            "timestamp": 1574151522135
        },
        {
            "tradeId": "9507433577",
            "orderId": "4384291972",
            "price": "0.08574",
            "action": "BUY",
            "amount": "1",
            "fee": "129.5967742",
            "feeSymbol": "BITO",
            "isTaker": false,
            "timestamp": 1574151572215
        },
        {
            "tradeId": "9261150366",
            "orderId": "9014867155",
            "price": "0.08574",
            "action": "SELL",
            "amount": "1",
            "fee": "0",
            "feeSymbol": "BTC",
            "isTaker": true,
            "timestamp": 1574219341520
        },
        {
            "tradeId": "9261150366",
            "orderId": "4138008761",
            "price": "0.08574",
            "action": "BUY",
            "amount": "1",
            "fee": "0",
            "feeSymbol": "BTC",
            "isTaker": false,
            "timestamp": 1574219341520
        },
        {
            "tradeId": "9014867155",
            "orderId": "8768583944",
            "price": "0.08574",
            "action": "SELL",
            "amount": "1",
            "fee": "0",
            "feeSymbol": "BTC",
            "isTaker": true,
            "timestamp": 1574219419880
        },
        {
            "tradeId": "9014867155",
            "orderId": "3891725550",
            "price": "0.08574",
            "action": "BUY",
            "amount": "1",
            "fee": "0",
            "feeSymbol": "BTC",
            "isTaker": false,
            "timestamp": 1574219419880
        },
        {
            "tradeId": "8768583944",
            "orderId": "8522300733",
            "price": "0.08574",
            "action": "SELL",
            "amount": "1",
            "fee": "0",
            "feeSymbol": "BTC",
            "isTaker": true,
            "timestamp": 1574219457466
        }
    ],
    "page": 1,
    "totalPages": 1
}
```

[Back](../rest.md)