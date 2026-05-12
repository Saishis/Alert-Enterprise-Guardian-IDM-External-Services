### Delete Access
Deletes access.

API Call:
POST/api/access/update


**Request Example**

POST /api/access/update HTTP/1.1
Host: 
Content-Length: 259

{
"filterCriteria": [{
    "seq": 1,
     "fieldName": "id",
      "operator": "in",
        "valueList":["{{accessId}}"]
}],
 "size": 1,
"sortBy": [{"direction": "DESC", "property": "createdOn"}],
"updateFieldName": "intStatus",
"updateValue": 3
}

**Response Example**

{
  "success": true,
  "messages": [
    {
      "messageText": "All records (1) are marked as successful",
      "messageType": "INFO",
      "priority": 0
    }
  ],
  "data": [
    {
      "id": 4081719192866652,
      "id_str": "4081719192866652",
      "isReplaceEntityWhenFound": false,
      "intStatus": 3,
      "createdBy": 1,
      "createdOn": "2022-11-23T12:16:46.793+0000",
      "changedBy": 1,
      "changedOn": "2022-11-23T12:17:05.573+0000",
      "extId": "ACS-013142",
      "text": "UpdatedName",
      "description": "UpdatedName",
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
      "sourceId": "2002",
      "criticality": "HIGH",
      "highRisk": false,
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
    }
  ],
  "numberOfElements": 0,
  "totalPages": 0,
  "totalElements": 0,
  "pageNumber": 0,
  "pageSize": 0
}