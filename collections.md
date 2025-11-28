---
title: CLIENT APIs3
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.30"

---

# CLIENT APIs3

Base URLs:

# Authentication

- HTTP Authentication, scheme: bearer

# Deliveries

## GET get deliveries

GET /deliveries

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|paginate|query|string| yes |can be 1 or 0|
|per_page|query|string| yes |none|
|filter|query|string| yes |all|today|yesterday|created_at|assigned_at|dropoff_at|schedule_date|
|start_date|query|string| yes |none|
|end_date|query|string| yes |none|
|delivery_status|query|string| yes |pending|awaiting_pickup|in_transit|delivered|cancelled|declined|
|creation_mode|query|string| no |automated|manual|via booking|imported|
|search|query|string| no |none|
|group_by|query|string| no |sender_city|receiver_city|
|tag_id|query|string| no |none|
|scheduled|query|string| no |none|
|schedule_date|query|string| no |none|
|search_all_locations|query|string| no |boolean|
|partner_id|query|string| no |none|
|delivery_in_all_locations|query|string| no |none|
|rider_id|query|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "message": "Deliveries retrieved successfully!",
  "data": {
    "delivery_counts": {
      "overall_scheduled_deliveries": 0,
      "overall_user_pending_deliveries": 0,
      "overall_user_awaiting_pickup_deliveries": 0,
      "overall_user_in_transit_deliveries": 0,
      "overall_user_delivered_deliveries": 0,
      "overall_user_cancelled_deliveries": 0,
      "overall_partners_delivered_deliveries": 0
    },
    "grouped_deliveries": null,
    "deliveries": {
      "data": [
        {
          "uuid": "60630d45-98b8-441d-a5d7-5b779681f9ec",
          "order_number": "KMACG",
          "fleet_identity_number": "96667461",
          "status": "Pending",
          "status_label": "Pending",
          "sender_longitude": null,
          "sender_latitude": null,
          "customer_longitude": null,
          "customer_latitude": null,
          "delivery_fee": 125,
          "total_delivery_amount": 125,
          "service_charge": 103.125,
          "rider_commission": 0,
          "currency": "NGN",
          "location": {
            "id": "980e0e64-14ee-4e0f-b78b-c95ea3bdffe1",
            "name": "Default Location",
            "currency": "NGN",
            "is_default": true,
            "location_code": "DEFDE3550",
            "created_at": "2025-09-02T10:06:47.000000Z"
          },
          "can_view": false,
          "note": null,
          "creation_mode": "Manual",
          "scheduled": false,
          "schedule_date": null,
          "schedule_time": null,
          "schedule_date_time": null,
          "schedule_due_status": null,
          "created_at": "2025-09-19T23:45:18.000000Z",
          "pickup_at": null,
          "dropoff_at": null,
          "customer_detail": [
            {
              "uuid": "c2f4a611-5258-4bb0-940e-56b7eeff6530",
              "delivery_uuid": "c2f4a611-5258-4bb0-940e-56b7eeff6530",
              "status": "Pending",
              "dropoff_photo": null,
              "customer_name": "Victor Maduforo",
              "customer_email": null,
              "customer_phone_number": "8131013478",
              "customer_phone_code": "234",
              "customer_address": "Penthouse - DC, Demo Estate, 404, Not Found Road, Lagos, Nigeria",
              "created_at": "2025-09-19T23:45:18.000000Z",
              "items": [
                {
                  "uuid": "04b00b7d-eedf-4e6f-bca3-969d97787c46",
                  "item_description": "Midea 463L Top Mount Direct Cool Refrigerator - SBS (MDRT645MTU46)",
                  "item_quantity": 1,
                  "item_value": "30.00",
                  "item_discount": 0,
                  "currency": "NGN",
                  "item_type_id": null,
                  "item_type": null,
                  "created_at": "2025-09-19T23:45:18.000000Z"
                }
              ]
            }
          ],
          "sender_detail": {
            "uuid": "3af0d770-08bb-451d-8508-03eb0bce1da6",
            "sender_name": "Arc Freight",
            "sender_phone": "8130057256",
            "sender_email": "mantchi@gmail.com",
            "sender_phonecode": "234",
            "sender_address": "85 Allen Avenue, Ikeja, Lagos, Nigeria",
            "business_owned": true,
            "created_at": "2025-09-19T23:45:18.000000Z",
            "updated_at": "2025-09-19T23:45:18.000000Z"
          },
          "tag": null,
          "rider_info": null,
          "delivery_info_from_rider": null,
          "is_paid": false,
          "pickup_photo": null,
          "dropoff_photo": null,
          "cancellation_reason": null,
          "cancelled_by": {
            "name": null,
            "photo": null
          },
          "show_delivery_fee": true,
          "metadata": null,
          "partner_direction": "from_partner"
        },
        {
          "uuid": "5150bf01-09d9-47e2-accf-b9fb26e660dd",
          "order_number": "GP856",
          "fleet_identity_number": "96667461",
          "status": "Pending",
          "status_label": "Pending",
          "sender_longitude": null,
          "sender_latitude": null,
          "customer_longitude": null,
          "customer_latitude": null,
          "delivery_fee": 125,
          "total_delivery_amount": 125,
          "service_charge": 103.125,
          "rider_commission": 0,
          "currency": "NGN",
          "location": {
            "id": "980e0e64-14ee-4e0f-b78b-c95ea3bdffe1",
            "name": "Default Location",
            "currency": "NGN",
            "is_default": true,
            "location_code": "DEFDE3550",
            "created_at": "2025-09-02T10:06:47.000000Z"
          },
          "can_view": false,
          "note": null,
          "creation_mode": "Manual",
          "scheduled": false,
          "schedule_date": null,
          "schedule_time": null,
          "schedule_date_time": null,
          "schedule_due_status": null,
          "created_at": "2025-09-19T23:45:14.000000Z",
          "pickup_at": null,
          "dropoff_at": null,
          "customer_detail": [
            {
              "uuid": "89935ad3-fec4-4395-8774-b14fb5da8930",
              "delivery_uuid": "89935ad3-fec4-4395-8774-b14fb5da8930",
              "status": "Pending",
              "dropoff_photo": null,
              "customer_name": "Victor Maduforo",
              "customer_email": null,
              "customer_phone_number": "8131013478",
              "customer_phone_code": "234",
              "customer_address": "Penthouse - DC, Demo Estate, 404, Not Found Road, Lagos, Nigeria",
              "created_at": "2025-09-19T23:45:14.000000Z",
              "items": [
                {
                  "uuid": "ff851885-0746-428b-bc7c-9e447e41db43",
                  "item_description": "Midea 463L Top Mount Direct Cool Refrigerator - SBS (MDRT645MTU46)",
                  "item_quantity": 1,
                  "item_value": "30.00",
                  "item_discount": 0,
                  "currency": "NGN",
                  "item_type_id": null,
                  "item_type": null,
                  "created_at": "2025-09-19T23:45:14.000000Z"
                }
              ]
            }
          ],
          "sender_detail": {
            "uuid": "0cdd0675-b7fd-45d1-9edb-74ba4f7e2f20",
            "sender_name": "Arc Freight",
            "sender_phone": "8130057256",
            "sender_email": "mantchi@gmail.com",
            "sender_phonecode": "234",
            "sender_address": "85 Allen Avenue, Ikeja, Lagos, Nigeria",
            "business_owned": true,
            "created_at": "2025-09-19T23:45:14.000000Z",
            "updated_at": "2025-09-19T23:45:14.000000Z"
          },
          "tag": null,
          "rider_info": null,
          "delivery_info_from_rider": null,
          "is_paid": false,
          "pickup_photo": null,
          "dropoff_photo": null,
          "cancellation_reason": null,
          "cancelled_by": {
            "name": null,
            "photo": null
          },
          "show_delivery_fee": true,
          "metadata": null,
          "partner_direction": "from_partner"
        }
      ],
      "links": {
        "first": "http://localhost/api/deliveries?delivery_status=pending&partner_id=982051ce-9976-476a-a103-6ebddf094b24&page=1",
        "last": "http://localhost/api/deliveries?delivery_status=pending&partner_id=982051ce-9976-476a-a103-6ebddf094b24&page=1",
        "prev": null,
        "next": null
      },
      "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "links": [
          {
            "url": null,
            "label": "&laquo; Previous",
            "active": false
          },
          {
            "url": "http://localhost/api/deliveries?delivery_status=pending&partner_id=982051ce-9976-476a-a103-6ebddf094b24&page=1",
            "label": "1",
            "active": true
          },
          {
            "url": null,
            "label": "Next &raquo;",
            "active": false
          }
        ],
        "path": "http://localhost/api/deliveries",
        "per_page": 10,
        "to": 2,
        "total": 2
      }
    }
  },
  "status": "success"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» message|string|true|none||none|
|» data|object|true|none||none|
|»» delivery_counts|object|true|none||none|
|»»» overall_scheduled_deliveries|integer|true|none||none|
|»»» overall_user_pending_deliveries|integer|true|none||none|
|»»» overall_user_awaiting_pickup_deliveries|integer|true|none||none|
|»»» overall_user_in_transit_deliveries|integer|true|none||none|
|»»» overall_user_delivered_deliveries|integer|true|none||none|
|»»» overall_user_cancelled_deliveries|integer|true|none||none|
|»»» overall_partners_delivered_deliveries|integer|true|none||none|
|»» grouped_deliveries|null|true|none||none|
|»» deliveries|object|true|none||none|
|»»» data|[object]|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» order_number|string|true|none||none|
|»»»» fleet_identity_number|string|true|none||none|
|»»»» status|string|true|none||none|
|»»»» status_label|string|true|none||none|
|»»»» sender_longitude|null|true|none||none|
|»»»» sender_latitude|null|true|none||none|
|»»»» customer_longitude|null|true|none||none|
|»»»» customer_latitude|null|true|none||none|
|»»»» delivery_fee|integer|true|none||none|
|»»»» total_delivery_amount|integer|true|none||none|
|»»»» service_charge|number|true|none||none|
|»»»» rider_commission|integer|true|none||none|
|»»»» currency|string|true|none||none|
|»»»» location|object|true|none||none|
|»»»»» id|string|true|none||none|
|»»»»» name|string|true|none||none|
|»»»»» currency|string|true|none||none|
|»»»»» is_default|boolean|true|none||none|
|»»»»» location_code|string|true|none||none|
|»»»»» created_at|string|true|none||none|
|»»»» can_view|boolean|true|none||none|
|»»»» note|null|true|none||none|
|»»»» creation_mode|string|true|none||none|
|»»»» scheduled|boolean|true|none||none|
|»»»» schedule_date|null|true|none||none|
|»»»» schedule_time|null|true|none||none|
|»»»» schedule_date_time|null|true|none||none|
|»»»» schedule_due_status|null|true|none||none|
|»»»» created_at|string|true|none||none|
|»»»» pickup_at|null|true|none||none|
|»»»» dropoff_at|null|true|none||none|
|»»»» customer_detail|[object]|true|none||none|
|»»»»» uuid|string|true|none||none|
|»»»»» delivery_uuid|string|true|none||none|
|»»»»» status|string|true|none||none|
|»»»»» dropoff_photo|null|true|none||none|
|»»»»» customer_name|string|true|none||none|
|»»»»» customer_email|null|true|none||none|
|»»»»» customer_phone_number|string|true|none||none|
|»»»»» customer_phone_code|string|true|none||none|
|»»»»» customer_address|string|true|none||none|
|»»»»» created_at|string|true|none||none|
|»»»»» items|[object]|true|none||none|
|»»»»»» uuid|string|true|none||none|
|»»»»»» item_description|string|true|none||none|
|»»»»»» item_quantity|integer|true|none||none|
|»»»»»» item_value|string|true|none||none|
|»»»»»» item_discount|integer|true|none||none|
|»»»»»» currency|string|true|none||none|
|»»»»»» item_type_id|null|true|none||none|
|»»»»»» item_type|null|true|none||none|
|»»»»»» created_at|string|true|none||none|
|»»»» sender_detail|object|true|none||none|
|»»»»» uuid|string|true|none||none|
|»»»»» sender_name|string|true|none||none|
|»»»»» sender_phone|string|true|none||none|
|»»»»» sender_email|string|true|none||none|
|»»»»» sender_phonecode|string|true|none||none|
|»»»»» sender_address|string|true|none||none|
|»»»»» business_owned|boolean|true|none||none|
|»»»»» created_at|string|true|none||none|
|»»»»» updated_at|string|true|none||none|
|»»»» tag|null|true|none||none|
|»»»» rider_info|null|true|none||none|
|»»»» delivery_info_from_rider|null|true|none||none|
|»»»» is_paid|boolean|true|none||none|
|»»»» pickup_photo|null|true|none||none|
|»»»» dropoff_photo|null|true|none||none|
|»»»» cancellation_reason|null|true|none||none|
|»»»» cancelled_by|object|true|none||none|
|»»»»» name|null|true|none||none|
|»»»»» photo|null|true|none||none|
|»»»» show_delivery_fee|boolean|true|none||none|
|»»»» metadata|null|true|none||none|
|»»»» partner_direction|string|true|none||none|
|»»» links|object|true|none||none|
|»»»» first|string|true|none||none|
|»»»» last|string|true|none||none|
|»»»» prev|null|true|none||none|
|»»»» next|null|true|none||none|
|»»» meta|object|true|none||none|
|»»»» current_page|integer|true|none||none|
|»»»» from|integer|true|none||none|
|»»»» last_page|integer|true|none||none|
|»»»» links|[object]|true|none||none|
|»»»»» url|string¦null|true|none||none|
|»»»»» label|string|true|none||none|
|»»»»» active|boolean|true|none||none|
|»»»» path|string|true|none||none|
|»»»» per_page|integer|true|none||none|
|»»»» to|integer|true|none||none|
|»»»» total|integer|true|none||none|
|» status|string|true|none||none|

## POST move to in transit

POST /deliveries/move_to_in_transit

> Body Parameters

```yaml
"delivery_uuid[0]": "{{delivery_uuid}}"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid[0]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Delivery status updated, notifications sent."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## POST move to in delivered

POST /deliveries/move_to_delivered

> Body Parameters

```yaml
"delivery_uuid[0]": "{{delivery_uuid}}"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid[0]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Delivery status updated, notifications sent."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## GET get sms estimate

GET /

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "estimated_sms_charge": 16,
    "currency": "₦"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» estimated_sms_charge|integer|true|none||none|
|»» currency|string|true|none||none|

## POST create delivery

POST /deliveries/create

> Body Parameters

