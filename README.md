WcfConfigurationSamples
=======================

WsSecurityService
-----------------
configuration for WS-Security enabled service with custom username+password validation

sample request:
```xml
<Envelope xmlns="http://www.w3.org/2003/05/soap-envelope">
	<Header>
		<wsse:Security xmlns:wsse="http://schemas.xmlsoap.org/ws/2003/06/secext">
			<wsse:UsernameToken>
				<wsse:Username>aaa</wsse:Username>
				<wsse:Password>bbb</wsse:Password>
			</wsse:UsernameToken>
		</wsse:Security>
	</Header>
	<Body>
		<GetData xmlns="http://tempuri.org/">
			<value>123</value>
		</GetData>
	</Body>
</Envelope>
```

Config samples
--------------

HTTPS vs HTTP binding
```xml
        <binding name="XX">
          <!--HTTPS --> <security mode="Transport" />
          <!--HTTP--> <security mode="TransportCredentialOnly">
            <transport clientCredentialType="Basic"/>
          </security>
        </binding>
```
