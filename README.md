
https://dev-leadgen.apexure.org/
![[Pasted image 20230911192919.png]]

## information gathering

![[Pasted image 20230911193340.png]]

```css
$IP = 142.93.40.28
mail server = mail.dev-leadgen.apexure.org
```

5 open ports found
![[Pasted image 20230911200605.png]]

port scan
```css
PORT     STATE SERVICE    REASON          VERSION
21/tcp   open  tcpwrapped syn-ack ttl 250
22/tcp   open  tcpwrapped syn-ack ttl 46
| ssh-hostkey: 
|   2048 f2:2b:1e:3a:e3:7d:33:d8:38:c9:1c:cd:c8:d0:f2:76 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDXeV5OGfEjEm9V9qFOGgUo3Mm5NcEnOH8g68PY2WMnhJ6O4AkmvWY1RXmAP8BH8ibec9Y62N29LWFpQ5yaOsHfhBYlyxeTAsw7WEbg5BoX4bjTaZv5ZqiAQQT8FDJTfpQu4nB7u5+XOXbMwNlUBW2zwzvEpt5qX+SlOMUoK+z4DHg5R/17UzFPRmX5J+wUslKrnFv5ZVgs6wX8C2p4S1IUVTrVJAcUxv6OytV3RZqzpMrXJnv8XVc4O57sVJTLIHepfnimCNM3FmWP1eDjblf3MxvfcxjQt8UZY+t256AFW7mOd/2jSN645TuFuwSQ5q1bA7CSNrkSrsNabjVgwT3f
|   256 b0:d2:93:c0:b4:74:29:0b:9a:04:86:ba:78:78:93:7d (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIA1fzyLQpOJUJd1eNf/qorV1Fw215ofKeJl1kY4mzypq
80/tcp   open  http       syn-ack ttl 45  nginx 1.14.0 (Ubuntu)
|_http-title: Apache2 Ubuntu Default Page: It works
554/tcp  open  rtsp?      syn-ack ttl 250
1723/tcp open  tcpwrapped syn-ack ttl 250
```


