## PRM Data Exchange
```yaml
-**id**: {
	max-length: 8,
	type: integer,
	nillable: false,
	label: unique passenger id,
},
-**date**: {
	format: DD/MM/YYYY,
	max-length: 10,
	type: string,
	nillable: false,
	label:Job date, 
},
-**smi**: {
	nillable: false, 
	max-length: 16, 
	type: string,
	values:{
		PRM: task created manualy either by dispatcher or by PickUpPoint agents locally,
		PSM: task created by the airline / origin airport,
		PAL or CAL: task created by travel agents (mostly used in europe)
		(also multiple entries possible ex: PSM,CAL,PAL,CAL)
	},
	label: Type of message sent to the PRM system,
},
-**ssr**: {
	nillable: false,
	max-length: 4,
	type: string
	values: {
		WCHR: Wheelchair Ramp
		WCHS: Wheelchair Steps
		WCHC: Wheelchair Carry
		MAAS: Meet and Assist
		DEAF: Deaf
		BLND: Blind
		DPNA: Intellectual or Developmental Disability
	},
	label: special service requirements
},
-**arr_airline_code**: {
	nillable: true,
	max-length: 3,
	type: string,
	label: airline code for incoming flights,
},
-**arr_flight_number**: {
	nillable: true,
	max-length: 4,
	type: integer,
	label: airline flight number for incoming flights
},
-**origin_iata_code**: {
	max-length: 3,
	type: string,
	nillable: true,
	label: iata code from flight origin
},
-**arr_date**: {
	label: flight arrival date, 
	format: dd/mm/yyyy,
	max-length: 10,
	type: string,
	nillable: true
},
-**sta**: {
	max-length:8,
	type: string,
	nillable: true,
	format: hh:mm:ss,
	label: local time - scheduled time of arrival
},
-**eta**: {
	label: local time - estimated time of arrival
	max-length:8,
	type: string,
	nillable: true,
	format: hh:mm:ss
},
-**arr_stand**: {
	label: Flight parking position of arrival,
	max-length: 3,
	type: string,
	nillable: true 
},
-**arr_pre_status**: {
	label: Time range of prenotification from PSM, CAL, PAL messages for arriving passengers,
	max-length: 4,
	type: string,
	nillable: true
},
-**dep_airline_code**: {
	nillable: true,
	max-length: 3,
	type: string,
	label: airline code for outgoing flights,
},
-**dep_flight_number**: {
	nillable: true,
	max-length: 4,
	type: integer,
	label: airline flight number for outgoing flights
},
-**dest_iata_code**: {
	nillable: true,
	max-length: 3,
	type: string,
	label: airport of destination IATA-code
},
-**dep_date**: {
	label: flight departure date, 
	format: DD/MM/YYYY,
	max-length: 10,
	type: string,
	nillable: true
},
-**std**: {
	label: local time - scheduled time of departure
	max-length:8,
	type: string,
	nillable: true,
	format: hh:mm:ss
},
-**etd**: {
	label: local time - estimated time of departure
	max-length:8,
	type: string,
	nillable: true,
	format: hh:mm:ss
},
-**dep_stand**: {
	label: Flight parking position of departure,
	max-length: 3,
	type: string,
	nillable: true 	
},
-**dep_pre_status**: {
	label: Time range of prenotification from PSM, CAL, PAL messages for departing passengers,
	max-length: 4,
	type: string,
	nillable: true,
	example: >32h
},
-**milestones_percent**: {
	max-length: 3,
	type: integer,
	nillable: false,
	label: Percentage of milestones completed
	example: 100
},
-**sorti_detail**: {
	max-length: 12,
	type: string,
	nillable: true,
	label: Identify NOSHOWS, or ALONE,
	example: NO SHOW
},
-**pbrm_d**: {
	max-length: 55,
	type: string
	nillable: true,
	label: Date in UTC when passenger arrived at PickUpPoint for outgoing flights
},
-**go_br**: {
	max-length: 55,
	type: string,
	nillable: true,
	label: Date in UTC when passenger has been collected at PickUpPoint for outgoing flights,
}
```
