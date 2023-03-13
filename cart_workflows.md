




# Cart 1 
https://www.figma.com/proto/TQHONTvvjdnSmeR6TeoejF/20221210?node-id=10%3A184&scaling=min-zoom&page-id=0%3A1&starting-point-node-id=10%3A184


## Top Restaurant Banner

### Data Format

| Attribute                     | Type          | Description                                        |
| ----------------------------- | ------------- | -------------------------------------------------- |
| vendor_id                     | string        | vendor ID.                                         |
| vendor_name                   | string        | vendor name.                                       |

### Example

```json
{
  "vendor_id": "R00001",
  "vendor_name": "Golden Mile Fish Porridge & Seafood Soup"
}
```


## Delivery Time Banner

### Data Format

| Attribute                     | Type          | Description                                        |
| ----------------------------- | ------------- | -------------------------------------------------- |
| expected_delivery_at          | string        | The planned delivery date in RFC3339Nano format.   |

### Example

```json
{
  "expected_delivery_at": "2022-10-28T13:51:04.032429+07:00"
}
```


## Dish Banner

### Data Format

#### Vendor_Dish

| Attribute                     | Type                            | Description                                        |
| ----------------------------- | ------------------------------- | -------------------------------------------------- |
| vendor_id                     | string                          | vendor ID.                                         |
| vendor_name                   | string                          | vendor name.                                       |
| dish                          | array[Dish]                     | The list of dishes in the order.                   |

#### Dish

| Attribute                     | Type          | Description                                        |
| ----------------------------- | ------------- | -------------------------------------------------- |
| dish_name                     | string        | Dish name.                                         |
| quantity                      | number        | Quantity of same dish being ordered.               |
| unit_cost                     | 64-bit        | Dish unit cost.                                    |
| dish_remark                   | string        | Additional remark for dish being ordered           |


### Example

```json
{
  "dish_name": "Signature Sliced Fish Soup",
  "quantity": "Signature Sliced Fish Soup",
}
```
```json
{
  "vendor_id": "R00001",
  "vendor_name": "Golden Mile Fish Porridge & Seafood Soup"
  "dish": [
    {
      "dish_name": "Signature Sliced Fish Soup",
      "quantity": 1,
      "unit_cost": 7.80
      "dish_remark": "Without Lettuce, Without Milk"
    }
  ]
}
```