```json
{
  "creation_date": "2025-08-28",
  "delivery_fee": 0,
  "iam_sender": true,
  "riderid": "2ce7ff7a-2c76-4e18-b681-41121ef48631",
  "send_sms": true,
  "sender_address": "85 Allen Avenue, Ikeja, Lagos, Nigeria",
  "sender_email": "devs@venco.co",
  "sender_name": "Takasuki",
  "sender_phone": "8131013478",
  "sender_phonecode": "234",
  "receivers": [
    {
      "customer_address": "Penthouse - DC, Demo Estate, 404, Not Found Road, Lagos, Nigeria",
      "customer_name": "Victor Maduforo",
      "customer_phone_number": "8131013478",
      "customer_phone_code": "234",
      "item_type": "manual",
      "items": [
        {
          "item_description": "Midea 463L Top Mount Direct Cool Refrigerator - SBS (MDRT645MTU46)",
          "item_quantity": 1,
          "item_value": 30
        }
      ]
    }
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» creation_date|body|string| yes |none|
|» delivery_fee|body|integer| yes |none|
|» iam_sender|body|boolean| yes |none|
|» riderid|body|string| yes |none|
|» send_sms|body|boolean| yes |none|
|» sender_address|body|string| yes |none|
|» sender_email|body|string| yes |none|
|» sender_name|body|string| yes |none|
|» sender_phone|body|string| yes |none|
|» sender_phonecode|body|string| yes |none|
|» receivers|body|[object]| yes |none|
|»» customer_address|body|string| no |none|
|»» customer_name|body|string| no |none|
|»» customer_phone_number|body|string| no |none|
|»» customer_phone_code|body|string| no |none|
|»» item_type|body|string| no |none|
|»» items|body|[object]| no |none|
|»»» item_description|body|string| no |none|
|»»» item_quantity|body|integer| no |none|
|»»» item_value|body|integer| no |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "9fd136b9-dd33-4006-859b-5e57906f02b4",
    "order_number": "41127",
    "fleet_identity_number": "63471915",
    "status": "Pending",
    "status_label": "Pending",
    "sender_longitude": null,
    "sender_latitude": null,
    "customer_longitude": null,
    "customer_latitude": null,
    "delivery_fee": 5000,
    "total_delivery_amount": 5250,
    "service_charge": 125,
    "rider_commission": null,
    "currency": "NGN",
    "note": null,
    "creation_mode": null,
    "created_at": "2025-04-15T18:25:54.000000Z",
    "pickup_at": null,
    "dropoff_at": null,
    "customer_detail": [],
    "sender_detail": {
      "uuid": "8e09f8fe-147a-4178-b3be-6b7eec4bf849",
      "sender_name": "Emmanuel Chinatuka",
      "sender_phone": "08087168391",
      "sender_email": "chimaobinice@gmail.com",
      "sender_phonecode": "234",
      "sender_address": "2 Umuleri street, Lagos",
      "business_owned": false,
      "created_at": "2025-04-15T18:25:54.000000Z",
      "updated_at": "2025-04-15T18:25:54.000000Z"
    },
    "rider_info": null,
    "delivery_info_from_rider": null,
    "is_paid": true,
    "pickup_photo": null,
    "dropoff_photo": null,
    "cancellation_reason": null,
    "cancelled_by": {
      "name": null,
      "photo": null
    }
  },
  "message": "Delivery created successfully"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» fleet_identity_number|string|true|none||none|
|»» status|string|true|none||none|
|»» status_label|string|true|none||none|
|»» sender_longitude|null|true|none||none|
|»» sender_latitude|null|true|none||none|
|»» customer_longitude|null|true|none||none|
|»» customer_latitude|null|true|none||none|
|»» delivery_fee|integer|true|none||none|
|»» total_delivery_amount|integer|true|none||none|
|»» service_charge|integer|true|none||none|
|»» rider_commission|null|true|none||none|
|»» currency|string|true|none||none|
|»» note|null|true|none||none|
|»» creation_mode|null|true|none||none|
|»» created_at|string|true|none||none|
|»» pickup_at|null|true|none||none|
|»» dropoff_at|null|true|none||none|
|»» customer_detail|[any]|true|none||none|
|»» sender_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|string|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» business_owned|boolean|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» rider_info|null|true|none||none|
|»» delivery_info_from_rider|null|true|none||none|
|»» is_paid|boolean|true|none||none|
|»» pickup_photo|null|true|none||none|
|»» dropoff_photo|null|true|none||none|
|»» cancellation_reason|null|true|none||none|
|»» cancelled_by|object|true|none||none|
|»»» name|null|true|none||none|
|»»» photo|null|true|none||none|
|» message|string|true|none||none|

## GET get delivery

GET /deliveries/get/delivery_uuid

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "b0febc7b-91a0-43d2-a933-fc1c27dd25c3",
    "order_number": "531886487269",
    "fleet_id": null,
    "status": "Awaiting Pickup",
    "delivery_type": "intra_state",
    "sender_longitude": "7.3445666",
    "sender_latitude": "8.95625",
    "customer_longitude": "7.4974495",
    "customer_latitude": "9.0339358",
    "delivery_fee": "3000",
    "created_at": "2023-12-05T01:02:02.000000Z",
    "customer_detail": {
      "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
      "customer_name": "TundeNasri",
      "customer_email": null,
      "customer_phone_number": "08065302534",
      "customer_phone_code": "234",
      "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
      "created_at": "2023-12-04T22:03:06.000000Z"
    },
    "sender_detail": {
      "uuid": "2743f3a5-b692-4c10-99f7-b3b941f0c3eb",
      "sender_name": "Nuel Geek",
      "sender_phone": "08087168391",
      "sender_email": null,
      "sender_phonecode": "234",
      "sender_address": "Aso housing estate, lugbe",
      "created_at": "2023-12-05T01:02:02.000000Z",
      "updated_at": "2023-12-05T01:02:02.000000Z"
    },
    "items": [
      {
        "uuid": "a67c925e-c9bd-4829-ac2b-c429437f50e1",
        "item_description": "Freshfish",
        "item_quantity": 1,
        "item_value": "10000.00",
        "created_at": "2023-12-05T01:02:02.000000Z"
      }
    ],
    "organization_detail": {
      "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
      "fleet_identity_number": null,
      "business_address": null,
      "phone_number": "8081939285",
      "phone_code": "234",
      "logo": null,
      "created_at": "2023-11-30T16:57:27.000000Z",
      "updated_at": "2023-11-30T16:57:27.000000Z"
    }
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» fleet_id|null|true|none||none|
|»» status|string|true|none||none|
|»» delivery_type|string|true|none||none|
|»» sender_longitude|string|true|none||none|
|»» sender_latitude|string|true|none||none|
|»» customer_longitude|string|true|none||none|
|»» customer_latitude|string|true|none||none|
|»» delivery_fee|string|true|none||none|
|»» created_at|string|true|none||none|
|»» customer_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|null|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»» sender_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|null|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» items|[object]|true|none||none|
|»»» uuid|string|false|none||none|
|»»» item_description|string|false|none||none|
|»»» item_quantity|integer|false|none||none|
|»»» item_value|string|false|none||none|
|»»» created_at|string|false|none||none|
|»» organization_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» fleet_identity_number|null|true|none||none|
|»»» business_address|null|true|none||none|
|»»» phone_number|string|true|none||none|
|»»» phone_code|string|true|none||none|
|»»» logo|null|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|

## POST assign delivery

POST /deliveries/assign/rider_uuid

> Body Parameters

```yaml
"delivery_uuid[]": ae96e085-30fa-4997-86ec-75015771705c

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid[]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": [
    {
      "uuid": "e207ecc7-dcab-439e-88e8-f3e630e53697",
      "order_number": "387451602924",
      "fleet_id": null,
      "status": "Awaiting Pickup",
      "delivery_type": "intra_state",
      "sender_longitude": "7.3445666",
      "sender_latitude": "8.95625",
      "customer_longitude": "7.4974495",
      "customer_latitude": "9.0339358",
      "delivery_fee": "NGN3,000.00",
      "created_at": "2023-12-05T00:51:00.000000Z",
      "customer_detail": {
        "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
        "customer_name": "TundeNasri",
        "customer_email": null,
        "customer_phone_number": "08065302534",
        "customer_phone_code": "234",
        "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
        "created_at": "2023-12-04T22:03:06.000000Z"
      },
      "sender_detail": {
        "uuid": "cadb63c6-577b-4b30-ac6a-c4ca30884631",
        "sender_name": "Nuel Geek",
        "sender_phone": "08087168391",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Aso housing estate, lugbe",
        "created_at": "2023-12-05T00:51:00.000000Z",
        "updated_at": "2023-12-05T00:51:00.000000Z"
      },
      "items": [
        {
          "uuid": "68222706-82e4-4a30-a298-c64bd6240f99",
          "item_description": "Freshfish",
          "item_quantity": 1,
          "item_value": "10000.00",
          "created_at": "2023-12-05T00:51:00.000000Z"
        }
      ]
    },
    {
      "uuid": "b0febc7b-91a0-43d2-a933-fc1c27dd25c3",
      "order_number": "531886487269",
      "fleet_id": null,
      "status": "In Transit",
      "delivery_type": "state_to_state",
      "sender_longitude": "3.3096414",
      "sender_latitude": "6.5352628",
      "customer_longitude": "7.4974495",
      "customer_latitude": "9.0339358",
      "delivery_fee": "NGN3,000.00",
      "created_at": "2023-12-05T01:02:02.000000Z",
      "customer_detail": {
        "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
        "customer_name": "TundeNasri",
        "customer_email": null,
        "customer_phone_number": "08065302534",
        "customer_phone_code": "234",
        "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
        "created_at": "2023-12-04T22:03:06.000000Z"
      },
      "sender_detail": {
        "uuid": "2743f3a5-b692-4c10-99f7-b3b941f0c3eb",
        "sender_name": "Nuel Geek",
        "sender_phone": "08087168391",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "2 Umuleri street, Lagos",
        "created_at": "2023-12-05T01:02:02.000000Z",
        "updated_at": "2023-12-06T00:45:41.000000Z"
      },
      "items": [
        {
          "uuid": "cbf13cbb-b817-42ce-b948-12344ff7507f",
          "item_description": "Freshfish",
          "item_quantity": 1,
          "item_value": "10000.00",
          "created_at": "2023-12-06T00:45:41.000000Z"
        },
        {
          "uuid": "7cf6577f-c6e1-40fa-aa98-443ca27cdc3f",
          "item_description": "Freshfish",
          "item_quantity": 1,
          "item_value": "10000.00",
          "created_at": "2023-12-06T01:00:27.000000Z"
        },
        {
          "uuid": "a758c1cb-011a-4f96-9f5e-249bff763e07",
          "item_description": "Canno Camera",
          "item_quantity": 1,
          "item_value": "30000.00",
          "created_at": "2023-12-06T01:00:54.000000Z"
        },
        {
          "uuid": "a67c925e-c9bd-4829-ac2b-c429437f50e1",
          "item_description": "Eva soap pack",
          "item_quantity": 1,
          "item_value": "4000.00",
          "created_at": "2023-12-05T01:02:02.000000Z"
        }
      ]
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|[object]|true|none||none|
|»» uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» fleet_id|null|true|none||none|
|»» status|string|true|none||none|
|»» delivery_type|string|true|none||none|
|»» sender_longitude|string|true|none||none|
|»» sender_latitude|string|true|none||none|
|»» customer_longitude|string|true|none||none|
|»» customer_latitude|string|true|none||none|
|»» delivery_fee|string|true|none||none|
|»» created_at|string|true|none||none|
|»» customer_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|null|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»» sender_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|null|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» items|[object]|true|none||none|
|»»» uuid|string|true|none||none|
|»»» item_description|string|true|none||none|
|»»» item_quantity|integer|true|none||none|
|»»» item_value|string|true|none||none|
|»»» created_at|string|true|none||none|

## POST delete delivery

POST /deliveries/delete/delivery_uuid

> Response Examples

> 422 Response

```json
{
  "status": "error",
  "message": "Delivery does not exist or may have been processed!"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|none|Inline|

### Responses Data Schema

HTTP Status Code **422**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## POST delete multiple deliveries

POST /deliveries/delete_multiple_deliveries

> Body Parameters

```yaml
"delivery_uuid[]": "{{delivery_uuid}}"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid[]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Deliveries deleted."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## POST update delivery

POST /deliveries/update/ae96e085-30fa-4997-86ec-75015771705c

> Body Parameters

```yaml
sender_name: Nuel Geek
sender_address: 2 Umuleri street, Lagos
sender_phone: "08087168391"
sender_phonecode: "234"
sender_email: sender@example.com
"receivers[0][customer_name]": TundeNasri
"receivers[0][customer_address]":
  - TundeNasri
  - TundeNasri
  - 12 Ahmadu Bello way, Central Business District, Abuja
"receivers[0][customer_phone_number]": "08065302534"
"receivers[0][customer_phone_code]": "234"
"receivers[0][customer_email]": sinoma@gmail.com
"receivers[0][items][0][item_uuid]": "{{item_uuid}}"
"receivers[0][items][0][item_description]": Eva soap pack for me
"receivers[0][items][0][item_quantity]": "1"
"receivers[0][items][0][item_value]": "4000"
"receivers[0][items][1][item_description]": Cannon Camera
"receivers[0][items][1][item_quantity]": "1"
"receivers[0][items][1][item_value]": "30000"
delivery_fee: "3000"
send_sms: "1"
creation_date: 13-03-2024
"receivers[0][customer_detail_id]": 4d012972-e3b7-46c7-9362-5409fef8ba6d

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» sender_name|body|string| yes |none|
|» sender_address|body|string| yes |none|
|» sender_phone|body|string| yes |none|
|» sender_phonecode|body|string| yes |none|
|» sender_email|body|string| yes |none|
|» receivers[0][customer_name]|body|string| yes |none|
|» receivers[0][customer_address]|body|array| yes |none|
|» receivers[0][customer_phone_number]|body|string| yes |none|
|» receivers[0][customer_phone_code]|body|string| yes |none|
|» receivers[0][customer_email]|body|string| yes |none|
|» receivers[0][items][0][item_uuid]|body|string| yes |none|
|» receivers[0][items][0][item_description]|body|string| yes |none|
|» receivers[0][items][0][item_quantity]|body|string| yes |none|
|» receivers[0][items][0][item_value]|body|string| yes |none|
|» receivers[0][items][1][item_description]|body|string| yes |none|
|» receivers[0][items][1][item_quantity]|body|string| yes |none|
|» receivers[0][items][1][item_value]|body|string| yes |none|
|» delivery_fee|body|string| yes |none|
|» send_sms|body|string| yes |True Or False|
|» creation_date|body|string| no |none|
|» receivers[0][customer_detail_id]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "b0febc7b-91a0-43d2-a933-fc1c27dd25c3",
    "order_number": "531886487269",
    "fleet_id": null,
    "status": "Awaiting Pickup",
    "delivery_type": "state_to_state",
    "sender_longitude": 3.3096414,
    "sender_latitude": 6.5352628,
    "customer_longitude": 7.4974495,
    "customer_latitude": 9.0339358,
    "delivery_fee": "3000",
    "created_at": "2023-12-05T01:02:02.000000Z",
    "customer_detail": {
      "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
      "customer_name": "TundeNasri",
      "customer_email": null,
      "customer_phone_number": "08065302534",
      "customer_phone_code": "234",
      "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
      "created_at": "2023-12-04T22:03:06.000000Z"
    },
    "sender_detail": {
      "uuid": "2743f3a5-b692-4c10-99f7-b3b941f0c3eb",
      "sender_name": "Nuel Geek",
      "sender_phone": "08087168391",
      "sender_email": null,
      "sender_phonecode": "234",
      "sender_address": "2 Umuleri street, Lagos",
      "created_at": "2023-12-05T01:02:02.000000Z",
      "updated_at": "2023-12-06T00:45:41.000000Z"
    },
    "items": [
      {
        "uuid": "cbf13cbb-b817-42ce-b948-12344ff7507f",
        "item_description": "Freshfish",
        "item_quantity": 1,
        "item_value": "10000.00",
        "created_at": "2023-12-06T00:45:41.000000Z"
      },
      {
        "uuid": "7cf6577f-c6e1-40fa-aa98-443ca27cdc3f",
        "item_description": "Freshfish",
        "item_quantity": 1,
        "item_value": "10000.00",
        "created_at": "2023-12-06T01:00:27.000000Z"
      },
      {
        "uuid": "a758c1cb-011a-4f96-9f5e-249bff763e07",
        "item_description": "Canno Camera",
        "item_quantity": 1,
        "item_value": "30000.00",
        "created_at": "2023-12-06T01:00:54.000000Z"
      },
      {
        "uuid": "a67c925e-c9bd-4829-ac2b-c429437f50e1",
        "item_description": "Eva soap pack",
        "item_quantity": 1,
        "item_value": "4000.00",
        "created_at": "2023-12-05T01:02:02.000000Z"
      }
    ],
    "organization_detail": {
      "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
      "fleet_identity_number": null,
      "business_address": null,
      "phone_number": "8081939285",
      "phone_code": "234",
      "logo": null,
      "created_at": "2023-11-30T16:57:27.000000Z",
      "updated_at": "2023-11-30T16:57:27.000000Z"
    }
  },
  "message": "Delivery updated"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» fleet_id|null|true|none||none|
|»» status|string|true|none||none|
|»» delivery_type|string|true|none||none|
|»» sender_longitude|number|true|none||none|
|»» sender_latitude|number|true|none||none|
|»» customer_longitude|number|true|none||none|
|»» customer_latitude|number|true|none||none|
|»» delivery_fee|string|true|none||none|
|»» created_at|string|true|none||none|
|»» customer_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|null|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»» sender_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|null|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» items|[object]|true|none||none|
|»»» uuid|string|true|none||none|
|»»» item_description|string|true|none||none|
|»»» item_quantity|integer|true|none||none|
|»»» item_value|string|true|none||none|
|»»» created_at|string|true|none||none|
|»» organization_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» fleet_identity_number|null|true|none||none|
|»»» business_address|null|true|none||none|
|»»» phone_number|string|true|none||none|
|»»» phone_code|string|true|none||none|
|»»» logo|null|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|» message|string|true|none||none|

## GET download pdf

GET /deliveries/download_pdf/delivery_uuid

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "pdf generated."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## POST update delivery status

POST /deliveries/update_status

> Body Parameters

```yaml
delivery_uuid: "{{delivery_uuid}}"
status: in_transit
pickup_otp: "097857"
dropoff_otp: "098798"
note: Reason for cancellation

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid|body|string| yes |none|
|» status|body|string| yes |accepted | in_transit | delivered | cancelled|
|» pickup_otp|body|string| no |required if status is in_transit|
|» dropoff_otp|body|string| no |required if status is delivered|
|» note|body|string| no |Reason for cancellation|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "e85616da-906c-4984-8980-069e7f3b2cd9",
    "order_number": "664481112612",
    "status": "Order Accepted",
    "delivery_type": "intra_state",
    "sender_longitude": "7.4724033",
    "sender_latitude": "9.0820999",
    "customer_longitude": "7.4974495",
    "customer_latitude": "9.0339358",
    "created_at": "2023-10-30T18:45:33.000000Z",
    "customer_detail": {
      "id": "8670aeb6-8299-4f0f-8915-31c7db66a7c0",
      "customer_name": "TundeNasri",
      "customer_email": "sinoma@gmail.com",
      "customer_state_id": 304,
      "customer_phone_number": "08065302534",
      "customer_phone_code": "234",
      "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
      "created_at": "2023-10-30T18:45:33.000000Z"
    },
    "delivery_detail": {
      "uuid": "dc09555f-42ac-426b-963c-7d301ea4deb3",
      "sender_name": "Ac Nice",
      "sender_phone": "08087168391",
      "sender_phonecode": "234",
      "sender_address": "T-pumpy estate, phase 20 lugbe, Abuja",
      "delivery_total_order_value": "10000.00",
      "delivery_number_of_parcels": 1,
      "delivery_unit_weight": "10.00",
      "created_at": "2023-10-30T18:45:33.000000Z",
      "updated_at": "2023-10-30T18:45:33.000000Z"
    },
    "items": [
      {
        "uuid": "aee2ca50-bed0-40b3-90da-534097c39f91",
        "item_description": "Freshfish",
        "item_quantity": 1,
        "item_weight": "10.00",
        "item_value": "10000.00",
        "created_at": "2023-10-30T18:45:33.000000Z"
      }
    ],
    "organization_detail": {
      "uuid": "355c96cd-aa77-459e-9107-1223bea38f9b",
      "business_address": "Aso Housing Estate, Airport road, Abuja",
      "country_id": 161,
      "state_id": 303,
      "city": "Abuja",
      "logo": "https://usedora-bucket-dev.s3.amazonaws.com/provider-logos/mwFmcQ7ppveoNULRwL3AEyKtwoHT2KViXte8AYJA.jpg",
      "created_at": "2023-10-15T10:57:05.000000Z",
      "updated_at": "2023-10-28T16:40:21.000000Z"
    }
  },
  "message": "Delivery status updated"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» status|string|true|none||none|
