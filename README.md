# kuka-vda5050-custom-snippets
Custom snippets for VScode for writing json vda5050 files

In examples below empty fields will have default values on which your cursos will be placed after pressing Tab. exceptions are:
- "timestamp" will be generated automatically based on the time snipped was created
- "headerId" and "orderId" will be filled with UNIX seconds (number of seconds since 00:00:00 (UTC) on January 1, 1970) to ensure these fields will always be unique and bigger than in previous orders. There is a special qIDs snipped for quick update of these fields.

Supported snippeds: 
- order
```json
{
	"$schema": "https://raw.githubusercontent.com/VDA5050/VDA5050/refs/heads/main/json_schemas/order.schema",
	"headerId": ,
	"orderId": "",
	"timestamp": "",
	"version": "2.0.0",
	"manufacturer": "kuka",
	"serialNumber": "1583485",
	"orderUpdateId": 0,
	"nodes": [],
	"edges": []
}
```
- node
```json
{
	"nodeId": "",
	"sequenceId": ,
	"released": true,
	"nodePosition": {
		"x": ,
		"y": ,
		"allowedDeviationXY": 0.05,
		"allowedDeviationTheta": 0.07,
		"mapId": "map_october_30_october_30_y2k_updateEdgeLabel_Config.xml,"
	},
	"actions": []
}
```
- edge
```json
{
	"edgeId": "e",
	"sequenceId": ,
	"released": true,
	"startNodeId" :"",
	"endNodeId" :"",
	"maxSpeed": 1,
	"orientation": 0,
	"actions": []
}
```
- pick
```json
{
	"actionId": "",
	"actionType": "pick",
	"blockingType": "HARD",
	"actionParameters" :
	[
		{
			"key": "loadType",
			"value": ""
		},
		{
			"key": "loadName",
			"value": ""
		}
	]
}
```
- drop
```json
{
	"actionId": "",
	"actionType": "drop",
	"blockingType": "HARD",
	"actionParameters" :
	[
		{
			"key": "loadType",
			"value": ""
		},
		{
			"key": "loadName",
			"value": ""
		}
	]
}
```
- cancel
```json
{
	"$schema": "https://raw.githubusercontent.com/VDA5050/VDA5050/refs/heads/main/json_schemas/instantActions.schema",
	"headerId": ,
	"timestamp": "",
	"version": "2.0.0",
	"manufacturer": "kuka",
	"serialNumber": "1583485",
	"orderUpdateId": 0,
	"actions": [
		{
			"actionId": "0",
			"actionType": "canceOrder",
			"blockingType": "HARD"
		}
	]
}
```
- qIDs ($CURRENT_SECONDS_UNIX will automatically become a number of seconds)
```json
	"headerId": $CURRENT_SECONDS_UNIX,
	"orderId": "$CURRENT_SECONDS_UNIX",
```