```css
PORT     STATE    SERVICE      REASON      VERSION
21/tcp   open     ftp?         syn-ack
22/tcp   open     ssh          syn-ack     OpenSSH 7.6p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 80:5f:8f:13:4c:5b:66:de:d1:e6:01:eb:6d:b0:f9:81 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBI6NrEjKAraPd36S2wuOKHBhmG6VSeYxaxF1bWL/XEWCIaZr+4bGivybfXq8sHGrOhYfLzdqtydsoj2wVzd5xrc=
|   256 b0:d2:93:c0:b4:74:29:0b:9a:04:86:ba:78:78:93:7d (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIA1fzyLQpOJUJd1eNf/qorV1Fw215ofKeJl1kY4mzypq
25/tcp   filtered smtp         no-response
80/tcp   open     http         syn-ack     nginx 1.14.0 (Ubuntu)
135/tcp  filtered msrpc        no-response
139/tcp  filtered netbios-ssn  no-response
179/tcp  filtered bgp          no-response
443/tcp  open     ssl/https    syn-ack     nginx/1.14.0 (Ubuntu)
| http-methods: 
|_  Supported Methods: HEAD POST
| tls-alpn: 
|_  http/1.1
| ssl-cert: Subject: commonName=api.dev-leadgen.apexure.org
| Subject Alternative Name: DNS:api.dev-leadgen.apexure.org
| Issuer: commonName=R3/organizationName=Let's Encrypt/countryName=US
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-08-18T14:15:59
| Not valid after:  2023-11-16T14:15:58
| MD5:   3afb:0ac5:0984:d0b2:b2bd:517d:d8e4:6e51
| SHA-1: f780:baf7:9618:8783:ce47:b37d:c5b2:031b:1563:98ab
| -----BEGIN CERTIFICATE-----
| MIIFATCCA+mgAwIBAgISA1ucl+gcsbs73O1wRAPBcKldMA0GCSqGSIb3DQEBCwUA
| MDIxCzAJBgNVBAYTAlVTMRYwFAYDVQQKEw1MZXQncyBFbmNyeXB0MQswCQYDVQQD
| EwJSMzAeFw0yMzA4MTgxNDE1NTlaFw0yMzExMTYxNDE1NThaMCYxJDAiBgNVBAMT
| G2FwaS5kZXYtbGVhZGdlbi5hcGV4dXJlLm9yZzCCASIwDQYJKoZIhvcNAQEBBQAD
| ggEPADCCAQoCggEBAJp/26nkF4K1VXYM5xDI4a5W+fLxvxzrm9itoTA77kqAmaWu
| 3Zcrl2Ls7xHJmSWcZ5urtvDo35wKMVx/xh5ETFsxE+9OXhZIPVPv9lPGq8mGEkqi
| XnIfSxaUFy8KQkRdX/k+g8+i5SWG3KaxEWu6T9McMPabetk9VL/Fx9WFUmaUgZCN
| /CMuJLDUpk+aoINpAceBxojZOXE4wIRPyS70lLJeqgrrsJCrAz+jqVc4Omy0TlGD
| KksMYPIG4QwHfyVbtT5mV9h59bw/UqZukZEhMlujEgjtUoed47aa5hfew9SwrESR
| P6nKD9DKNha8HfW3/tS4PKDYC43gtCkYIS1MJNkCAwEAAaOCAhswggIXMA4GA1Ud
| DwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwDAYDVR0T
| AQH/BAIwADAdBgNVHQ4EFgQULybbp7tPgI5zmjLWUB+obgub7C4wHwYDVR0jBBgw
| FoAUFC6zF7dYVsuuUAlA5h+vnYsUwsYwVQYIKwYBBQUHAQEESTBHMCEGCCsGAQUF
| BzABhhVodHRwOi8vcjMuby5sZW5jci5vcmcwIgYIKwYBBQUHMAKGFmh0dHA6Ly9y
| My5pLmxlbmNyLm9yZy8wJgYDVR0RBB8wHYIbYXBpLmRldi1sZWFkZ2VuLmFwZXh1
| cmUub3JnMBMGA1UdIAQMMAowCAYGZ4EMAQIBMIIBAgYKKwYBBAHWeQIEAgSB8wSB
| 8ADuAHUAtz77JN+cTbp18jnFulj0bF38Qs96nzXEnh0JgSXttJkAAAGKCTexMAAA
| BAMARjBEAiEA77cXh/fFWob4nLX/fdWRlSxaMTYu1sltMXnbMb9+7XoCH1chL/je
| Kp3+C1efjxHxvzE6uRsTLvkdKOWMXqo1sZAAdQB6MoxU2LcttiDqOOBSHumEFnAy
| E4VNO9IrwTpXo1LrUgAAAYoJN7FUAAAEAwBGMEQCICXJBtlDFllE+4vpiah1dq6I
| ve/C2M+Rd3voTEjfLNndAiBSnO1EvVY3ESeAYfND/4kQ+Mmd9gQCWh7kXJWh0jrN
| 3TANBgkqhkiG9w0BAQsFAAOCAQEASdPY3w4V4c2Hf3KW7tAH0NdhPa73tfs7emOx
| jcTQe195PfxZlk7Lqu+bP4p05K/ALCz16tSZqltoaiawj/q+lvaua50dPZB/Gd+R
| Pn3iqK2qYowm8I8hR0iCqQmP2+GWhlfLv8gNMK31IoHl0xZUJe3KUtXo7+jN6iP6
| cvJsXQagi+OXtnLEWKADs4Z5N6fhU18oqPrBn1jCJ8ZsnyB9Cid++M/9jn5A8qRr
| LuAo/xB30M3qLOS+oQ2TQOO5c+Omt50hElO+7iA/YiPErSpazh0YKAPvKfC5tcVJ
| 3WKm2ZbH6H4SENjYzmEY/n49cy1uLOeCvWi64xxkR2A3+cPkrA==
|_-----END CERTIFICATE-----
|_http-title: Site doesn't have a title (application/json).
| tls-nextprotoneg: 
|_  http/1.1
| http-robots.txt: 1 disallowed entry 
|_/
|_http-favicon: Unknown favicon MD5: D41D8CD98F00B204E9800998ECF8427E
|_http-server-header: nginx/1.14.0 (Ubuntu)
445/tcp  filtered microsoft-ds no-response
554/tcp  open     rtsp?        syn-ack
646/tcp  filtered ldp          no-response
1723/tcp open     pptp?        syn-ack
9220/tcp filtered unknown      no-response
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

```

