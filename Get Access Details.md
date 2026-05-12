### Get Access Details
Retrieves detailed information about a specific access record.

API Call:
GET/api/access/{{accessId}}

**Request Example**
GET /api/access/{{accessId}} HTTP/1.1
Host: 

**Response Example**
{
  "success": true,
  "data": {
    "id": 4081500016430990,
    "id_str": "4081500016430990",
    "isReplaceEntityWhenFound": false,
    "intStatus": 0,
    "createdBy": 1,
    "createdOn": "2022-11-23T10:11:34.874+0000",
    "changedBy": 1,
    "changedOn": "2022-11-23T10:11:34.874+0000",
    "extId": "ACS-013141",
    "text": "TestAccess471368",
    "description": "TestAccess471368",
    "type": "AC-001",
    "accessType": {
      "id": 2,
      "isReplaceEntityWhenFound": false,
      "intStatus": 0,
      "extId": "AC-001",
      "text": "Physical System",
      "description": "Access for Physical System",
      "icon": "/resources/shared/images/icons/accessType/physys.svg"
    },
    "sourceId": "1001",
    "criticality": "HIGH",
    "highRisk": true,
    "system": {
      "id": 20,
      "isReplaceEntityWhenFound": false,
      "intStatus": 0,
      "createdBy": 1,
      "createdOn": "2020-09-21T17:29:53.736+0000",
      "changedBy": 1,
      "changedOn": "2022-11-22T10:15:24.255+0000",
      "extId": "CCMAS-LAB",
      "text": "CCMAS-LAB",
      "description": "CCURE MAS - LAB",
      "type": "CCU-001",
      "systemType": {
        "id": 20,
        "isReplaceEntityWhenFound": false,
        "intStatus": 0,
        "createdBy": 1,
        "createdOn": "2020-12-10T05:52:25.890+0000",
        "changedBy": 1,
        "changedOn": "2021-04-13T01:48:59.828+0000",
        "extId": "CCU-001",
        "text": "CCURE 9000 ",
        "description": "System Type for CCURE9000",
        "category": "PHYSICALSYSTEM",
        "icon": "3248119136501229",
        "masterIdentityIdisSourceId": false
      },
      "isAuthenticationSystem": true
    },
    "systemId": 20,
    "isAlertAuthorization": true,
    "userGroup": true
  },
  "numberOfElements": 0,
  "totalPages": 0,
  "totalElements": 0,
  "pageNumber": 0,
  "pageSize": 0
}

| --- | --- | --- |
|**Field**|**Type**|**Description**|
| --- | --- | --- |
| success | Boolean | Query success status. |
| --- | --- | --- |
| data.id | Integer | Internal ID. |
| --- | --- | --- |
| data.extId | String | External identifier. |
| --- | --- | --- |
| data.text | String | Access name. |
| --- | --- | --- |
| data.description | String | Description. |
| --- | --- | --- |
| data.type | String | Access type code. |
| --- | --- | --- |
| data.accessType | Object | Nested details of access type (id, extId, text, description, icon). |
| --- | --- | --- |
| data.system | Object | Nested system details (id, extId, text, description, type). |
| --- | --- | --- |
| data.system.systemType | Object | Nested system type details (id, extId, text, description, category, icon). |
| --- | --- | --- |
| criticality | String | Risk classification. |
| --- | --- | --- |
| highRisk | Boolean | Risk flag. |
| --- | --- | --- |
