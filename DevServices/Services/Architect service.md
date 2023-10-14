Configuration example:
``` json
{
	"services":{
		"service_a":{
			"from":"registry",
			"name":"..."
		},
		"service_b":{
			"from":"url",
			"url":"..."
		},
		"main":{
			"from":"default",
			"name":"distributer"// web server to distribute requests to clusters
		}
	},
	"clusters":[
		{
			"ssh":{
				"host":"...",
				"port":"...",
				"key":"..."
			},
			"services":[
				"service_a",
				"service_b"
			],
			"endpoints":[/* endpoint setup */],
			"load_balancing":1// weight
		},
		{
			"ssh":{/*...*/},
			"services":[
				"service_b"
			],
			"endpoints":[/* endpoint setup */]
			"load_balancing":10
		},
		{
			"ssh":{/*...*/},
			"services":[
				"main"
			]
			// has no load_balancing, it's set to Infinity
		}
	]
}
```