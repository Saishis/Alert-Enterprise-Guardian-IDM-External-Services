### Check Filter Functionality


API Call:
POST/api/access/find

**Request Example**

POST /api/access/find HTTP/1.1
Host: 
Content-Length: 386

{
    "jsonView": "HEADER", 
    "filterCriteria": [
        {"fieldName": "intStatus", "operator": "in", "valueList": [9, 0]},
        {"fieldName": "linkedId", "operator": "isnull"},
        {"fieldName": "text", "operator": ":", "value": "updatedname"}
    ],


"page": 1,
"size": 25,
"sortByString": "[{\"property\":\"createdOn\",\"direction\":\"DESC\"}]",
"start": 0
}

| --- | --- |
|**Field**|**Meaning**|
| --- | --- |
| fieldName | The attribute you want to filter on (e.g., ``accessId``, ``systemId``, ``criticality``). |
| --- | --- |
| operator | Defines how the filter is applied (e.g., ``in``, ``equals``, ``like``). |
| --- | --- |
| valueList | The values to match against (e.g., list of IDs or names). |
| --- | --- |

**Response Example**

{
  "success": true,
  "data": [
    {
      "id": 4081500016430990,
      "id_str": "4081500016430990",
      "intStatus": 0,
      "createdBy": 1,
      "createdOn": "2022-11-23T15:41:34.874+0530",
      "changedBy": 1,
      "changedOn": "2022-11-23T16:22:22.430+0530",
      "extId": "ACS-013141",
      "text": "UpdatedName",
      "description": "UpdatedName",
      "type": "AC-001",
      "accessType": {
        "id": 2,
        "intStatus": 0,
        "extId": "AC-001",
        "text": "Physical System",
        "description": "Access for Physical System",
        "icon": "/resources/shared/images/icons/accessType/physys.svg",
        "replaceEntityWhenFound": false
      },
      "sourceId": "2002",
      "criticality": "HIGH",
      "highRisk": false,
      "system": {
        "id": 20,
        "intStatus": 0,
        "createdBy": 1,
        "createdOn": "2020-09-21T22:59:53.736+0530",
        "changedBy": 1,
        "changedOn": "2022-11-22T15:45:24.255+0530",
        "extId": "CCMAS-LAB",
        "text": "CCMAS-LAB",
        "description": "CCURE MAS - LAB",
        "type": "CCU-001",
        "systemType": {
          "id": 20,
          "intStatus": 0,
          "createdBy": 1,
          "createdOn": "2020-12-10T11:22:25.890+0530",
          "changedBy": 1,
          "changedOn": "2021-04-13T07:18:59.828+0530",
          "extId": "CCU-001",
          "text": "CCURE 9000 ",
          "description": "System Type for CCURE9000",
          "category": "PHYSICALSYSTEM",
          "icon": "3248119136501229",
          "masterIdentityIdisSourceId": false,
          "replaceEntityWhenFound": false
        },
        "isAuthenticationSystem": true,
        "replaceEntityWhenFound": false
      },
      "systemId": 20,
      "isAlertAuthorization": true,
      "userGroup": true,
      "replaceEntityWhenFound": false
    }
  ],
  "numberOfElements": 1,
  "totalPages": 1,
  "totalElements": 1,
  "pageNumber": 0,
  "pageSize": 25
}
