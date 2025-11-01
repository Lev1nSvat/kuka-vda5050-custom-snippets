# kuka-vda5050-custom-snippets
Custom snippets for VScode for writing json vda5050 files

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
