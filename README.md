# bitcoin-cryptography

is:open is:pr author:app/github-actions 

2021-01-29 16:24:06 UTC
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 26 so you won 2 tokens
Client seed 1b08b782
Server seed 1480c1003409b86810c64e8fc565a970
Server seed hash f0eaa47b858dbf8e543102edea22a554003c8203995c99e79bdfdcfab9704d9c
2021-01-29 16:24:05 UTC

Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 168 so you won 2 tokens
Client seed 5de92f4d
Server seed f0089d8329291ecaed4ff0af7eaf455a
Server seed hash 82bc4919731f9ed282a802326f7d11a75399f08d6b24acdee5eecef75f04a956
2021-01-29 16:24:05 UTC
frontend fe_mqtt
  mode tcp  
  bind :1993

  # Reject connections that have an invalid MQTT packet
  tcp-request content reject unless { req.payload(0,0),mqtt_is_valid }
  default_backend be_mqtt

backend be_mqtt
  mode tcp

  # Create a stick table for session persistence
  stick-table type string len 32 size 100k expire 30m

  # Use ClientID / client_identifier as persistence key
  stick on req.payload(0,0),mqtt_field_value(connect,client_identifier)

  server mosquitto1 10.1.0.6:1883
  server mosquitto2 10.1.0.7:1883
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 116 so you won 2 tokens
Client seed da0f7ff3
Server seed f7760a888a8e59605818fac719b113f4
Server seed hash c4d80ade8461b2ab605cf022b39be33b22dca8f431bf229d3de1af90e1cc2b9a
2021-01-29 16:24:04 UTC
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 701 so you did not win
Client seed b088acf2
Server seed 042895a82b5168ac3b00eff0b4a1031b
Server seed hash ff760b96e64137d0c43aab15b6372fa6081812c442ef0801ea792ff602e3e31d
2021-01-29 16:24:04 UTC
it broken?
  acl circuit_open be_name,table_gpc1 gt 0

  # Reject request if circuit is broken
  http-request return status 503 content-type "application/json" string "{ \"message\": \"Circuit Breaker tripped\" }" if circuit_open

  # Begin tracking requests
  http-request track-sc0 be_name

  # Store the HTTP request rate and error rate in variables
  http-response set-var(res.req_rate) sc_http_req_rate(0)
  http-response set-var(res.err_rate) sc_http_fail_rate(0)

  # Check if error rate is greater than 50% using some math
  http-response sc-inc-gpc1(0) if { int(100),mul(res.err_rate),div(res.req_rate) gt 50 }
  
  server s1 192.168.0.10:80 check
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 968 so you did not win
Client seed d96fb53e
Server seed b5d063a89a446ab9eaa8842e1bcd29de
Server seed hash c99be15ee350dc9599807ac25a981e33990f7a3e03df63b6e540f61253dcbe76
2021-01-29 16:24:03 UTC
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 384 so you won 2 tokens
Client seed 11a50d45
Server seed 677c4d365c9910d0f509ded08ab01e05
Server seed hash e0838e7fdf84e3bdcb20ad0d3581fd0651b0fb6a256757a17831a9ea80425836
2021-01-29 16:24:02 UTC
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 105 so you won 2 tokens
Client seed ce947dc1
Server seed 09391dbf75905f1eb4756fffb3003245
Server seed hash 99224a9ae86a294ff51ec2849f341b9f9e7a17b2e1bb4a7283579eaaf5ed086c
2021-01-29 16:24:01 UTC
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 699 so you did not win
Client seed a805585d
Server seed e4172d4fc120deea5546b233abf7fad3
Server seed hash d9e8e46c79b69aeab73b455b69bfc8b026b6f4d5d413946848e7d31d782f2967
2021-01-29 16:24:00 UTC
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 51 so you won 2 tokens
Client seed 67fa2158
Server seed 1af2a4b2c08f2132756cf4789ecd34b3
Server seed hash 8e096ff879bd0e2fca9ceda9afccd06093459f3077d13e6c3021a007bb6cfde9
2021-01-29 16:23:59 UTC
# Get loaded certificates
$ echo "show ssl cert" |socat /var/run/haproxy/api.sock -

# filename
/etc/haproxy/cert/haproxy-client.pem

# Update HAProxy's client certificate
$ echo -e -n "set ssl cert /etc/haproxy/cert/haproxy-client.pem <<\n$(cat /etc/haproxy/cert/haproxy-client.pem)\n\n" |socat /var/run/haproxy/api.sock -

Transaction created for certificate /etc/haproxy/cert/haproxy-client.pem!

# Commit the SSL transaction
$ echo "commit ssl cert /etc/haproxy/cert/haproxy-client.pem" |socat /var/run/haproxy/api.sock -

Committing /etc/haproxy/cert/haproxy-client.pem.
Success!
Roll 000-499 to win 2 times your stake of 1 token (50% win chance)
You rolled 737 so you did not win
Client seed ae29d1e3
Server seed 60ed5ce28bb78f366bead03e2690553e
Server seed hash 13d77242c5abc82c40fb067712bad8d47cba67b06f23d096930bc4e34bf9cba6
© 2017-2019 CoinPot | Contact | Terms | Privacy
