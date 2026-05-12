### Find Access And Verify Details
Searches for specific access records using filter criteria.

API Call:
POST/api/action/find

**Request Example**

POST /action/find HTTP/1.1
Host: api
Content-Length: 171

{
    "filterCriteria": [
        {
            "fieldName": "accessId",
            "operator": "in",
            "valueList":["{{accessId}}"]
        }
    ]

}

|---------|--------|---------------|
|**Field**|**Type**|**Description**|
|---------|--------|---------------|
|filterCriteria|Array|List of filters. Each filter includes:|
|---------|--------|---------------|
|fieldName|String|Field to filter (e.g., accessId).|
|---------|--------|---------------|
|operator|String|Comparison operator (e.g., in, equals).|
|---------|--------|---------------|
|valueList|Array|Values to match (e.g., [“ACS-013141”]).|
|---------|--------|---------------|

**Response Example**

{
  "success": true,
  "numberOfElements": 0,
  "totalPages": 0,
  "totalElements": 0,
  "pageNumber": 0,
  "pageSize": 50
}

| --- | --- | --- |
|**Field**|**Type**|**Description**|
| --- | --- | --- |
| success | Boolean | Query success status. |
| --- | --- | --- |
| numberOfElements | Integer | Number of records returned. |
| --- | --- | --- |
| totalPages | Integer | Pagination metadata. |
| --- | --- | --- |
| totalElements | Integer | Total records available. |
| --- | --- | --- |
| pageNumber | Integer | Current page. |
| --- | --- | --- |
| pageSize | Integer | Records per page. |
| --- | --- | --- |