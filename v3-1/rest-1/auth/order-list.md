# Get order list

## `GET` /orders/{pair}

## Parameters

| Header | Path | Query | Type | Required | Description | Default | Range | Example |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| X-BITOPRO-APIKEY |  |  | string | Yes | [API Key](../authentication.md#api-key) |  |  |  |
| X-BITOPRO-PAYLOAD |  |  | string | Yes | [Payload](../authentication.md#payload) |  |  |  |
| X-BITOPRO-SIGNATURE |  |  | string | Yes | [Signature](../authentication.md#signature) |  |  |  |
|  | pair |  | string | Yes | The trading pair in format ${BASE}\_${QUOTE}, Please follow the [link](https://www.bitopro.com/fees) to check the pair list. |  |  | bito\_eth |
|  |  | page | integer | No | The page number for the query. | 1 |  | 1 |
|  |  | active | bool | No | The flag to specify if only active\(in progress\) orders will return. | `false` | `true`, `false` | true |
|  |  | startTime | long | No | The start of timestamp to filter the orders. | 0 |  | 1596158198653 |
|  |  | endTime | long | No | The end of timestamp to filter the orders. | 0 |  | 1596158198653 |

## Response sample

```javascript
{
  "data": [
    {
      "action": "BUY",
      "avgExecutionPrice": "0",
      "bitoFee": "0",
      "executedAmount": "0",
      "fee": "0",
      "feeSymbol": "bito",
      "id": "887521192",
      "originalAmount": "1000",
      "pair": "bito_eth",
      "price": "0.005",
      "remainingAmount": "1000",
      "seq": "BITOETH8913789893",
      "status": 0,
      "timestamp": 1570591525592,
      "total": "0",
      "type": "LIMIT"
    },
    {
      "action": "BUY",
      "avgExecutionPrice": "0",
      "bitoFee": "0",
      "condition": ">=",
      "executedAmount": "0",
      "fee": "0",
      "feeSymbol": "bito",
      "id": "SL-1133804403",
      "originalAmount": "1000",
      "pair": "bito_eth",
      "price": "0.05",
      "remainingAmount": "1000",
      "seq": "BITOETH4618822599",
      "status": -1,
      "stopPrice": "10",
      "timestamp": 1570591225827,
      "total": "0",
      "type": "STOP_LIMIT"
    },
    {
      "action": "BUY",
      "avgExecutionPrice": "0",
      "bitoFee": "0",
      "condition": ">=",
      "executedAmount": "0",
      "fee": "0",
      "feeSymbol": "bito",
      "id": "SL-6256946008",
      "originalAmount": "1000",
      "pair": "bito_eth",
      "price": "0.05",
      "remainingAmount": "1000",
      "seq": "BITOETH2471338952",
      "status": -1,
      "stopPrice": "10",
      "timestamp": 1570591217063,
      "total": "0",
      "type": "STOP_LIMIT"
    }
  ],
  "page": 1,
  "totalPages": 1
}
```

[Back](../rest.md)