## Available exploits for port 22/ssh

```css
22/tcp   open  ssh        syn-ack ttl 46  OpenSSH 7.6p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| vulners: 
|   cpe:/a:openbsd:openssh:7.6p1: 
|     	EXPLOITPACK:98FE96309F9524B8C84C508837551A19	5.8	https://vulners.com/exploitpack/EXPLOITPACK:98FE96309F9524B8C84C508837551A19	*EXPLOIT*
|     	EXPLOITPACK:5330EA02EBDE345BFC9D6DDDD97F9E97	5.8	https://vulners.com/exploitpack/EXPLOITPACK:5330EA02EBDE345BFC9D6DDDD97F9E97	*EXPLOIT*
|     	EDB-ID:46516	5.8	https://vulners.com/exploitdb/EDB-ID:46516	*EXPLOIT*
|     	EDB-ID:46193	5.8	https://vulners.com/exploitdb/EDB-ID:46193	*EXPLOIT*
|     	CVE-2019-6111	5.8	https://vulners.com/cve/CVE-2019-6111
|     	1337DAY-ID-32328	5.8	https://vulners.com/zdt/1337DAY-ID-32328	*EXPLOIT*
|     	1337DAY-ID-32009	5.8	https://vulners.com/zdt/1337DAY-ID-32009	*EXPLOIT*
|     	SSH_ENUM	5.0	https://vulners.com/canvas/SSH_ENUM	*EXPLOIT*
|     	PACKETSTORM:150621	5.0	https://vulners.com/packetstorm/PACKETSTORM:150621	*EXPLOIT*
|     	EXPLOITPACK:F957D7E8A0CC1E23C3C649B764E13FB0	5.0	https://vulners.com/exploitpack/EXPLOITPACK:F957D7E8A0CC1E23C3C649B764E13FB0	*EXPLOIT*
|     	EXPLOITPACK:EBDBC5685E3276D648B4D14B75563283	5.0	https://vulners.com/exploitpack/EXPLOITPACK:EBDBC5685E3276D648B4D14B75563283	*EXPLOIT*
|     	EDB-ID:45939	5.0	https://vulners.com/exploitdb/EDB-ID:45939	*EXPLOIT*
|     	EDB-ID:45233	5.0	https://vulners.com/exploitdb/EDB-ID:45233	*EXPLOIT*
|     	CVE-2018-15919	5.0	https://vulners.com/cve/CVE-2018-15919
|     	CVE-2018-15473	5.0	https://vulners.com/cve/CVE-2018-15473
|     	1337DAY-ID-31730	5.0	https://vulners.com/zdt/1337DAY-ID-31730	*EXPLOIT*
|     	CVE-2021-41617	4.4	https://vulners.com/cve/CVE-2021-41617
|     	CVE-2020-14145	4.3	https://vulners.com/cve/CVE-2020-14145
|     	CVE-2019-6110	4.0	https://vulners.com/cve/CVE-2019-6110
|     	CVE-2019-6109	4.0	https://vulners.com/cve/CVE-2019-6109
|     	CVE-2018-20685	2.6	https://vulners.com/cve/CVE-2018-20685
|     	PACKETSTORM:151227	0.0	https://vulners.com/packetstorm/PACKETSTORM:151227	*EXPLOIT*
|     	MSF:AUXILIARY-SCANNER-SSH-SSH_ENUMUSERS-	0.0	https://vulners.com/metasploit/MSF:AUXILIARY-SCANNER-SSH-SSH_ENUMUSERS-	*EXPLOIT*
|_    	1337DAY-ID-30937	0.0	https://vulners.com/zdt/1337DAY-ID-30937	*EXPLOIT*
```
