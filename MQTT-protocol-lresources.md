# MQTT

MQTT is a lightweight, publish-subscribe network protocol that transports messages between devices. The protocol usually runs over TCP/IP, however, any network protocol that provides ordered, lossless, bi-directional connections can support MQTT.[1] It is designed for connections with remote locations where resource constraints exist or the network bandwidth is limited. The protocol is an open OASIS standard and an ISO recommendation (ISO/IEC 20922).


Andy Stanford-Clark (IBM) and Arlen Nipper (then working for Eurotech, Inc.) authored the first version of the protocol in 1999.[5] It was used to monitor oil pipelines within the SCADA industrial control system.[6] The goal was to have a protocol that is bandwidth-efficient, lightweight and uses little battery power, because the devices were connected via satellite link which, at that time, was extremely expensive.[7]

Historically, the "MQ" in "MQTT" came from the IBM MQ (then 'MQSeries') MQ product line, where it stands for "Message Queue". However, the protocol provides publish-and-subscribe messaging (no queues, in spite of the name).[8] In the specification opened by IBM as version 3.1 the protocol was referred to as "MQ Telemetry Transport".[9][10] Subsequent versions released by OASIS strictly refers to the protocol as just "MQTT", although the technical committee itself is named "OASIS Message Queuing Telemetry Transport Technical Committee".[2] Since 2013, "MQTT" does not stand for anything.[11][8]

In 2013, IBM submitted MQTT v3.1 to the OASIS specification body with a charter that ensured only minor changes to the specification could be accepted.[2] After taking over maintenance of the standard from IBM, OASIS released version 3.1.1 on October 29, 2014.[12][13] A more substantial upgrade to MQTT version 5, adding several new features,[14] was released on March 7, 2019.[1]

MQTT-SN (MQTT for Sensor Networks) is a variation of the main protocol aimed at battery-powered embedded devices on non-TCP/IP networks,[15] such as Zigbee.[16]
 