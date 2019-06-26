# Companies

- [Companies](#Companies)
  - [Overview](#Overview)
  - [List all the companies in your account](#List-all-the-companies-in-your-account)
    - [Parameters](#Parameters)
    - [Response](#Response)
  - [Update a company](#Update-a-company)
    - [Parameters](#Parameters-1)
    - [Example](#Example)
    - [Response](#Response-1)

## Overview

based on https://www.monicahq.com/api/companies (last accessed 2019-06-26 23:37:19)

## List all the companies in your account

```
GET /companies/
```

### Parameters

| Name  | Type    | Description                    |
| ----- | ------- | ------------------------------ |
| limit | integer | Indicates the page size.       |
| page  | integer | Indidcates the page to return. |

### Response

```json
{
  "data": [
    {
      "id": 1,
      "object": "company",
      "name": "Central Perk",
      "website": "http:\/\/url.com",
      "number_of_employees": 3,
      "account": {
        "id": 1
      },
      "created_at": "2019-01-02T14:44:30Z",
      "updated_at": "2019-01-02T14:47:07Z"
    },
    {
      "id": 3,
      "object": "company",
      "name": "ACME",
      "website": "http:\/\/url.com",
      "number_of_employees": 3,
      "account": {
        "id": 1
      },
      "created_at": "2019-01-02T14:49:07Z",
      "updated_at": "2019-01-02T14:49:07Z"
    }
  ],
  "links": {
    "first": "https:\/\/app.monicahq.com\/api\/companies?page=1",
    "last": "https:\/\/app.monicahq.com\/api\/companies?page=1",
    "prev": null,
    "next": null
  },
  "meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 1,
    "path": "https:\/\/app.monicahq.com\/api\/companies",
    "per_page": 15,
    "to": 2,
    "total": 2
  }
}
```

## Update a company

```
PUT /companies/:id
```

### Parameters

| Name | Type   | Description        |
| ---- | ------ | ------------------ |
| name | string | **Required.** .... |

### Example

```json
{
    "name": "Central Perk",
    "website": "http://url.com",
    "number_of_employees": 3
}
```

### Response

```json
{
  "data": {
    "id": 1,
    "object": "company",
    "name": "Central Perk",
    "website": "http:\/\/url.com",
    "number_of_employees": 3,
    "account": {
      "id": 1
    },
    "created_at": "2019-01-02T14:44:30Z",
    "updated_at": "2019-01-02T14:47:07Z"
  }
}
```