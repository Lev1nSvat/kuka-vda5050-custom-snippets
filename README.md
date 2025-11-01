# kuka-vda5050-custom-snippets
Custom snippets for VScode for writing json vda5050 files

Supported snippeds: 
- order `{
	"$schema": "https://raw.githubusercontent.com/VDA5050/VDA5050/refs/heads/main/json_schemas/order.schema",
	"headerId": 1761997656,
	"orderId": "1761997656",
	"timestamp": "2025-11-01T14:47:36.16Z",
	"version": "2.0.0",
	"manufacturer": "kuka",
	"serialNumber": "1583485",
	"orderUpdateId": 0,
	"nodes": [],
	"edges": []
}`
- node `{
	"nodeId": "id",
	"sequenceId": seqId,
	"released": true,
	"nodePosition": {
		"x": 0,
		"y": 0,
		"allowedDeviationXY": 0.05,
		"allowedDeviationTheta": 0.07,
		"mapId": "map_october_30_october_30_y2k_updateEdgeLabel_Config.xml,"
	},
	"actions": []
}`
- edge `{
	"edgeId": "e",
	"sequenceId": seqId,
	"released": true,
	"startNodeId" :"start",
	"endNodeId" :"end",
	"maxSpeed": 1,
	"orientation": 0,
	"actions": []
}`
- pick `{
	"actionId": "1761997737",
	"actionType": "pick",
	"blockingType": "HARD",
	"actionParameters" :
	[
		{
			"key": "loadType",
			"value": "9004"
		},
		{
			"key": "loadName",
			"value": "JHYD_Rack"
		}
	]
}`
- drop `{
	"actionId": "1761997757",
	"actionType": "drop",
	"blockingType": "HARD",
	"actionParameters" :
	[
		{
			"key": "loadType",
			"value": "9004"
		},
		{
			"key": "loadName",
			"value": "JHYD_Rack"
		}
	]
}`
- cancel `{
	"$schema": "https://raw.githubusercontent.com/VDA5050/VDA5050/refs/heads/main/json_schemas/instantActions.schema",
	"headerId": 1761997792,
	"timestamp": "2025-11-01T14:49:52.16Z",
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
}`
