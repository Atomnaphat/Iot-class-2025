# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
  client = mqtt.Client()
[16:09:42] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [16:09:42] DEBUG | Received CONNACK (0, 0)
asdasdasdasdasdasdasdasdasdasdsadasdasdasdasdasdasdasdasdasd
Enter QoS level (0, 1, 2): 2
[16:10:39] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6410301001/temperature'', ... (60 bytes)
[16:10:39] PUBLISH REQUESTED | QoS=2 | Message='asdasdasdasdasdasdasdasdasdasdsadasdasdasdasdasdasdasdasdasd' | msgid=1      
Enter message to publish: [16:10:39] DEBUG | Received PUBREC (Mid: 1)
[16:10:39] DEBUG | Sending PUBREL (Mid: 1)
[16:10:39] DEBUG | Received PUBCOMP (Mid: 1)
[16:10:39] PUBLISHED | msgid=1
[16:10:42] DEBUG | Sending PINGREQ
[16:10:42] DEBUG | Received PINGRESP
```

## Subscriber_qos.py Output

```
  client = mqtt.Client()
[16:04:57] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[16:04:57] DEBUG | Received CONNACK (0, 0)
[16:04:57] Connected with result code 0
[16:04:57] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6410301001', 2)]
[16:04:57] DEBUG | Received SUBACK
[16:05:58] DEBUG | Sending PINGREQ
[16:05:58] DEBUG | Received PINGRESP
[16:06:58] DEBUG | Sending PINGREQ
[16:06:58] DEBUG | Received PINGRESP
[16:07:59] DEBUG | Sending PINGREQ
[16:07:59] DEBUG | Received PINGRESP
[16:09:00] DEBUG | Sending PINGREQ
[16:09:00] DEBUG | Received PINGRESP
[16:10:00] DEBUG | Sending PINGREQ
[16:10:00] DEBUG | Received PINGRESP
[16:11:01] DEBUG | Sending PINGREQ
[16:11:01] DEBUG | Received PINGRESP
[16:12:01] DEBUG | Sending PINGREQ
[16:12:01] DEBUG | Received PINGRESP
[16:13:02] DEBUG | Sending PINGREQ
[16:13:02] DEBUG | Received PINGRESP

```