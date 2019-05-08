# ![LOGO](logo.png) Orders **flow**ground Connector

## Description

A generated **flow**ground connector for the Orders API (version 3.0.1).

Generated from: https://api.apis.guru/v2/specs/walmart.com/order/3.0.1/swagger.json<br/>
Generated at: 2019-05-07T17:44:48+03:00

## API Description

Please make sure you use the correct version of the APIs for your use case. To find out the appropriate version, go to the API Docs  drop down on the menu.

## Authorization

This API does not require authorization.

## Actions

### Get all orders

> You can display a list of all orders with the query parameter filter criteria.

*Tags:* `Version 3`

#### Input Parameters
* `shipNode` - _optional_ - Ship Node
* `sku` - _optional_ - Retrieves all orders with the specified SKU.
* `customerOrderId` - _optional_ - Retrives the details of the specified customerOrderId.
* `purchaseOrderId` - _optional_ - The purchase order ID associated with the order to retrieve. One customer order can have multiple purchase orders associated with it.
* `status` - _optional_ - The list of orders corresponding to the requested status.
* `createdStartDate` - _optional_ - Limit orders to those created after this date or a timestamp.
* `createdEndDate` - _optional_ - Limit orders to those created before this date or timestamp.
* `fromExpectedShipDate` - _optional_ - Limit orders to those that have order lines with an expected ship date after this date.
* `toExpectedShipDate` - _optional_ - Limit orders to those that have order lines with an expected ship date before this date. 
* `limit` - _optional_ - The number of orders to be returned. Do not set this parameter to over 200 orders.
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Get all released orders

> You can display all released orders that have been created and are ready for fulfilment.

*Tags:* `Version 3`

#### Input Parameters
* `shipNode` - _optional_ - Ship Node
* `createdStartDate` - _required_ - Limit orders to those created after this date or a timestamp.
* `limit` - _optional_ - The number of orders to be returned. Do not set this parameter to over 200 orders.
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Get released orders for next page

> You can display all released orders that have been created and are ready for fulfilment with nextCursor path parameter.

*Tags:* `Version 3`

#### Input Parameters
* `nextCursor` - _required_ - Used for pagination when there are more than 200 orders to retrieve. The nextCursor value of the returned response includes a link to another GET call to retrieve the next page. Copy the link and paste it in the next call.
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Get an order

> You can display details of a specific order based on the purchaseOrderId.

*Tags:* `Version 3`

#### Input Parameters
* `purchaseOrderId` - _required_ - Purchase Order ID
* `shipNode` - _optional_ - Ship Node
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Acknowledge orders

> You can acknowledge an entire order, including all of its order lines. Walmart business rules require to acknowledge orders within four hour of receipt of the order, except in extenuating circumstances.

*Tags:* `Version 3`

#### Input Parameters
* `purchaseOrderId` - _required_ - Purchase Order ID
* `shipNode` - _optional_ - Ship Node
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Cancel order lines

> You can cancel one or more order lines. You must include a purchaseOrderLineNumber when cancelling an order. After cancelling your order, update the inventory for the cancelled order and send it in the next inventory feed.

*Tags:* `Version 3`

#### Input Parameters
* `purchaseOrderId` - _required_ - Purchase Order ID
* `shipNode` - _optional_ - Ship Node
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Refund order lines

> You can refund one or more order lines that have been shipped. The response to a successful call contains the order with the refunded line item.

*Tags:* `Version 3`

#### Input Parameters
* `purchaseOrderId` - _required_ - Purchase Order ID
* `shipNode` - _optional_ - Ship Node
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Shipping updates

> You can change the status of order lines to "Shipped" and trigger the charge to a customer. You must acknowledge your orders before sending a shipping update to avoid underselling. An order line, once marked as shipped, cannot be updated.

*Tags:* `Version 3`

#### Input Parameters
* `purchaseOrderId` - _required_ - Purchase Order ID
* `shipNode` - _optional_ - Ship Node
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

### Get orders for next page

> You can display a list of all orders with nextCursor path parameter pagination criteria.

*Tags:* `Version 3`

#### Input Parameters
* `nextCursor` - _required_ - Used for pagination when there are more than 200 orders to retrieve. The nextCursor value of the returned response includes a link to another GET call to retrieve the next page. Copy the link and paste it in the next call.
* `Content-Type` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `Accept` - _required_ - application/xml,
application/json
    Possible values: application/xml, application/json.
* `WM_CONSUMER.CHANNEL.TYPE` - _required_ - Channel Type
    Possible values: SWAGGER_CHANNEL_TYPE.
* `WM_CONSUMER.ID` - _required_ - Your Consumer ID
* `WM_SEC.TIMESTAMP` - _required_ - Epoch timestamp
* `WM_SEC.AUTH_SIGNATURE` - _required_ - Authentication signature
* `WM_SVC.NAME` - _required_ - The Service name
* `WM_QOS.CORRELATION_ID` - _required_ - A Transaction ID

## License

**flow**ground :- Telekom iPaaS / walmart-com-order-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