|»» delivery_type|string|true|none||none|
|»» sender_longitude|string|true|none||none|
|»» sender_latitude|string|true|none||none|
|»» customer_longitude|string|true|none||none|
|»» customer_latitude|string|true|none||none|
|»» created_at|string|true|none||none|
|»» customer_detail|object|true|none||none|
|»»» id|string|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|string|true|none||none|
|»»» customer_state_id|integer|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»» delivery_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» delivery_total_order_value|string|true|none||none|
|»»» delivery_number_of_parcels|integer|true|none||none|
|»»» delivery_unit_weight|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» items|[object]|true|none||none|
|»»» uuid|string|false|none||none|
|»»» item_description|string|false|none||none|
|»»» item_quantity|integer|false|none||none|
|»»» item_weight|string|false|none||none|
|»»» item_value|string|false|none||none|
|»»» created_at|string|false|none||none|
|»» organization_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» business_address|string|true|none||none|
|»»» country_id|integer|true|none||none|
|»»» state_id|integer|true|none||none|
|»»» city|string|true|none||none|
|»»» logo|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|» message|string|true|none||none|

## POST track

POST /track

> Body Parameters

```json
{
  "order_number": 78895817
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» order_number|body|integer| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "current_status": "Awaiting-Pickup",
    "order_number": "78895817",
    "stages": {
      "delivery_received": {
        "title": "Delivery request received",
        "reached": true,
        "timestamp": "1 year ago",
        "message": "Waiting for Sendstack to assign your order to a rider."
      },
      "processing": {
        "title": "Delivery request is being processed",
        "reached": true,
        "timestamp": "1 year ago",
        "message": "Your delivery request will be ready in a short while."
      },
      "assigned": {
        "title": "Delivery assigned to a rider",
        "reached": true,
        "timestamp": "1 year ago",
        "message": "Your order is awaiting pickup from rider"
      },
      "declined": {
        "title": "Delivery unassigned from rider",
        "reached": false,
        "timestamp": null,
        "message": "Your delivery order has been rejected by the rider and will be reassigned shortly."
      },
      "picked_up": {
        "title": "Your order has been picked up",
        "reached": false,
        "timestamp": null,
        "message": "Rider is in transit to final destination"
      },
      "delivered": {
        "title": "Order delivered! 🎉",
        "reached": false,
        "timestamp": null,
        "message": " has received the order"
      }
    }
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» current_status|string|true|none||none|
|»» order_number|string|true|none||none|
|»» stages|object|true|none||none|
|»»» delivery_received|object|true|none||none|
|»»»» title|string|true|none||none|
|»»»» reached|boolean|true|none||none|
|»»»» timestamp|string|true|none||none|
|»»»» message|string|true|none||none|
|»»» processing|object|true|none||none|
|»»»» title|string|true|none||none|
|»»»» reached|boolean|true|none||none|
|»»»» timestamp|string|true|none||none|
|»»»» message|string|true|none||none|
|»»» assigned|object|true|none||none|
|»»»» title|string|true|none||none|
|»»»» reached|boolean|true|none||none|
|»»»» timestamp|string|true|none||none|
|»»»» message|string|true|none||none|
|»»» declined|object|true|none||none|
|»»»» title|string|true|none||none|
|»»»» reached|boolean|true|none||none|
|»»»» timestamp|null|true|none||none|
|»»»» message|string|true|none||none|
|»»» picked_up|object|true|none||none|
|»»»» title|string|true|none||none|
|»»»» reached|boolean|true|none||none|
|»»»» timestamp|null|true|none||none|
|»»»» message|string|true|none||none|
|»»» delivered|object|true|none||none|
|»»»» title|string|true|none||none|
|»»»» reached|boolean|true|none||none|
|»»»» timestamp|null|true|none||none|
|»»»» message|string|true|none||none|

## POST move to new location

POST /deliveries/move_to_location

> Body Parameters

```json
{
  "delivery_uuid": [
    "14329293-782d-4c77-96f2-e5ff923a1d2d"
  ],
  "location_code": "NAI1747946840"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid|body|[string]| yes |none|
|» location_code|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Deliveries successfully moved to new location for processing: Nairobi"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## POST Add Tag

POST /deliveries/add_tag

> Body Parameters

```json
{
  "delivery_uuid": "4bed8beb-3d9c-475f-8891-6988910ba89d",
  "name": "Called customer",
  "color_code": "#e41e12"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuid|body|string| yes |none|
|» name|body|string| yes |none|
|» color_code|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "4bed8beb-3d9c-475f-8891-6988910ba89d",
    "order_number": "86250",
    "fleet_identity_number": "63471915",
    "status": "Pending",
    "status_label": "Pending",
    "sender_longitude": null,
    "sender_latitude": null,
    "customer_longitude": null,
    "customer_latitude": null,
    "delivery_fee": "5000",
    "total_delivery_amount": "5500",
    "service_charge": "0",
    "rider_commission": "0",
    "currency": "NGN",
    "note": null,
    "creation_mode": "Manual",
    "created_at": "2025-05-23T16:04:01.000000Z",
    "pickup_at": null,
    "dropoff_at": null,
    "customer_detail": [
      {
        "uuid": "b3d0f2da-70c7-4011-a24c-9ba47ca1337e",
        "delivery_uuid": "b3d0f2da-70c7-4011-a24c-9ba47ca1337e",
        "status": "Pending",
        "dropoff_photo": null,
        "customer_name": "Idris",
        "customer_email": "chimaobinice@gmail.com",
        "customer_phone_number": "09098998983",
        "customer_phone_code": "234",
        "customer_address": "Aso housing estate",
        "created_at": "2025-05-23T16:04:01.000000Z",
        "items": [
          {
            "uuid": "c1eccff0-671e-47ee-8a43-fc6947f7d618",
            "item_description": "C-Way",
            "item_quantity": 4,
            "item_value": "250.00",
            "item_discount": "100",
            "currency": "NGN",
            "item_type_id": null,
            "item_type": null,
            "created_at": "2025-05-23T16:04:01.000000Z"
          }
        ]
      },
      {
        "uuid": "d5395528-1015-45cb-ac4c-66e22fa502bd",
        "delivery_uuid": "d5395528-1015-45cb-ac4c-66e22fa502bd",
        "status": "Pending",
        "dropoff_photo": null,
        "customer_name": "Idris",
        "customer_email": "chimaobinice@gmail.com",
        "customer_phone_number": "09098998983",
        "customer_phone_code": "234",
        "customer_address": "Aso housing estate, Lagos",
        "created_at": "2025-05-23T16:04:01.000000Z",
        "items": [
          {
            "uuid": "c359125a-c174-47ae-8aca-77e982a3fa69",
            "item_description": "C-Way",
            "item_quantity": 4,
            "item_value": "250.00",
            "item_discount": "0",
            "currency": "NGN",
            "item_type_id": null,
            "item_type": null,
            "created_at": "2025-05-23T16:04:01.000000Z"
          }
        ]
      }
    ],
    "sender_detail": {
      "uuid": "632ebe8a-f649-4dc2-85e8-05479967611a",
      "sender_name": "Sendstack",
      "sender_phone": "7086181776",
      "sender_email": "james@gmail.com",
      "sender_phonecode": "234",
      "sender_address": "Road 1 Umumba road",
      "business_owned": true,
      "created_at": "2025-05-23T16:04:01.000000Z",
      "updated_at": "2025-05-23T16:04:01.000000Z"
    },
    "tag": {
      "id": "8c57eac8-9eac-44da-a8bc-b0b7ac6aa385",
      "name": "Called Customer",
      "color_code": "e41e12"
    },
    "rider_info": null,
    "delivery_info_from_rider": null,
    "is_paid": true,
    "pickup_photo": null,
    "dropoff_photo": null,
    "cancellation_reason": null,
    "cancelled_by": {
      "name": null,
      "photo": null
    }
  },
  "message": "Delivery tagged."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» fleet_identity_number|string|true|none||none|
|»» status|string|true|none||none|
|»» status_label|string|true|none||none|
|»» sender_longitude|null|true|none||none|
|»» sender_latitude|null|true|none||none|
|»» customer_longitude|null|true|none||none|
|»» customer_latitude|null|true|none||none|
|»» delivery_fee|string|true|none||none|
|»» total_delivery_amount|string|true|none||none|
|»» service_charge|string|true|none||none|
|»» rider_commission|string|true|none||none|
|»» currency|string|true|none||none|
|»» note|null|true|none||none|
|»» creation_mode|string|true|none||none|
|»» created_at|string|true|none||none|
|»» pickup_at|null|true|none||none|
|»» dropoff_at|null|true|none||none|
|»» customer_detail|[object]|true|none||none|
|»»» uuid|string|true|none||none|
|»»» delivery_uuid|string|true|none||none|
|»»» status|string|true|none||none|
|»»» dropoff_photo|null|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|string|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» items|[object]|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» item_description|string|true|none||none|
|»»»» item_quantity|integer|true|none||none|
|»»»» item_value|string|true|none||none|
|»»»» item_discount|string|true|none||none|
|»»»» currency|string|true|none||none|
|»»»» item_type_id|null|true|none||none|
|»»»» item_type|null|true|none||none|
|»»»» created_at|string|true|none||none|
|»» sender_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|string|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» business_owned|boolean|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» tag|object|true|none||none|
|»»» id|string|true|none||none|
|»»» name|string|true|none||none|
|»»» color_code|string|true|none||none|
|»» rider_info|null|true|none||none|
|»» delivery_info_from_rider|null|true|none||none|
|»» is_paid|boolean|true|none||none|
|»» pickup_photo|null|true|none||none|
|»» dropoff_photo|null|true|none||none|
|»» cancellation_reason|null|true|none||none|
|»» cancelled_by|object|true|none||none|
|»»» name|null|true|none||none|
|»»» photo|null|true|none||none|
|» message|string|true|none||none|

## GET Get Tags

GET /deliveries/tags

> Body Parameters

```json
{}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": [
    {
      "id": "8c57eac8-9eac-44da-a8bc-b0b7ac6aa385",
      "name": "Called Customer",
      "color_code": "e41e12"
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|[object]|true|none||none|
|»» id|string|false|none||none|
|»» name|string|false|none||none|
|»» color_code|string|false|none||none|

## POST Update Tag

POST /deliveries/update_tag

> Body Parameters

```json
{
  "tag_id": "8c57eac8-9eac-44da-a8bc-b0b7ac6aa385",
  "name": "Yet to Call",
  "color_code": "fffff"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» tag_id|body|string| yes |none|
|» name|body|string| yes |none|
|» color_code|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Tag updated.",
  "data": {
    "id": "8c57eac8-9eac-44da-a8bc-b0b7ac6aa385",
    "name": "Yet To Call",
    "color_code": "fffff"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|
|» data|object|true|none||none|
|»» id|string|true|none||none|
|»» name|string|true|none||none|
|»» color_code|string|true|none||none|

## POST Delete Tag

POST /deliveries/delete_tag

> Body Parameters

```json
{
  "tag_id": "8c57eac8-9eac-44da-a8bc-b0b7ac6aa385"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» tag_id|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Tag deleted.",
  "data": []
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|
|» data|[any]|true|none||none|

## POST schedule delivery

POST /deliveries/schedule

> Body Parameters

```json
{
  "delivery_uuids": [
    "8a51a6f4-29ab-4d59-84ad-cb3f136d0f19"
  ],
  "schedule_date": "2025-06-21",
  "schedule_time": "11:00"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» delivery_uuids|body|[string]| yes |none|
|» schedule_date|body|string| yes |none|
|» schedule_time|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Delivery re-scheduled successfully",
  "data": [
    {
      "uuid": "8a51a6f4-29ab-4d59-84ad-cb3f136d0f19",
      "order_number": "95343",
      "fleet_identity_number": "63471915",
      "status": "Pending",
      "status_label": "Pending",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "5000",
      "total_delivery_amount": "5500",
      "service_charge": "0",
      "rider_commission": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "scheduled": true,
      "schedule_date": "2025-06-21",
      "schedule_time": "11:00:00",
      "schedule_date_time": "21 JUN, 2025 - 11:00AM",
      "schedule_due_status": "SCHEDULED",
      "created_at": "2025-06-19T09:45:58.000000Z",
      "pickup_at": null,
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "4c12aa4f-2b87-4b70-87e2-5cec528ad12d",
          "delivery_uuid": "4c12aa4f-2b87-4b70-87e2-5cec528ad12d",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Idris",
          "customer_email": "chimaobinice@gmail.com",
          "customer_phone_number": "09098998983",
          "customer_phone_code": "234",
          "customer_address": "Aso housing estate",
          "created_at": "2025-06-19T09:45:58.000000Z",
          "items": [
            {
              "uuid": "b34783e5-c70b-4b3a-8ed4-b53e8cc4f5fb",
              "item_description": "C-Way",
              "item_quantity": 4,
              "item_value": "250.00",
              "item_discount": "100",
              "currency": "NGN",
              "item_type_id": null,
              "item_type": null,
              "created_at": "2025-06-19T09:45:58.000000Z"
            }
          ]
        },
        {
          "uuid": "17276420-c4f6-4e4d-aafb-327f0aa93b69",
          "delivery_uuid": "17276420-c4f6-4e4d-aafb-327f0aa93b69",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Idris",
          "customer_email": "chimaobinice@gmail.com",
          "customer_phone_number": "09098998983",
          "customer_phone_code": "234",
          "customer_address": "Aso housing estate, Lagos",
          "created_at": "2025-06-19T09:45:58.000000Z",
          "items": [
            {
              "uuid": "06610650-828e-4db8-bfbe-dec704cdeee7",
              "item_description": "C-Way",
              "item_quantity": 4,
              "item_value": "250.00",
              "item_discount": "0",
              "currency": "NGN",
              "item_type_id": null,
              "item_type": null,
              "created_at": "2025-06-19T09:45:58.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "52f185e4-51fc-45dd-be98-4e69af09f7d0",
        "sender_name": "Sendstack",
        "sender_phone": "7086181776",
        "sender_email": "james@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "Road 1 Umumba road",
        "business_owned": true,
        "created_at": "2025-06-19T09:45:58.000000Z",
        "updated_at": "2025-06-19T09:45:58.000000Z"
      },
      "tag": {
        "id": "4e5fdbad-c2f9-46fa-9d25-fd68abf878d6",
        "name": "Called Customer",
        "color_code": "e41e12"
      },
      "rider_info": null,
      "delivery_info_from_rider": null,
      "is_paid": true,
      "pickup_photo": null,
      "dropoff_photo": null,
      "cancellation_reason": null,
      "cancelled_by": {
        "name": null,
        "photo": null
      }
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|
|» data|[object]|true|none||none|
|»» uuid|string|false|none||none|
|»» order_number|string|false|none||none|
|»» fleet_identity_number|string|false|none||none|
|»» status|string|false|none||none|
|»» status_label|string|false|none||none|
|»» sender_longitude|null|false|none||none|
|»» sender_latitude|null|false|none||none|
|»» customer_longitude|null|false|none||none|
|»» customer_latitude|null|false|none||none|
|»» delivery_fee|string|false|none||none|
|»» total_delivery_amount|string|false|none||none|
|»» service_charge|string|false|none||none|
|»» rider_commission|string|false|none||none|
|»» currency|string|false|none||none|
|»» note|null|false|none||none|
|»» creation_mode|string|false|none||none|
|»» scheduled|boolean|false|none||none|
|»» schedule_date|string|false|none||none|
|»» schedule_time|string|false|none||none|
|»» schedule_date_time|string|false|none||none|
|»» schedule_due_status|string|false|none||none|
|»» created_at|string|false|none||none|
|»» pickup_at|null|false|none||none|
|»» dropoff_at|null|false|none||none|
|»» customer_detail|[object]|false|none||none|
|»»» uuid|string|true|none||none|
|»»» delivery_uuid|string|true|none||none|
|»»» status|string|true|none||none|
|»»» dropoff_photo|null|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|string|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» items|[object]|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» item_description|string|true|none||none|
|»»»» item_quantity|integer|true|none||none|
|»»»» item_value|string|true|none||none|
|»»»» item_discount|string|true|none||none|
|»»»» currency|string|true|none||none|
|»»»» item_type_id|null|true|none||none|
|»»»» item_type|null|true|none||none|
|»»»» created_at|string|true|none||none|
|»» sender_detail|object|false|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|string|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» business_owned|boolean|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» tag|object|false|none||none|
|»»» id|string|true|none||none|
|»»» name|string|true|none||none|
|»»» color_code|string|true|none||none|
|»» rider_info|null|false|none||none|
|»» delivery_info_from_rider|null|false|none||none|
|»» is_paid|boolean|false|none||none|
|»» pickup_photo|null|false|none||none|
|»» dropoff_photo|null|false|none||none|
|»» cancellation_reason|null|false|none||none|
|»» cancelled_by|object|false|none||none|
|»»» name|null|true|none||none|
|»»» photo|null|true|none||none|

## GET Delivery Activity Logs

GET /deliveries/activity_logs/delivery_uuid

> Body Parameters

```yaml
{}

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": [
    {
      "month": "July 2025",
      "logs": [
        {
          "causer_name": "james@gmail.com",
          "causer_profile_photo": "https://usedora-bucket-dev.s3.amazonaws.com/provider-logos/X5xQzSnl3Mn1k4YhgvNGVyN2ViP4dkXygIE1fY9U.png",
          "description": "Delivery status changed from Pending to In-Transit by user: james@gmail.com",
          "log_name": "Changed status",
          "created_at": "July 02, 2025. 03:26am",
          "month": "July 2025"
        }
      ]
    },
    {
      "month": "June 2025",
      "logs": [
        {
          "causer_name": "james@gmail.com",
          "causer_profile_photo": "https://usedora-bucket-dev.s3.amazonaws.com/provider-logos/X5xQzSnl3Mn1k4YhgvNGVyN2ViP4dkXygIE1fY9U.png",
          "description": "Delivery created with order number: FYQSJ by user: james@gmail.com",
          "log_name": "Delivery Created",
          "created_at": "June 30, 2025. 10:34pm",
          "month": "June 2025"
        }
      ]
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|[object]|true|none||none|
|»» month|string|true|none||none|
|»» logs|[object]|true|none||none|
|»»» causer_name|string|true|none||none|
|»»» causer_profile_photo|string|true|none||none|
|»»» description|string|true|none||none|
|»»» log_name|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» month|string|true|none||none|

## POST get delivery fee

POST /booking_inbound/link_code/get_delivery_fee

> Body Parameters

```json
"{\n    \"sender_address\": \"Aso housing estate, Lugbe, Abuja\",\n    \"receiver_address\": \"Grandeur squares and cubes estate, FHA, Lugbe, Abuja\",\n    \"scope\":\"\" // insterstate, intracity\n}"
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» sender_address|body|string| yes |none|
|» receiver_address|body|string| yes |none|
|» scope|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Riders

## POST create rider

POST /riders/create

> Body Parameters

```json
"{\r\n    \"rider_emails\":[\"kingddsassa@gmail.com\"],\r\n    \"commission_value\": 10,\r\n    \"commission_type\" : \"commission\" //commission, fixed\r\n}"
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» rider_emails|body|[string]| yes |none|
|» commission_value|body|integer| yes |none|
|» commission_type|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "9dbb0847-a2ba-4cdb-b904-72fd9ab2f3bc",
    "riderid": 45689646,
    "name": "Nice Chimaobi",
    "address": "Aso housing estate, lugbe",
    "phone_number": "08028492844",
    "phone_code": "234",
    "email": "king@gmail.com",
    "vehicle_plate_number": "Ae93480G",
    "photo": "https://usedora-bucket-dev.s3.amazonaws.com/photos/oNhnn9x1fxoiPkJ3kbJUxYWNa6L4iusIChYI2B8G.jpg",
    "created_at": "2023-12-03T07:47:46.000000Z"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» riderid|integer|true|none||none|
|»» name|string|true|none||none|
|»» address|string|true|none||none|
|»» phone_number|string|true|none||none|
|»» phone_code|string|true|none||none|
|»» email|string|true|none||none|
|»» vehicle_plate_number|string|true|none||none|
|»» photo|string|true|none||none|
|»» created_at|string|true|none||none|

## GET Pending Riders Invites

GET /riders

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|pending_invites|query|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "total_number_of_riders": 1,
    "total_active_riders": 1,
    "total_deactivated_riders": 0,
    "total_number_of_fulfilled_orders": 9,
    "total_revenue": 31050,
    "riders": [
      {
        "uuid": "9b2a7ad9-aefb-4495-9d17-f893e817e594",
        "riderid": "9b2a7ad9-aefb-4495-9d17-f893e817e594",
        "name": null,
        "address": null,
        "phone_number": null,
        "phone_code": "234",
        "email": "moses@gmail.com",
        "vehicle_plate_number": null,
        "photo": null,
        "total_completed_delivery": 0,
        "invite_status": "pending",
        "active": false,
        "number_of_ongoing_deliveries": 0,
        "total_revenue_by_rider": 0,
        "rider_ongoing_deliveries": null,
        "created_at": "2024-07-04T20:12:47.000000Z"
      },
      {
        "uuid": "4d778510-c8d2-407e-ba73-4a333b671a21",
        "riderid": "4d778510-c8d2-407e-ba73-4a333b671a21",
        "name": "angwamoses@gmail.com",
        "address": "My home",
        "phone_number": "07089183428",
        "phone_code": "234",
        "email": "angwamoses@gmail.com",
        "vehicle_plate_number": null,
        "photo": null,
        "total_completed_delivery": 0,
        "invite_status": "pending",
        "active": false,
        "number_of_ongoing_deliveries": 0,
        "total_revenue_by_rider": 0,
        "rider_ongoing_deliveries": null,
        "created_at": "2024-07-04T20:12:45.000000Z"
      }
    ]
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» total_number_of_riders|integer|true|none||none|
|»» total_active_riders|integer|true|none||none|
|»» total_deactivated_riders|integer|true|none||none|
|»» total_number_of_fulfilled_orders|integer|true|none||none|
|»» total_revenue|integer|true|none||none|
|»» riders|[object]|true|none||none|
|»»» uuid|string|true|none||none|
|»»» riderid|string|true|none||none|
|»»» name|string¦null|true|none||none|
|»»» address|string¦null|true|none||none|
|»»» phone_number|string¦null|true|none||none|
|»»» phone_code|string|true|none||none|
|»»» email|string|true|none||none|
|»»» vehicle_plate_number|null|true|none||none|
|»»» photo|null|true|none||none|
|»»» total_completed_delivery|integer|true|none||none|
|»»» invite_status|string|true|none||none|
|»»» active|boolean|true|none||none|
|»»» number_of_ongoing_deliveries|integer|true|none||none|
|»»» total_revenue_by_rider|integer|true|none||none|
|»»» rider_ongoing_deliveries|null|true|none||none|
|»»» created_at|string|true|none||none|

## POST activate riders

POST /riders/activate

> Body Parameters

```yaml
"rider_uuids[]": "{{rider_uuid}}"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» rider_uuids[]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "9dbb0847-a2ba-4cdb-b904-72fd9ab2f3bc",
    "riderid": "45689646",
    "name": "Nice Chimaobi",
    "address": "Aso housing estate, lugbe",
    "phone_number": "08028492844",
    "phone_code": "234",
    "email": "king@gmail.com",
    "vehicle_plate_number": "Ae93480G",
    "photo": "https://usedora-bucket-dev.s3.amazonaws.com/photos/oNhnn9x1fxoiPkJ3kbJUxYWNa6L4iusIChYI2B8G.jpg",
    "total_completed_delivery": 0,
    "active": false,
    "created_at": "2023-12-03T07:47:46.000000Z"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» riderid|string|true|none||none|
|»» name|string|true|none||none|
|»» address|string|true|none||none|
|»» phone_number|string|true|none||none|
|»» phone_code|string|true|none||none|
|»» email|string|true|none||none|
|»» vehicle_plate_number|string|true|none||none|
|»» photo|string|true|none||none|
|»» total_completed_delivery|integer|true|none||none|
|»» active|boolean|true|none||none|
|»» created_at|string|true|none||none|

## GET get rider

GET /riders/get/rider_uuid

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "9dbb0847-a2ba-4cdb-b904-72fd9ab2f3bc",
    "riderid": "45689646",
    "name": "Kelly Chimaobi",
    "address": "Aso housing estate, lugbe",
    "phone_number": "08028492844",
    "phone_code": "234",
    "email": "king@gmail.com",
    "vehicle_plate_number": "Ae93480G",
    "photo": "https://usedora-bucket-dev.s3.amazonaws.com/photos/CvvdCXduNkboQLuaMOm00FnAFmIZH7EoU5bjWstL.jpg",
    "total_completed_delivery": 0,
    "active": true,
    "number_of_ongoing_deliveries": 6,
    "ongoing_deliveries": [
      {
        "uuid": "ed05dfc1-a055-46b2-b2e6-679005749ef7",
        "order_number": "190482668017",
        "fleet_id": null,
        "status": "Awaiting Pickup",
        "delivery_type": "intra_state",
        "sender_longitude": "7.3445666",
        "sender_latitude": "8.95625",
        "customer_longitude": "7.4974495",
        "customer_latitude": "9.0339358",
        "delivery_fee": "NGN3,000.00",
        "created_at": "2023-12-04T22:04:44.000000Z",
        "customer_detail": {
          "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
          "customer_name": "TundeNasri",
          "customer_email": null,
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2023-12-04T22:03:06.000000Z"
        },
        "sender_detail": {
          "uuid": "aeb0e264-73bf-4a92-b089-6aa01f1d87f3",
          "sender_name": "Ac Nice",
          "sender_phone": "08087168391",
          "sender_email": null,
          "sender_phonecode": "234",
          "sender_address": "Aso housing estate, lugbe",
          "created_at": "2023-12-04T22:04:44.000000Z",
          "updated_at": "2023-12-04T22:04:44.000000Z"
        },
        "items": [],
        "organization_detail": {
          "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
          "fleet_identity_number": null,
          "business_address": null,
          "phone_number": "8081939285",
          "phone_code": "234",
          "logo": null,
          "created_at": "2023-11-30T16:57:27.000000Z",
          "updated_at": "2023-11-30T16:57:27.000000Z"
        }
      },
      {
        "uuid": "1f42c4f9-5b57-42b8-96b7-77b07d282d85",
        "order_number": "952080652375",
        "fleet_id": null,
        "status": "Awaiting Pickup",
        "delivery_type": "intra_state",
        "sender_longitude": "7.3445666",
        "sender_latitude": "8.95625",
        "customer_longitude": "7.4974495",
        "customer_latitude": "9.0339358",
        "delivery_fee": "NGN3,000.00",
        "created_at": "2023-12-04T22:27:13.000000Z",
        "customer_detail": {
          "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
          "customer_name": "TundeNasri",
          "customer_email": null,
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2023-12-04T22:03:06.000000Z"
        },
        "sender_detail": {
          "uuid": "cce0d5df-c1cb-4fed-b1a7-29677b585a5d",
          "sender_name": "Ac Nice",
          "sender_phone": "08087168391",
          "sender_email": null,
          "sender_phonecode": "234",
          "sender_address": "Aso housing estate, lugbe",
          "created_at": "2023-12-04T22:27:13.000000Z",
          "updated_at": "2023-12-04T22:27:13.000000Z"
        },
        "items": [],
        "organization_detail": {
          "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
          "fleet_identity_number": null,
          "business_address": null,
          "phone_number": "8081939285",
          "phone_code": "234",
          "logo": null,
          "created_at": "2023-11-30T16:57:27.000000Z",
          "updated_at": "2023-11-30T16:57:27.000000Z"
        }
      },
      {
        "uuid": "0b4f765e-4ef1-4649-86fd-65c6c4d5f882",
        "order_number": "337850592853",
        "fleet_id": null,
        "status": "Awaiting Pickup",
        "delivery_type": "intra_state",
        "sender_longitude": "7.3445666",
        "sender_latitude": "8.95625",
        "customer_longitude": "7.4974495",
        "customer_latitude": "9.0339358",
        "delivery_fee": "NGN3,000.00",
        "created_at": "2023-12-05T00:50:10.000000Z",
        "customer_detail": {
          "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
          "customer_name": "TundeNasri",
          "customer_email": null,
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2023-12-04T22:03:06.000000Z"
        },
        "sender_detail": {
          "uuid": "aecc7eb3-f0ca-40aa-9b9a-5ec4f520c1ef",
          "sender_name": "Ac Nice",
          "sender_phone": "08087168391",
          "sender_email": null,
          "sender_phonecode": "234",
          "sender_address": "Aso housing estate, lugbe",
          "created_at": "2023-12-05T00:50:10.000000Z",
          "updated_at": "2023-12-05T00:50:10.000000Z"
        },
        "items": [
          {
            "uuid": "05b19768-6711-4468-9412-48648101f557",
            "item_description": "Freshfish",
            "item_quantity": 1,
            "item_value": "10000.00",
            "created_at": "2023-12-05T00:50:10.000000Z"
          }
        ],
        "organization_detail": {
          "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
          "fleet_identity_number": null,
          "business_address": null,
          "phone_number": "8081939285",
          "phone_code": "234",
          "logo": null,
          "created_at": "2023-11-30T16:57:27.000000Z",
          "updated_at": "2023-11-30T16:57:27.000000Z"
        }
      },
      {
        "uuid": "e207ecc7-dcab-439e-88e8-f3e630e53697",
        "order_number": "387451602924",
        "fleet_id": null,
        "status": "Awaiting Pickup",
        "delivery_type": "intra_state",
        "sender_longitude": "7.3445666",
        "sender_latitude": "8.95625",
        "customer_longitude": "7.4974495",
        "customer_latitude": "9.0339358",
        "delivery_fee": "NGN3,000.00",
        "created_at": "2023-12-05T00:51:00.000000Z",
        "customer_detail": {
          "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
          "customer_name": "TundeNasri",
          "customer_email": null,
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2023-12-04T22:03:06.000000Z"
        },
        "sender_detail": {
          "uuid": "cadb63c6-577b-4b30-ac6a-c4ca30884631",
          "sender_name": "Nuel Geek",
          "sender_phone": "08087168391",
          "sender_email": null,
          "sender_phonecode": "234",
          "sender_address": "Aso housing estate, lugbe",
          "created_at": "2023-12-05T00:51:00.000000Z",
          "updated_at": "2023-12-05T00:51:00.000000Z"
        },
        "items": [
          {
            "uuid": "68222706-82e4-4a30-a298-c64bd6240f99",
            "item_description": "Freshfish",
            "item_quantity": 1,
            "item_value": "10000.00",
            "created_at": "2023-12-05T00:51:00.000000Z"
          }
        ],
        "organization_detail": {
          "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
          "fleet_identity_number": null,
          "business_address": null,
          "phone_number": "8081939285",
          "phone_code": "234",
          "logo": null,
          "created_at": "2023-11-30T16:57:27.000000Z",
          "updated_at": "2023-11-30T16:57:27.000000Z"
        }
      },
      {
        "uuid": "65238f36-88db-477a-a9bc-738867ca2bab",
        "order_number": "784051429645",
        "fleet_id": null,
        "status": "Awaiting Pickup",
        "delivery_type": "intra_state",
        "sender_longitude": "7.3445666",
        "sender_latitude": "8.95625",
        "customer_longitude": "7.4974495",
        "customer_latitude": "9.0339358",
        "delivery_fee": "NGN3,000.00",
        "created_at": "2023-12-05T01:01:18.000000Z",
        "customer_detail": {
          "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
          "customer_name": "TundeNasri",
          "customer_email": null,
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2023-12-04T22:03:06.000000Z"
        },
        "sender_detail": {
          "uuid": "536c2419-3041-4392-aa0f-d80eeddae637",
          "sender_name": "Nuel Geek",
          "sender_phone": "08087168391",
          "sender_email": null,
          "sender_phonecode": "234",
          "sender_address": "Aso housing estate, lugbe",
          "created_at": "2023-12-05T01:01:18.000000Z",
          "updated_at": "2023-12-05T01:01:18.000000Z"
        },
        "items": [
          {
            "uuid": "12d3f0e3-60a9-4455-9fbc-dbb2af959382",
            "item_description": "Freshfish",
            "item_quantity": 1,
            "item_value": "10000.00",
            "created_at": "2023-12-05T01:01:18.000000Z"
          }
        ],
        "organization_detail": {
          "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
          "fleet_identity_number": null,
          "business_address": null,
          "phone_number": "8081939285",
          "phone_code": "234",
          "logo": null,
          "created_at": "2023-11-30T16:57:27.000000Z",
          "updated_at": "2023-11-30T16:57:27.000000Z"
        }
      },
      {
        "uuid": "b0febc7b-91a0-43d2-a933-fc1c27dd25c3",
        "order_number": "531886487269",
        "fleet_id": null,
        "status": "In Transit",
        "delivery_type": "state_to_state",
        "sender_longitude": "3.3096414",
        "sender_latitude": "6.5352628",
        "customer_longitude": "7.4974495",
        "customer_latitude": "9.0339358",
        "delivery_fee": "NGN3,000.00",
        "created_at": "2023-12-05T01:02:02.000000Z",
        "customer_detail": {
          "uuid": "caf911a3-7b66-4599-9b3a-aa26d7730e69",
          "customer_name": "TundeNasri",
          "customer_email": null,
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2023-12-04T22:03:06.000000Z"
        },
        "sender_detail": {
          "uuid": "2743f3a5-b692-4c10-99f7-b3b941f0c3eb",
          "sender_name": "Nuel Geek",
          "sender_phone": "08087168391",
          "sender_email": null,
          "sender_phonecode": "234",
          "sender_address": "2 Umuleri street, Lagos",
          "created_at": "2023-12-05T01:02:02.000000Z",
          "updated_at": "2023-12-06T00:45:41.000000Z"
        },
        "items": [
          {
            "uuid": "cbf13cbb-b817-42ce-b948-12344ff7507f",
            "item_description": "Freshfish",
            "item_quantity": 1,
            "item_value": "10000.00",
            "created_at": "2023-12-06T00:45:41.000000Z"
          },
          {
            "uuid": "7cf6577f-c6e1-40fa-aa98-443ca27cdc3f",
            "item_description": "Freshfish",
            "item_quantity": 1,
            "item_value": "10000.00",
            "created_at": "2023-12-06T01:00:27.000000Z"
          },
          {
            "uuid": "a758c1cb-011a-4f96-9f5e-249bff763e07",
            "item_description": "Canno Camera",
            "item_quantity": 1,
            "item_value": "30000.00",
            "created_at": "2023-12-06T01:00:54.000000Z"
          },
          {
            "uuid": "a67c925e-c9bd-4829-ac2b-c429437f50e1",
            "item_description": "Eva soap pack",
            "item_quantity": 1,
            "item_value": "4000.00",
            "created_at": "2023-12-05T01:02:02.000000Z"
          }
        ],
        "organization_detail": {
          "uuid": "9a7519bc-a726-4bff-a9aa-e77d627e2688",
          "fleet_identity_number": null,
          "business_address": null,
          "phone_number": "8081939285",
          "phone_code": "234",
          "logo": null,
          "created_at": "2023-11-30T16:57:27.000000Z",
          "updated_at": "2023-11-30T16:57:27.000000Z"
        }
      }
    ],
    "created_at": "2023-12-03T07:47:46.000000Z"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» riderid|string|true|none||none|
|»» name|string|true|none||none|
|»» address|string|true|none||none|
|»» phone_number|string|true|none||none|
|»» phone_code|string|true|none||none|
|»» email|string|true|none||none|
|»» vehicle_plate_number|string|true|none||none|
|»» photo|string|true|none||none|
|»» total_completed_delivery|integer|true|none||none|
|»» active|boolean|true|none||none|
|»» number_of_ongoing_deliveries|integer|true|none||none|
|»» ongoing_deliveries|[object]|true|none||none|
|»»» uuid|string|true|none||none|
|»»» order_number|string|true|none||none|
|»»» fleet_id|null|true|none||none|
|»»» status|string|true|none||none|
|»»» delivery_type|string|true|none||none|
|»»» sender_longitude|string|true|none||none|
|»»» sender_latitude|string|true|none||none|
|»»» customer_longitude|string|true|none||none|
|»»» customer_latitude|string|true|none||none|
|»»» delivery_fee|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» customer_detail|object|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» customer_name|string|true|none||none|
|»»»» customer_email|null|true|none||none|
|»»»» customer_phone_number|string|true|none||none|
|»»»» customer_phone_code|string|true|none||none|
|»»»» customer_address|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»»» sender_detail|object|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» sender_name|string|true|none||none|
|»»»» sender_phone|string|true|none||none|
|»»»» sender_email|null|true|none||none|
|»»»» sender_phonecode|string|true|none||none|
|»»»» sender_address|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»»»» updated_at|string|true|none||none|
|»»» items|[object]|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» item_description|string|true|none||none|
|»»»» item_quantity|integer|true|none||none|
|»»»» item_value|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»»» organization_detail|object|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» fleet_identity_number|null|true|none||none|
|»»»» business_address|null|true|none||none|
|»»»» phone_number|string|true|none||none|
|»»»» phone_code|string|true|none||none|
|»»»» logo|null|true|none||none|
|»»»» created_at|string|true|none||none|
|»»»» updated_at|string|true|none||none|
|»» created_at|string|true|none||none|

## POST update rider

POST /riders/update/rider_uuid

> Body Parameters

```yaml
rider_name: Nice Chimaobi
rider_address: Aso housing estate, lugbe
rider_email: king@gmail.com
rider_phone: "08028492844"
rider_phonecode: "234"
vehicle_plate_number: Ae93480G
rider_photo: string

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» rider_name|body|string| yes |none|
|» rider_address|body|string| yes |none|
|» rider_email|body|string| yes |none|
|» rider_phone|body|string| yes |none|
|» rider_phonecode|body|string| yes |none|
|» vehicle_plate_number|body|string| yes |none|
|» rider_photo|body|string(binary)| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "uuid": "9dbb0847-a2ba-4cdb-b904-72fd9ab2f3bc",
    "riderid": "45689646",
    "name": "Kelly Chimaobi",
    "address": "Aso housing estate, lugbe",
    "phone_number": "08028492844",
    "phone_code": "234",
    "email": "king@gmail.com",
    "vehicle_plate_number": "Ae93480G",
    "photo": "https://usedora-bucket-dev.s3.amazonaws.com/photos/CvvdCXduNkboQLuaMOm00FnAFmIZH7EoU5bjWstL.jpg",
    "total_completed_delivery": 0,
    "active": true,
    "created_at": "2023-12-03T07:47:46.000000Z"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» uuid|string|true|none||none|
|»» riderid|string|true|none||none|
|»» name|string|true|none||none|
|»» address|string|true|none||none|
|»» phone_number|string|true|none||none|
|»» phone_code|string|true|none||none|
|»» email|string|true|none||none|
|»» vehicle_plate_number|string|true|none||none|
|»» photo|string|true|none||none|
|»» total_completed_delivery|integer|true|none||none|
|»» active|boolean|true|none||none|
|»» created_at|string|true|none||none|

## POST deactivate riders

POST /riders/deactivate

> Body Parameters

```yaml
"rider_uuids[]": "{{rider_uuid}}"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» rider_uuids[]|body|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Riders deactivated successfully"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## GET rider delivery history

GET /riders/delivery_history/rider_uuid

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|paginate|query|string| yes |none|
|per_page|query|string| yes |none|
|filter|query|string| yes |all|today|yesterday|
|start_date|query|string| yes |optional|
|end_date|query|string| yes |optional|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": {
    "current_page": 1,
    "data": [
      {
        "uuid": "4560f59a-d071-4854-a098-2978ba373004",
        "order_number": "14192541",
        "fleet_identity_number": "68316349",
        "status": "Awaiting-Pickup",
        "delivery_type": "intra_state",
        "sender_longitude": null,
        "sender_latitude": null,
        "customer_longitude": null,
        "customer_latitude": null,
        "delivery_fee": "3000",
        "currency": "NGN",
        "note": null,
        "creation_mode": "Manual",
        "created_at": "2024-01-06T17:02:09.000000Z",
        "customer_detail": {
          "uuid": "21803e28-08b7-4b23-b3f6-49161f8a6a4c",
          "customer_name": "TundeNasri",
          "customer_email": "sinoma@gmail.com",
          "customer_phone_number": "08065302534",
          "customer_phone_code": "234",
          "customer_address": "12 Ahmadu Bello way, Central Business District, Abuja",
          "created_at": "2024-01-06T07:28:13.000000Z"
        },
        "sender_detail": {
          "uuid": "62c70575-366c-44c3-893e-504abce1f667",
          "sender_name": "Nuel Geek",
          "sender_phone": "08087168391",
          "sender_email": "sender@example.com",
          "sender_phonecode": "234",
          "sender_address": "2 Umuleri street, Lagos",
          "created_at": "2024-01-06T17:02:09.000000Z",
          "updated_at": "2024-01-06T17:03:26.000000Z"
        },
        "items": [
          {
            "uuid": "99594223-8c39-49be-aefb-a1704e2e2650",
            "item_description": "Packaged makeup for mama emma's birthday celebration",
            "item_quantity": 2,
            "item_value": "43500.00",
            "currency": "NGN",
            "created_at": "2024-01-06T17:02:09.000000Z"
          },
          {
            "uuid": "801f2638-4a26-444d-9409-c5f54667e449",
            "item_description": "Eva soap pack",
            "item_quantity": 1,
            "item_value": "4000.00",
            "currency": "NGN",
            "created_at": "2024-01-06T17:03:26.000000Z"
          },
          {
            "uuid": "68751dcf-4440-4b51-9dbc-9e161b21ce2b",
            "item_description": "Cannon Camera",
            "item_quantity": 1,
            "item_value": "30000.00",
            "currency": "NGN",
            "created_at": "2024-01-06T17:03:26.000000Z"
          }
        ],
        "rider_info": {
          "uuid": "69234d24-61c1-4d68-a232-7a04d71f2b0e",
          "riderid": "71762164",
          "name": "Kelly Chimaobi",
          "address": "Aso housing estate, lugbe",
          "phone_number": "07081131771",
          "phone_code": "234",
          "email": "kyl@gmail.com",
          "vehicle_plate_number": "Ae93480G",
          "photo": "https://usedora-bucket-dev.s3.amazonaws.com/photos/S97Eie0RU6bdafmq5OjV9HeZkuCYdL0UNaT4SP52.jpg",
          "total_completed_delivery": 0,
          "active": false,
          "number_of_ongoing_deliveries": 0,
          "total_revenue_by_rider": "0",
          "rider_ongoing_deliveries": null,
          "created_at": "2024-01-06T08:02:20.000000Z"
        }
      }
    ],
    "first_page_url": "http://127.0.0.1:8000/api/riders/delivery_history/69234d24-61c1-4d68-a232-7a04d71f2b0e?page=1",
    "from": 1,
    "last_page": 1,
    "last_page_url": "http://127.0.0.1:8000/api/riders/delivery_history/69234d24-61c1-4d68-a232-7a04d71f2b0e?page=1",
    "links": [
      {
        "url": null,
        "label": "&laquo; Previous",
        "active": false
      },
      {
        "url": "http://127.0.0.1:8000/api/riders/delivery_history/69234d24-61c1-4d68-a232-7a04d71f2b0e?page=1",
        "label": "1",
        "active": true
      },
      {
        "url": null,
        "label": "Next &raquo;",
        "active": false
      }
    ],
    "next_page_url": null,
    "path": "http://127.0.0.1:8000/api/riders/delivery_history/69234d24-61c1-4d68-a232-7a04d71f2b0e",
    "per_page": 5,
    "prev_page_url": null,
    "to": 1,
    "total": 1
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|object|true|none||none|
|»» current_page|integer|true|none||none|
|»» data|[object]|true|none||none|
|»»» uuid|string|false|none||none|
|»»» order_number|string|false|none||none|
|»»» fleet_identity_number|string|false|none||none|
|»»» status|string|false|none||none|
|»»» delivery_type|string|false|none||none|
|»»» sender_longitude|null|false|none||none|
|»»» sender_latitude|null|false|none||none|
|»»» customer_longitude|null|false|none||none|
|»»» customer_latitude|null|false|none||none|
|»»» delivery_fee|string|false|none||none|
|»»» currency|string|false|none||none|
|»»» note|null|false|none||none|
|»»» creation_mode|string|false|none||none|
|»»» created_at|string|false|none||none|
|»»» customer_detail|object|false|none||none|
|»»»» uuid|string|true|none||none|
|»»»» customer_name|string|true|none||none|
|»»»» customer_email|string|true|none||none|
|»»»» customer_phone_number|string|true|none||none|
|»»»» customer_phone_code|string|true|none||none|
|»»»» customer_address|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»»» sender_detail|object|false|none||none|
|»»»» uuid|string|true|none||none|
|»»»» sender_name|string|true|none||none|
|»»»» sender_phone|string|true|none||none|
|»»»» sender_email|string|true|none||none|
|»»»» sender_phonecode|string|true|none||none|
|»»»» sender_address|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»»»» updated_at|string|true|none||none|
|»»» items|[object]|false|none||none|
|»»»» uuid|string|true|none||none|
|»»»» item_description|string|true|none||none|
|»»»» item_quantity|integer|true|none||none|
|»»»» item_value|string|true|none||none|
|»»»» currency|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»»» rider_info|object|false|none||none|
|»»»» uuid|string|true|none||none|
|»»»» riderid|string|true|none||none|
|»»»» name|string|true|none||none|
|»»»» address|string|true|none||none|
|»»»» phone_number|string|true|none||none|
|»»»» phone_code|string|true|none||none|
|»»»» email|string|true|none||none|
|»»»» vehicle_plate_number|string|true|none||none|
|»»»» photo|string|true|none||none|
|»»»» total_completed_delivery|integer|true|none||none|
|»»»» active|boolean|true|none||none|
|»»»» number_of_ongoing_deliveries|integer|true|none||none|
|»»»» total_revenue_by_rider|string|true|none||none|
|»»»» rider_ongoing_deliveries|null|true|none||none|
|»»»» created_at|string|true|none||none|
|»» first_page_url|string|true|none||none|
|»» from|integer|true|none||none|
|»» last_page|integer|true|none||none|
|»» last_page_url|string|true|none||none|
|»» links|[object]|true|none||none|
|»»» url|string¦null|true|none||none|
|»»» label|string|true|none||none|
|»»» active|boolean|true|none||none|
|»» next_page_url|null|true|none||none|
|»» path|string|true|none||none|
|»» per_page|integer|true|none||none|
|»» prev_page_url|null|true|none||none|
|»» to|integer|true|none||none|
|»» total|integer|true|none||none|

## POST update delivery pickup

POST /delivery/pickup

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|order_number|query|string| yes |none|
|pickup_otp|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST update delivery dropoff

POST /delivery/dropoff

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|order_number|query|string| yes |none|
|dropoff_otp|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## DELETE Delete Rider

DELETE /riders/delete-rider

> Body Parameters

```json
{
  "rider_uuids": [
    "1550c152-2523-4f3d-931e-92ce8a4c80cc",
    "2550c152-2523-4f3d-931e-92ce8a4c80cc",
    "3550c152-2523-4f3d-931e-92ce8a4c80cc",
    "4550c152-2523-4f3d-931e-92ce8a4c80cc"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» rider_uuids|body|[string]| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Rider delete successfully."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## DELETE Cancel Pending invites

DELETE /riders/cancel-rider-invite/0d861d21-95a3-4d07-b7bb-988ef4118087

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "message": "Riders invite cancelled successfully."
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» message|string|true|none||none|

## GET Rider Ongoing Deliveries

GET /riders/ongoing-deliveries/{uuid}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|uuid|path|string| yes |none|

> Response Examples

> 200 Response

```json
{
  "status": "success",
  "data": [
    {
      "uuid": "5792237c-0e66-453e-aef2-2c6997bdd2fd",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "88714156",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Rider Declined",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "2432",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2024-07-13T23:00:00.000000Z",
      "pickup_at": null,
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "5b892e7a-bb26-4c83-a86d-5ccfe27f9d58",
          "delivery_uuid": "5792237c-0e66-453e-aef2-2c6997bdd2fd",
          "status": "Awaiting-Pickup",
          "dropoff_photo": null,
          "customer_name": "Sdfdsf1",
          "customer_email": null,
          "customer_phone_number": "12435456677",
          "customer_phone_code": "234",
          "customer_address": "sdfsdfsdfsd",
          "created_at": "2024-07-14T15:13:27.000000Z",
          "items": [
            {
              "uuid": "48e9a284-20de-4232-8370-657752844f84",
              "item_description": "sdfs",
              "item_quantity": 243,
              "item_value": "3242.00",
              "currency": "NGN",
              "created_at": "2024-07-14T15:13:27.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "af3c8ff5-b667-4f16-99ee-fdfbf393df5a",
        "sender_name": "Dsf",
        "sender_phone": "1234456789",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "zxfsdsdf",
        "business_owned": false,
        "created_at": "2024-07-14T15:13:27.000000Z",
        "updated_at": "2024-07-14T15:13:27.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "3fc90259-1eeb-406b-8096-74ed0fd3f371",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "Awaiting Pickup",
        "is_grouped": false,
        "picked_up_at": null,
        "dropped_off_at": null,
        "cancelled_reason": "I will not work with this business",
        "created_at": "2024-07-24T16:16:05.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "87b30a45-04c2-4cb9-87c4-7ab5ca61e1c9",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "59876221",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": "8.539144",
      "sender_latitude": "7.7321516",
      "customer_longitude": "8.539144",
      "customer_latitude": "7.7321516",
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-19T11:41:04.000000Z",
      "pickup_at": "2025-01-07T15:25:36.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "86a6ddf0-1a9a-43f6-b778-ffe2ea53935d",
          "delivery_uuid": "87b30a45-04c2-4cb9-87c4-7ab5ca61e1c9",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "7062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2024-07-19T11:41:04.000000Z",
          "items": []
        }
      ],
      "sender_detail": {
        "uuid": "1052ea9c-5ab9-433e-af8a-fb0838110be1",
        "sender_name": "Enki Business Ltd",
        "sender_phone": "7062423707",
        "sender_email": "angwamoses@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": false,
        "created_at": "2024-07-19T11:41:04.000000Z",
        "updated_at": "2024-07-19T11:41:04.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "f1b2acfa-bdac-47d4-9340-64d5b235d8ce",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-07 15:25:35",
        "dropped_off_at": null,
        "cancelled_reason": "Order came in late",
        "created_at": "2024-08-23T11:31:01.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "232f3af2-dfa2-48d4-b9e4-f4683eecbc83",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "58474523",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-19T12:53:57.000000Z",
      "pickup_at": "2025-01-07T15:56:07.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "f915035e-1b6a-469f-bde6-6d3e3cf6e132",
          "delivery_uuid": "232f3af2-dfa2-48d4-b9e4-f4683eecbc83",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "7062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2024-07-19T12:53:57.000000Z",
          "items": []
        }
      ],
      "sender_detail": {
        "uuid": "dad24ea0-9cd5-4682-bafd-e076425631a2",
        "sender_name": "Enki Business",
        "sender_phone": "7062423707",
        "sender_email": "angwamoses@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": false,
        "created_at": "2024-07-19T12:53:57.000000Z",
        "updated_at": "2024-07-19T12:53:57.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "ce0ac75e-56d8-48ee-9281-5c30c3a0beb6",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-07 15:56:07",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2024-08-20T14:45:07.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "7e3f6949-45b4-4150-8c8b-39aec9424331",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "60171320",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Pending",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-19T13:19:53.000000Z",
      "pickup_at": null,
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "b7276f2f-c0f2-4025-81cf-71b73d045479",
          "delivery_uuid": "7e3f6949-45b4-4150-8c8b-39aec9424331",
          "status": "Awaiting-Pickup",
          "dropoff_photo": null,
          "customer_name": "Ogbole Angwa",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "7062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2024-07-19T13:19:53.000000Z",
          "items": [
            {
              "uuid": "e9804a15-56e8-45ac-82a3-ebb72f85ae67",
              "item_description": "Yam tubers",
              "item_quantity": 20,
              "item_value": "30000.00",
              "currency": "NGN",
              "created_at": "2024-07-19T13:19:53.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "9cf8dd15-4b12-4eed-98b3-5538dac51b56",
        "sender_name": "Enki Business",
        "sender_phone": "7062423707",
        "sender_email": "angwamoses@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "Flat 4, Msg Qtrs",
        "business_owned": false,
        "created_at": "2024-07-19T13:19:53.000000Z",
        "updated_at": "2024-07-19T13:19:53.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "f79923c3-2a87-45a2-8411-b600f9e3ff09",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "Awaiting Pickup",
        "is_grouped": false,
        "picked_up_at": null,
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2024-08-16T11:09:45.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "41ca03b0-f392-442d-af33-8f98df3f1454",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "68209472",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-24T16:33:08.000000Z",
      "pickup_at": "2025-01-07T16:06:14.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "26e0e8d2-76f3-426a-8ddc-c26a9d0098bc",
          "delivery_uuid": "41ca03b0-f392-442d-af33-8f98df3f1454",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Chimaobi Nice",
          "customer_email": null,
          "customer_phone_number": "8087876754",
          "customer_phone_code": "234",
          "customer_address": "Mararaba, Nassarawa state",
          "created_at": "2024-07-24T16:33:08.000000Z",
          "items": [
            {
              "uuid": "e030b163-706e-4378-8d55-8725d3a288ce",
              "item_description": "New Item",
              "item_quantity": null,
              "item_value": null,
              "currency": "NGN",
              "created_at": "2024-07-24T16:33:08.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "2ed3b00b-a4d7-44f5-83bd-9083978ba8d3",
        "sender_name": "",
        "sender_phone": "8083776411",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Grandeur squares and cubes estate, lugbe Abuja",
        "business_owned": false,
        "created_at": "2024-07-24T16:33:08.000000Z",
        "updated_at": "2024-07-24T16:33:08.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "655af250-abb8-4715-ab93-6ea848fa884f",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-07 16:06:13",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2024-08-16T11:09:46.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "666d0bb1-7c1a-4571-8924-410268551cb1",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "29639449",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": "7.3445666",
      "sender_latitude": "8.95625",
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-25T23:28:55.000000Z",
      "pickup_at": "2025-01-07T16:05:11.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "69274978-1512-4e83-9701-a6d37dbe5644",
          "delivery_uuid": "666d0bb1-7c1a-4571-8924-410268551cb1",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Anosike Nice",
          "customer_email": null,
          "customer_phone_number": "8076686788",
          "customer_phone_code": "234",
          "customer_address": "Grandeur squares and cubes estate",
          "created_at": "2024-07-25T23:28:55.000000Z",
          "items": [
            {
              "uuid": "a9607672-033a-4f3c-a08f-bef244503e4d",
              "item_description": "Fuel and gas cylinder",
              "item_quantity": 1,
              "item_value": "80000.00",
              "currency": "NGN",
              "created_at": "2024-07-25T23:28:55.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "3c7575ea-aeb6-4b6e-8707-0893d89b0160",
        "sender_name": "",
        "sender_phone": "8097877876",
        "sender_email": "chimaobinice@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "Aso housing estate, lugbe abuja",
        "business_owned": false,
        "created_at": "2024-07-25T23:28:55.000000Z",
        "updated_at": "2024-07-25T23:28:55.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "bdbf0f3a-67ce-4856-bd70-125042707e8a",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-07 16:05:11",
        "dropped_off_at": null,
        "cancelled_reason": "Delivery cancelled by the business.",
        "created_at": "2024-08-16T11:09:47.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "54014ad8-d81e-4438-a9f4-0b188b674a22",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "65399180",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2024-07-13T23:00:00.000000Z",
      "pickup_at": "2024-12-28T20:20:47.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "fdffaaee-ef5c-4cd3-a1ea-3c30b5231112",
          "delivery_uuid": "54014ad8-d81e-4438-a9f4-0b188b674a22",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Dsfdgfd",
          "customer_email": null,
          "customer_phone_number": "09976745435",
          "customer_phone_code": "234",
          "customer_address": "dsfdsfds",
          "created_at": "2024-07-14T13:09:01.000000Z",
          "items": [
            {
              "uuid": "cbdeffd6-d595-40ec-9eaa-a56ebac6f11d",
              "item_description": "fgddf",
              "item_quantity": 34,
              "item_value": "453.00",
              "currency": "NGN",
              "created_at": "2024-07-14T13:09:01.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "7dd6ba5e-3543-4682-9e5a-6b9dec3021b5",
        "sender_name": "D@g.com",
        "sender_phone": "8064733458",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "fdgdfgd",
        "business_owned": false,
        "created_at": "2024-07-14T13:09:01.000000Z",
        "updated_at": "2024-07-14T13:09:01.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "5df552b7-81b0-4454-a025-895df2edd3c8",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2024-12-28 20:20:47",
        "dropped_off_at": null,
        "cancelled_reason": "I'm not interested in taking this orders",
        "created_at": "2024-08-23T12:20:54.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "8b700d1d-17ef-45a1-b902-4779e30e1d59",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "61350194",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-18T18:24:58.000000Z",
      "pickup_at": "2025-01-01T09:29:14.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "f7c5096c-d1cb-4d33-b5ce-b2950213e001",
          "delivery_uuid": "8b700d1d-17ef-45a1-b902-4779e30e1d59",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Gospel Ezenwa",
          "customer_email": "chimaobinice@gmail.com",
          "customer_phone_number": "9099898362",
          "customer_phone_code": "234",
          "customer_address": "Mararaba, Nassarawa state",
          "created_at": "2024-07-18T18:24:58.000000Z",
          "items": []
        }
      ],
      "sender_detail": {
        "uuid": "a1c56d19-f3a3-4159-ad58-76ea9dbb937d",
        "sender_name": "Kingsley Nzubechi",
        "sender_phone": "8089878372",
        "sender_email": "abasszz786@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "Aso Housing estate Lugbe, Abuja",
        "business_owned": false,
        "created_at": "2024-07-18T18:24:58.000000Z",
        "updated_at": "2024-07-18T18:24:58.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "6ee2c998-736a-4968-a86c-98db1591b92a",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-01 09:29:14",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2024-08-23T11:56:58.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "f96ab216-b3c6-41d1-826e-17103c7da827",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "37664826",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-19T12:12:56.000000Z",
      "pickup_at": "2025-01-04T00:50:50.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "ee8f2187-1dda-4139-a142-c615366a230d",
          "delivery_uuid": "f96ab216-b3c6-41d1-826e-17103c7da827",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "7062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2024-07-19T12:12:56.000000Z",
          "items": []
        }
      ],
      "sender_detail": {
        "uuid": "f070113a-2123-4e1f-a5b5-14762aed97bf",
        "sender_name": "Enki Business",
        "sender_phone": "7062423707",
        "sender_email": "angwamoses@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": false,
        "created_at": "2024-07-19T12:12:56.000000Z",
        "updated_at": "2024-07-19T12:12:56.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "3d34f7ab-dbb1-42a0-a959-a2622ea763f4",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-04 00:50:49",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2024-08-22T12:14:36.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "5d26f10e-b6fd-4945-8e26-518d5c65a68b",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "69675460",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "3175",
      "service_charge": "175",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Via Booking",
      "created_at": "2024-07-19T13:04:14.000000Z",
      "pickup_at": "2025-01-07T15:56:29.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "1d96fdff-2bc9-4a1c-9f2d-c5810be0215c",
          "delivery_uuid": "5d26f10e-b6fd-4945-8e26-518d5c65a68b",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "7062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2024-07-19T13:04:14.000000Z",
          "items": []
        }
      ],
      "sender_detail": {
        "uuid": "6d468fda-ba82-4799-8d57-318ddf334693",
        "sender_name": "Enki Business",
        "sender_phone": "7062423707",
        "sender_email": "angwamoses@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": false,
        "created_at": "2024-07-19T13:04:14.000000Z",
        "updated_at": "2024-07-19T13:04:14.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "75e58903-8ff4-48b0-a38c-3b9b98d94bbd",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-07 15:56:28",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2024-08-19T21:49:20.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "98433833-6ef4-4376-ae2b-a31423ede57e",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "NE8cm",
      "fleet_identity_number": "78218528",
      "status": "Pending",
      "status_label": "Pending",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "500",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-05T23:00:00.000000Z",
      "pickup_at": null,
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "52ffb324-dce2-4ca1-9f06-ae137cad1f01",
          "delivery_uuid": "98433833-6ef4-4376-ae2b-a31423ede57e",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "f737d0c9-4057-4c2f-bbfb-7ca157f21f40",
              "item_description": "Bags of Casava",
              "item_quantity": 3,
              "item_value": "15000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        },
        {
          "uuid": "c768c109-a8a7-4600-abca-c4a59c837b14",
          "delivery_uuid": "462dbaea-da54-4019-9ed0-c9f7cc40c75d",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Enki Business",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "afd3c895-f085-4a6b-a47b-d1f453e47212",
              "item_description": "Bags of groundnut",
              "item_quantity": 2,
              "item_value": "30000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        },
        {
          "uuid": "d8563a24-3ebe-430c-bfd3-42bb9b6dc247",
          "delivery_uuid": "1f53091b-1fc6-4ad7-824e-e431c390c5c0",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "54e47b4d-6eec-448a-8710-dfbb8b078a3f",
              "item_description": "Yams",
              "item_quantity": 3,
              "item_value": "6000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "f10d700f-6b3f-4342-8ccc-9c8eb646ff33",
        "sender_name": "Nuel Logistics",
        "sender_phone": "8083776411",
        "sender_email": "nuel@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": true,
        "created_at": "2024-04-10T23:26:19.000000Z",
        "updated_at": "2025-01-06T12:36:53.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "462dbaea-da54-4019-9ed0-c9f7cc40c75d",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "C4alp",
      "fleet_identity_number": "78218528",
      "status": "Pending",
      "status_label": "Pending",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "500",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-05T23:00:00.000000Z",
      "pickup_at": null,
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "52ffb324-dce2-4ca1-9f06-ae137cad1f01",
          "delivery_uuid": "98433833-6ef4-4376-ae2b-a31423ede57e",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "f737d0c9-4057-4c2f-bbfb-7ca157f21f40",
              "item_description": "Bags of Casava",
              "item_quantity": 3,
              "item_value": "15000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        },
        {
          "uuid": "c768c109-a8a7-4600-abca-c4a59c837b14",
          "delivery_uuid": "462dbaea-da54-4019-9ed0-c9f7cc40c75d",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Enki Business",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "afd3c895-f085-4a6b-a47b-d1f453e47212",
              "item_description": "Bags of groundnut",
              "item_quantity": 2,
              "item_value": "30000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        },
        {
          "uuid": "d8563a24-3ebe-430c-bfd3-42bb9b6dc247",
          "delivery_uuid": "1f53091b-1fc6-4ad7-824e-e431c390c5c0",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "54e47b4d-6eec-448a-8710-dfbb8b078a3f",
              "item_description": "Yams",
              "item_quantity": 3,
              "item_value": "6000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "f10d700f-6b3f-4342-8ccc-9c8eb646ff33",
        "sender_name": "Nuel Logistics",
        "sender_phone": "8083776411",
        "sender_email": "nuel@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": true,
        "created_at": "2024-04-10T23:26:19.000000Z",
        "updated_at": "2025-01-06T12:36:53.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "1f53091b-1fc6-4ad7-824e-e431c390c5c0",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "JVRaY",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": "8.539144",
      "sender_latitude": "7.7321516",
      "customer_longitude": "8.539144",
      "customer_latitude": "7.7321516",
      "delivery_fee": "500",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-05T23:00:00.000000Z",
      "pickup_at": "2025-01-08T00:51:08.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "52ffb324-dce2-4ca1-9f06-ae137cad1f01",
          "delivery_uuid": "98433833-6ef4-4376-ae2b-a31423ede57e",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "f737d0c9-4057-4c2f-bbfb-7ca157f21f40",
              "item_description": "Bags of Casava",
              "item_quantity": 3,
              "item_value": "15000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        },
        {
          "uuid": "c768c109-a8a7-4600-abca-c4a59c837b14",
          "delivery_uuid": "462dbaea-da54-4019-9ed0-c9f7cc40c75d",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Enki Business",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "afd3c895-f085-4a6b-a47b-d1f453e47212",
              "item_description": "Bags of groundnut",
              "item_quantity": 2,
              "item_value": "30000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        },
        {
          "uuid": "d8563a24-3ebe-430c-bfd3-42bb9b6dc247",
          "delivery_uuid": "1f53091b-1fc6-4ad7-824e-e431c390c5c0",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Angwa Moses",
          "customer_email": "angwamoses@gmail.com",
          "customer_phone_number": "07062423707",
          "customer_phone_code": "234",
          "customer_address": "MSG Teachers Qtrs, Makurdi",
          "created_at": "2025-01-06T12:36:53.000000Z",
          "items": [
            {
              "uuid": "54e47b4d-6eec-448a-8710-dfbb8b078a3f",
              "item_description": "Yams",
              "item_quantity": 3,
              "item_value": "6000.00",
              "currency": "NGN",
              "created_at": "2025-01-06T12:36:53.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "f10d700f-6b3f-4342-8ccc-9c8eb646ff33",
        "sender_name": "Nuel Logistics",
        "sender_phone": "8083776411",
        "sender_email": "nuel@gmail.com",
        "sender_phonecode": "234",
        "sender_address": "MSG Teachers Qtrs, Makurdi",
        "business_owned": true,
        "created_at": "2024-04-10T23:26:19.000000Z",
        "updated_at": "2025-01-06T12:36:53.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "18e195e8-9275-4741-88c1-1719546679b9",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "uLMsh",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Delivered",
      "sender_longitude": "8.675277",
      "sender_latitude": "9.081999",
      "customer_longitude": "8.675277",
      "customer_latitude": "9.081999",
      "delivery_fee": "1000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-07T23:00:00.000000Z",
      "pickup_at": "2025-01-08T15:31:12.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "f2b43ecd-29e9-469e-a710-2d8b0cee747a",
          "delivery_uuid": "18e195e8-9275-4741-88c1-1719546679b9",
          "status": "Awaiting-Pickup",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/Pxh7fRJca8qXH91bfM8MlHOWB7eyITtTatr5UDxq.jpg",
          "customer_name": "Sala",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-08T15:10:43.000000Z",
          "items": [
            {
              "uuid": "5b5fab39-18d7-4ead-a0df-57135bbdce63",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-08T15:10:43.000000Z"
            }
          ]
        },
        {
          "uuid": "d2b171a4-005c-4979-9a1d-c1aa4a437a90",
          "delivery_uuid": "a6627921-47da-4c72-9b1a-f38ffa60385b",
          "status": "Delivered",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/Ec2baTaOg1xQqofXuIHiZ0uI5AuqJNmC7OOuMaoI.jpg",
          "customer_name": "Sala 2",
          "customer_email": "abdullahijimoh3.ja@gmail.com",
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-08T15:10:43.000000Z",
          "items": [
            {
              "uuid": "118f4c3e-badf-4eea-bf4d-0174ea883864",
              "item_description": "book",
              "item_quantity": 2,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-08T15:10:43.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "f1a0ce84-d98e-4af9-9d21-77958774ce92",
        "sender_name": "Fela",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Nigeria",
        "business_owned": false,
        "created_at": "2025-01-08T15:10:43.000000Z",
        "updated_at": "2025-01-08T15:10:43.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "e4107c59-3682-42b0-ae5d-e1115d1b5cd2",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "Awaiting Pickup",
        "is_grouped": false,
        "picked_up_at": null,
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2025-01-08T17:50:08.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "64cd0fa0-a0bc-436c-a08d-ab9950791809",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "tWa4C",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Delivered",
      "sender_longitude": "8.675277",
      "sender_latitude": "9.081999",
      "customer_longitude": "8.675277",
      "customer_latitude": "9.081999",
      "delivery_fee": "2000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-06T23:00:00.000000Z",
      "pickup_at": "2025-01-07T22:10:35.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "389a2bec-5978-4fcc-a1cb-897a756ecd1d",
          "delivery_uuid": "9f674816-5ce0-4383-a063-d73ce8718aa8",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Den2",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T22:06:51.000000Z",
          "items": [
            {
              "uuid": "b9d03b66-ee29-4365-b388-1f25d57267f2",
              "item_description": "pend",
              "item_quantity": 1,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-07T22:06:51.000000Z"
            }
          ]
        },
        {
          "uuid": "cff60237-322e-40e2-881a-4c0ceefa6532",
          "delivery_uuid": "64cd0fa0-a0bc-436c-a08d-ab9950791809",
          "status": "Awaiting-Pickup",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/W7HswXiAWD18GIeyCv3D7P8OV5auGiHjWztJ7ewN.jpg",
          "customer_name": "Den1",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T22:06:51.000000Z",
          "items": [
            {
              "uuid": "6125bad4-0651-4587-ac1b-e7cbd28a1f95",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-07T22:06:51.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "5559a6e5-e75b-4d78-ac35-1a3a99291c75",
        "sender_name": "Kilo",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Nigeria",
        "business_owned": false,
        "created_at": "2025-01-07T22:06:51.000000Z",
        "updated_at": "2025-01-07T22:06:51.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "d47e1415-43a7-4ca5-aaa4-9399680b21c2",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "fTQ7H",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Delivered",
      "sender_longitude": "8.675277",
      "sender_latitude": "9.081999",
      "customer_longitude": "8.675277",
      "customer_latitude": "9.081999",
      "delivery_fee": "1000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-06T23:00:00.000000Z",
      "pickup_at": "2025-01-07T21:47:49.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "3beac173-8fff-4ad8-8da9-b47adc207506",
          "delivery_uuid": "fe64148d-4614-4770-85f1-29fc2c070d54",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Den2",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T21:45:06.000000Z",
          "items": [
            {
              "uuid": "0cb59ff4-5dc9-4618-a947-35367c5bca31",
              "item_description": "pen",
              "item_quantity": 1,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-07T21:45:06.000000Z"
            }
          ]
        },
        {
          "uuid": "6c17ddef-127f-4994-a211-c9d1e8b73fa5",
          "delivery_uuid": "d47e1415-43a7-4ca5-aaa4-9399680b21c2",
          "status": "Awaiting-Pickup",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/PzRukFgYFkTKy31izTcJiWU3b8JGpNVehfm7V7Dg.jpg",
          "customer_name": "Den 1",
          "customer_email": "abdullahijimoh3.ja@gmail.com",
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T21:45:06.000000Z",
          "items": [
            {
              "uuid": "e1643c39-fb1b-497c-b621-8e4006ffd06f",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-07T21:45:06.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "11e6ce3a-365b-46d2-acc6-ee2a6f247c0c",
        "sender_name": "Lala",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Nigeria",
        "business_owned": false,
        "created_at": "2025-01-07T21:45:06.000000Z",
        "updated_at": "2025-01-07T21:45:06.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "afae9182-7ecc-47ec-896c-ad7b0889913c",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "szIaN",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Delivered",
      "sender_longitude": "8.675277",
      "sender_latitude": "9.081999",
      "customer_longitude": "8.675277",
      "customer_latitude": "9.081999",
      "delivery_fee": "3000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-06T23:00:00.000000Z",
      "pickup_at": "2025-01-07T21:05:53.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "b3a54dc1-e138-47f1-bcf9-b394eaa6b962",
          "delivery_uuid": "f8414557-6b64-4e92-877f-56687bc2eefa",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Mana 1",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T21:03:46.000000Z",
          "items": [
            {
              "uuid": "2d00a233-ef66-4c13-a7be-ea29117c034e",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-07T21:03:47.000000Z"
            },
            {
              "uuid": "be2c377f-1634-4f66-b9ae-c5ec665fed1a",
              "item_description": "book",
              "item_quantity": 2,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-07T21:03:47.000000Z"
            }
          ]
        },
        {
          "uuid": "0a49fef6-97c7-4def-9de8-5c99dc5df318",
          "delivery_uuid": "afae9182-7ecc-47ec-896c-ad7b0889913c",
          "status": "Awaiting-Pickup",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/z1zXLUqUlQG8YwESALXitLfp9m38XT8E3rz0omhp.jpg",
          "customer_name": "Mana 2",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T21:03:47.000000Z",
          "items": [
            {
              "uuid": "c22f9885-6640-461f-b4d2-e97624a8ac42",
              "item_description": "pen",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-07T21:03:47.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "6f943afd-b51a-4d70-aefb-d5212c802db7",
        "sender_name": "Lala",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Nigeria",
        "business_owned": false,
        "created_at": "2025-01-07T21:03:46.000000Z",
        "updated_at": "2025-01-07T21:03:46.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "0e400d3c-bd07-4a2a-a68a-3561adb50eec",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "TjaW2",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Delivered",
      "sender_longitude": "8.675277",
      "sender_latitude": "9.081999",
      "customer_longitude": "8.675277",
      "customer_latitude": "9.081999",
      "delivery_fee": "2000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-06T23:00:00.000000Z",
      "pickup_at": "2025-01-07T20:58:58.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "677978c5-9624-4b9a-af13-328f1c848118",
          "delivery_uuid": "5bd4744a-0e38-4eae-9252-2e8dc6756dc8",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Dema 2",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T20:55:44.000000Z",
          "items": [
            {
              "uuid": "92d729da-78ba-4691-8585-75c21ed40b4e",
              "item_description": "book",
              "item_quantity": 2,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-07T20:55:44.000000Z"
            }
          ]
        },
        {
          "uuid": "f5ff1718-f35e-4e81-882c-dbcc9e103fbe",
          "delivery_uuid": "0e400d3c-bd07-4a2a-a68a-3561adb50eec",
          "status": "Awaiting-Pickup",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/xWuRmpH3IpZW0kj9ZoBwbPZdKCgW70WhFxdAUgjL.jpg",
          "customer_name": "Dema 1",
          "customer_email": "abdullahijimoh3.ja@gmail.com",
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T20:55:44.000000Z",
          "items": [
            {
              "uuid": "35ae7142-c62a-4ca0-acf8-80f2f1eac29d",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "100.00",
              "currency": "NGN",
              "created_at": "2025-01-07T20:55:44.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "d1dd8b9d-1f59-4cc8-bcc7-3bb13adac7ab",
        "sender_name": "Lala",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Nigeria",
        "business_owned": false,
        "created_at": "2025-01-07T20:55:44.000000Z",
        "updated_at": "2025-01-07T20:55:44.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "042b66b4-7342-43cc-91dd-5608422d6d68",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "t4cI9",
      "fleet_identity_number": "78218528",
      "status": "Awaiting-Pickup",
      "status_label": "Delivered",
      "sender_longitude": "8.675277",
      "sender_latitude": "9.081999",
      "customer_longitude": "8.675277",
      "customer_latitude": "9.081999",
      "delivery_fee": "3000",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-06T23:00:00.000000Z",
      "pickup_at": "2025-01-07T17:48:29.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "cefe9e7e-a9f5-4ed0-8582-256802a26732",
          "delivery_uuid": "c5a8d958-0193-4386-b67f-b72ba09ba0ca",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Deco 2",
          "customer_email": "abdullahijimoh3.ja@gmail.com",
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T17:21:15.000000Z",
          "items": [
            {
              "uuid": "a29cea82-e844-436f-84ab-46aa068fb5f8",
              "item_description": "Pen",
              "item_quantity": 1,
              "item_value": "500.00",
              "currency": "NGN",
              "created_at": "2025-01-07T17:21:15.000000Z"
            }
          ]
        },
        {
          "uuid": "e82e26c9-df66-4b1d-9065-20c2349fc67f",
          "delivery_uuid": "c66045fa-8234-47a0-bac5-8155d767c3b6",
          "status": "Pending",
          "dropoff_photo": null,
          "customer_name": "Deco 3",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T17:21:15.000000Z",
          "items": [
            {
              "uuid": "7cd4c9a5-5740-4512-ab4b-59f35289d7e0",
              "item_description": "Book",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-07T17:21:15.000000Z"
            }
          ]
        },
        {
          "uuid": "41d33f61-26bc-4f55-9e12-1a92d0598672",
          "delivery_uuid": "042b66b4-7342-43cc-91dd-5608422d6d68",
          "status": "Awaiting-Pickup",
          "dropoff_photo": "https://usedora-bucket-dev.s3.amazonaws.com/delivery_process/bMMR05zZF4TQiEt4svcQgAKc9VhWGAB5pT2jfytD.jpg",
          "customer_name": "Deco",
          "customer_email": "abdullahijimoh3.ja@gmail.com",
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "Nigeria",
          "created_at": "2025-01-07T17:21:14.000000Z",
          "items": [
            {
              "uuid": "abd537eb-20e7-4407-836f-868d2c78d52e",
              "item_description": "Book",
              "item_quantity": 1,
              "item_value": "500.00",
              "currency": "NGN",
              "created_at": "2025-01-07T17:21:14.000000Z"
            },
            {
              "uuid": "7e94fe93-7296-482a-9d58-dcf0a5d5ca28",
              "item_description": "Pen",
              "item_quantity": 1,
              "item_value": "300.00",
              "currency": "NGN",
              "created_at": "2025-01-07T17:21:14.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "44d82bf9-6c71-444d-b62f-df63ecb4e79e",
        "sender_name": "Lala",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "Nigeria",
        "business_owned": false,
        "created_at": "2025-01-07T17:21:14.000000Z",
        "updated_at": "2025-01-07T17:21:14.000000Z"
      },
      "delivery_info_from_rider": null,
      "is_paid": false
    },
    {
      "uuid": "370fff76-b259-4456-8de2-f1c6f179b74a",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "aSBGB",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": "3.2887349",
      "sender_latitude": "6.6338844",
      "customer_longitude": "3.2887349",
      "customer_latitude": "6.6338844",
      "delivery_fee": "1500",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-08T23:00:00.000000Z",
      "pickup_at": "2025-01-09T09:17:18.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "37fd0aa2-5be9-4313-80de-1f875e217b11",
          "delivery_uuid": "370fff76-b259-4456-8de2-f1c6f179b74a",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Deco1",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "10 Williams Okoro Street, Peace Estate, Aboru, Iyana Ipaja, Lagos",
          "created_at": "2025-01-09T08:03:05.000000Z",
          "items": [
            {
              "uuid": "201a9b2f-bd83-4120-b10f-f7dc62c6f5ee",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-09T08:03:06.000000Z"
            }
          ]
        },
        {
          "uuid": "35dedd1b-596a-4854-8287-4f04611ce5e8",
          "delivery_uuid": "b1a71541-2ace-413b-b588-329007362e81",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Deco2",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "10 Williams Okoro Street, Peace Estate, Aboru, Iyana Ipaja, Lagos",
          "created_at": "2025-01-09T08:03:06.000000Z",
          "items": [
            {
              "uuid": "3ac17941-729c-4520-b836-9f4675280474",
              "item_description": "pen",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-09T08:03:06.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "09942464-363d-47c6-8db2-b2b1aa4dd0c6",
        "sender_name": "Fela",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "10 Williams Okoro Street, Peace Estate, Aboru, Iyana Ipaja, Lagos",
        "business_owned": false,
        "created_at": "2025-01-09T08:03:05.000000Z",
        "updated_at": "2025-01-09T08:03:05.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "895ed4eb-c300-484d-af96-296802937691",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-09 09:17:18",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2025-01-09T08:03:54.000000Z"
      },
      "is_paid": false
    },
    {
      "uuid": "b1a71541-2ace-413b-b588-329007362e81",
      "rider_uuid": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
      "order_number": "ZlRgq",
      "fleet_identity_number": "78218528",
      "status": "In-Transit",
      "status_label": "In-Transit",
      "sender_longitude": null,
      "sender_latitude": null,
      "customer_longitude": null,
      "customer_latitude": null,
      "delivery_fee": "1500",
      "service_charge": "0",
      "currency": "NGN",
      "note": null,
      "creation_mode": "Manual",
      "created_at": "2025-01-08T23:00:00.000000Z",
      "pickup_at": "2025-01-09T09:17:17.000000Z",
      "dropoff_at": null,
      "customer_detail": [
        {
          "uuid": "37fd0aa2-5be9-4313-80de-1f875e217b11",
          "delivery_uuid": "370fff76-b259-4456-8de2-f1c6f179b74a",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Deco1",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "10 Williams Okoro Street, Peace Estate, Aboru, Iyana Ipaja, Lagos",
          "created_at": "2025-01-09T08:03:05.000000Z",
          "items": [
            {
              "uuid": "201a9b2f-bd83-4120-b10f-f7dc62c6f5ee",
              "item_description": "book",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-09T08:03:06.000000Z"
            }
          ]
        },
        {
          "uuid": "35dedd1b-596a-4854-8287-4f04611ce5e8",
          "delivery_uuid": "b1a71541-2ace-413b-b588-329007362e81",
          "status": "In-Transit",
          "dropoff_photo": null,
          "customer_name": "Deco2",
          "customer_email": null,
          "customer_phone_number": "08101299987",
          "customer_phone_code": "234",
          "customer_address": "10 Williams Okoro Street, Peace Estate, Aboru, Iyana Ipaja, Lagos",
          "created_at": "2025-01-09T08:03:06.000000Z",
          "items": [
            {
              "uuid": "3ac17941-729c-4520-b836-9f4675280474",
              "item_description": "pen",
              "item_quantity": 1,
              "item_value": "200.00",
              "currency": "NGN",
              "created_at": "2025-01-09T08:03:06.000000Z"
            }
          ]
        }
      ],
      "sender_detail": {
        "uuid": "09942464-363d-47c6-8db2-b2b1aa4dd0c6",
        "sender_name": "Fela",
        "sender_phone": "08101299987",
        "sender_email": null,
        "sender_phonecode": "234",
        "sender_address": "10 Williams Okoro Street, Peace Estate, Aboru, Iyana Ipaja, Lagos",
        "business_owned": false,
        "created_at": "2025-01-09T08:03:05.000000Z",
        "updated_at": "2025-01-09T08:03:05.000000Z"
      },
      "delivery_info_from_rider": {
        "id": "41bf4031-f8a7-4ae2-be4b-8235551bbe89",
        "rider_id": "6b8b5c9f-9182-407d-85cb-7fce108620e9",
        "status": "In Transit",
        "is_grouped": false,
        "picked_up_at": "2025-01-09 09:17:17",
        "dropped_off_at": null,
        "cancelled_reason": null,
        "created_at": "2025-01-09T09:03:52.000000Z"
      },
      "is_paid": false
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» status|string|true|none||none|
|» data|[object]|true|none||none|
|»» uuid|string|true|none||none|
|»» rider_uuid|string|true|none||none|
|»» order_number|string|true|none||none|
|»» fleet_identity_number|string|true|none||none|
|»» status|string|true|none||none|
|»» status_label|string|true|none||none|
|»» sender_longitude|string¦null|true|none||none|
|»» sender_latitude|string¦null|true|none||none|
|»» customer_longitude|string¦null|true|none||none|
|»» customer_latitude|string¦null|true|none||none|
|»» delivery_fee|string|true|none||none|
|»» service_charge|string|true|none||none|
|»» currency|string|true|none||none|
|»» note|null|true|none||none|
|»» creation_mode|string|true|none||none|
|»» created_at|string|true|none||none|
|»» pickup_at|string¦null|true|none||none|
|»» dropoff_at|null|true|none||none|
|»» customer_detail|[object]|true|none||none|
|»»» uuid|string|true|none||none|
|»»» delivery_uuid|string|true|none||none|
|»»» status|string|true|none||none|
|»»» dropoff_photo|string¦null|true|none||none|
|»»» customer_name|string|true|none||none|
|»»» customer_email|string¦null|true|none||none|
|»»» customer_phone_number|string|true|none||none|
|»»» customer_phone_code|string|true|none||none|
|»»» customer_address|string|true|none||none|
|»»» created_at|string|true|none||none|
|»»» items|[object]|true|none||none|
|»»»» uuid|string|true|none||none|
|»»»» item_description|string|true|none||none|
|»»»» item_quantity|integer¦null|true|none||none|
|»»»» item_value|string¦null|true|none||none|
|»»»» currency|string|true|none||none|
|»»»» created_at|string|true|none||none|
|»» sender_detail|object|true|none||none|
|»»» uuid|string|true|none||none|
|»»» sender_name|string|true|none||none|
|»»» sender_phone|string|true|none||none|
|»»» sender_email|string¦null|true|none||none|
|»»» sender_phonecode|string|true|none||none|
|»»» sender_address|string|true|none||none|
|»»» business_owned|boolean|true|none||none|
|»»» created_at|string|true|none||none|
|»»» updated_at|string|true|none||none|
|»» delivery_info_from_rider|object|true|none||none|
|»»» id|string|true|none||none|
|»»» rider_id|string|true|none||none|
|»»» status|string|true|none||none|
|»»» is_grouped|boolean|true|none||none|
|»»» picked_up_at|string¦null|true|none||none|
|»»» dropped_off_at|null|true|none||none|
|»»» cancelled_reason|string¦null|true|none||none|
|»»» created_at|string|true|none||none|
|»» is_paid|boolean|true|none||none|

# Data Schema

