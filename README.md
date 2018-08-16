Installs and configures OpenVPN
=====================

This role requires Ansible 2.0.0.2 or higher.

Variables
--------------

| Name                          | Default                                                       | Description                                                                                            |
|:------------------------------|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| vars_files_distribution            | Ubuntu                                                       | Version of distrib   
| vars_files_distribution_release           | xenial                                                       | Version of release  

Role Variables
--------------

| Name                          | Default                                                       | Description                                                                                            |
|:------------------------------|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| vpnclient_config_path         | /etc/openvpn/config.conf                                                       | Path to configuration files  
| vpnclient_server.address            | ru2.freeopenvpn.org                                                       | VPN server address  
| vpnclient_server.port            | 12595                                                       | VPN server port 
| vpnclient_version            | openvpn=2.3.10-1ubuntu2.1                                                       | VPN version 

Role Variables for setting the certificate and keys
--------------

**vpnclient_ca** # ca in config.conf

Default:
```yaml
-----BEGIN CERTIFICATE-----
  MIIDNTCCAh2gAwIBAgIJAMDWGcPiHbnCMA0GCSqGSIb3DQEBCwUAMBYxFDASBgNV
  BAMMC0Vhc3ktUlNBIENBMB4XDTE3MDEwMzIxMTgzMVoXDTI3MDEwMTIxMTgzMVow
  FjEUMBIGA1UEAwwLRWFzeS1SU0EgQ0EwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAw
  ggEKAoIBAQDCTrcHXkKt2U+y1BqNlnx1Ccrcj5agdqszlyE1vkNfoGxLSH4Q5fFk
  M7EYYP2l9RY1seWcJ6L/8aLJVRD/Z8rIlcMRgCAdMwNmiKSLLpNHv8yjhPhSt0si
  To4B/rpPKRmxczS1ZuKaU+V4i2ctx8dhrd/4JzfnJqkGCYEjPS3I4vl+8tMjoQkF
  Y3rAE5V+xA0TTZf2byE8iHYb3Dwhs+OlBrP59EY73CkEe6QCGgahVJ59vbs+FWZB
  LB7WHKWEPee9TFsMrDpI1N1PkaEOVmmFuWnWU9xBa281ULlDIh8aPadxnmzjmIXG
  JlTDlJJfbWwgRBAjO16dpkHUDS8t9Pr/AgMBAAGjgYUwgYIwHQYDVR0OBBYEFBs2
  2SVPbYQ5JKI8QtKt2d2GvlSiMEYGA1UdIwQ/MD2AFBs22SVPbYQ5JKI8QtKt2d2G
  vlSioRqkGDAWMRQwEgYDVQQDDAtFYXN5LVJTQSBDQYIJAMDWGcPiHbnCMAwGA1Ud
  EwQFMAMBAf8wCwYDVR0PBAQDAgEGMA0GCSqGSIb3DQEBCwUAA4IBAQA56+u+tMM/
  crZjv6ogzXawKEypoU4aLfl9XjEBbRIfuBDeo5A2xMQiAauQWArYKb/GaiBwDDCa
  W4wrhj1aMKxILL+Ppto0XsIKQ30S8e1OBJa7xJHIYzrFn1HngyTTlr207zMhYERr
  HYszQ4N3aVLObKb0w9aKGK3xfCMPBzAXjCcmTE1ErU6XENTnx5UNaK9l6yvxnUbx
  irFVsTTd0Eu+q8A3x3LGr/ggFZ3xRTmqbNf3mY66b2yeCQ1LBtV0jtrTZFY4IDmJ
  Y4Rk7MWkTonR/Y1PaIdmi2NeaJZCEuBS585ywcEeV6b0ODaHCEB2vwewpXdipXZ2
  UVF4I3AaI/l+
  -----END CERTIFICATE-----
```
**vpnclient_cert** # cert in config.conf

Default:
```yaml
-----BEGIN CERTIFICATE-----
  MIIDQDCCAiigAwIBAgIBAjANBgkqhkiG9w0BAQsFADAWMRQwEgYDVQQDDAtFYXN5
  LVJTQSBDQTAeFw0xNzAxMDMyMTIyNDJaFw0yNzAxMDEyMTIyNDJaMBcxFTATBgNV
  BAMMDGhlbGxvLndvcmxkZDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEB
  ALqii/OjtEIhpp19nwVjubT76Pg5HzBw5idP2XsmbgfZu9HLYW03Om09mJKD5OlX
  yg+eoijoSUKIsdJ0Yr+1Qi98XJamVgjPOANvbKGNFyNg4TpuVttD2mTU3uOaZ/xI
  GlStU7JLxtTtZkYc3Vv///al7/D9HPO3THjNUEmKSwlCZiOKO8UiJIx2S11AU3Sb
  M9t/iSzw7aWIAHVwpD84QcBqe+CZKxmtwQ06Dc6ZvuShAmt19xRphy2CiKz8bxsy
  Yft7CJUMrgLdI1kQmfyWvsDk4dMtqzCfnccB8RyxMuNxKp/QcRmS8/UklbcaLS7M
  2KF0fqCIver/RT+q6q2Aue8CAwEAAaOBlzCBlDAJBgNVHRMEAjAAMB0GA1UdDgQW
  BBRSXE6gGyQlWgxq+bm6Y4j5qdAQmTBGBgNVHSMEPzA9gBQbNtklT22EOSSiPELS
  rdndhr5UoqEapBgwFjEUMBIGA1UEAwwLRWFzeS1SU0EgQ0GCCQDA1hnD4h25wjAT
  BgNVHSUEDDAKBggrBgEFBQcDAjALBgNVHQ8EBAMCB4AwDQYJKoZIhvcNAQELBQAD
  ggEBAAwz0izj8QbZaHCM8mb424Un5a46mNe7G7d50q6YRH9iI07eeMJsFGvD87+i
  b7fdQ970ps31vrOvElt+wyz1r1lf6GfyKWsVx1ahYjX6TPupjoT2qGIrliQIu2QL
  PBQop8LmuxgDA8OqTB8oWlIDr5BX2P5hlNhSiIs3EIOFl5izq+HsS1k3WGGtd0Q3
  GriL7Q71AP/IElGTbLRhV99gasNtevsYMJRjVFaaVeh6Ktx7SZHHK0yO5P89YzYN
  VXBgtXDQlLnGfhZWIHwylXqczoxeGKC0ROpG11AzjrK+3SgpF3mPwowC8huC2Qb/
  cgSxv79EkTb3C79KUJTR8obinM8=
  -----END CERTIFICATE-----
```
**vpnclient_key** # key in config.conf

Default:
```yaml
-----BEGIN PRIVATE KEY-----
  MIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQC6oovzo7RCIaad
  fZ8FY7m0++j4OR8wcOYnT9l7Jm4H2bvRy2FtNzptPZiSg+TpV8oPnqIo6ElCiLHS
  dGK/tUIvfFyWplYIzzgDb2yhjRcjYOE6blbbQ9pk1N7jmmf8SBpUrVOyS8bU7WZG
  HN1b///2pe/w/Rzzt0x4zVBJiksJQmYjijvFIiSMdktdQFN0mzPbf4ks8O2liAB1
  cKQ/OEHAanvgmSsZrcENOg3Omb7koQJrdfcUaYctgois/G8bMmH7ewiVDK4C3SNZ
  EJn8lr7A5OHTLaswn53HAfEcsTLjcSqf0HEZkvP1JJW3Gi0uzNihdH6giL3q/0U/
  quqtgLnvAgMBAAECggEBAI82RbAKMTsBuWlmSM0I7iqblvRKWM2CBImr8xVVst7h
  TAc7SiJVW8cRme7ruI75p3p+3q4HOJgObm0wk8nJm+T2R9HuB1yxLaktKi15J4Ul
  RQ7iNlIAaigvVG1QQXTMGzBY5D2Peh5PoMgyRAXhlhc807aXc0zsnYig+3fC37tU
  31ynYcOrFFFUVozPmmQJOOVknmlzW/EdObvQ7bB+VeTusLExDoVYLXILk6d2ac0a
  yWCLbV6NA16e47A0KQKPERJbI4hD1MAkC+XmLjUIlRDZGMb/XG+tqHsocvJnsgrA
  Cu+5iMyslhHGPN4RsaweKieKtaUSc5Z+ZujALMCqKskCgYEA9hKBSOpe0dvTjDk9
  E5N+PDp9pnSj58RYPf2T5LdA9H0d29WPurzNn9nxfceFG4EGghvt2AP53XM6hUUJ
  cvj27sqB8sO2G+dgbfRq4h2AzWZWn7rKa30H4kVq1lH1Bh3zJ3KBONH7mjw1rTmp
  77tPr7WQRaRAHsiP2FZjp5CRPwMCgYEAwioog2AxYFIKD31Ux3f8CrM/1sRTc0tI
  k7S6GWCtRIAqE8xfhvFK9N2IVsDdryKvfLmn7X4GL8jmbjNmYILZ2ahI69qjBVuw
  xlhVNISoZKCtdIRWdtUQEVl7YX7lwJ/+n1D7WEcoE63nzbT3+0jm566fO/G4YcH5
  VlgMg6wrX6UCgYAPf9rk3N5cGZyZmIFgWkn5QTXo5i/syVFFllNadLCCtd7LmggT
  mxDYoMG1Snv334ipaVjx4k46xKdK/a46r7PeFqNYxzsRRuGsC1kwJOuYBHowVXOq
  kZWNixHPrhng6MIIGg5JpfBTJre60YcCsqmyR51uxYnEZp2o4sgkJdcAQQKBgFmR
  SQ8RmLVuIuXyUuGRH9tvxMs11akh2WEJxa9fQY6P8NkhNg/xzzoV14btgVYBEiLf
  IfAUapYwftvnKhrrQcN+NeVW/kzCd1GH/gY0C9ofpORTB+/ZaYgXVysqdqHdLIAh
  w1B9wqcRWhUynhJ1Fs9ZZmsonn26FWMXSu6SxY9hAoGBAJmVHpsb4YpwhnCIaOSj
  85WwRudIgo13g2sM/vffvQ9y5HwpdZnZ89przI7KRoNgO2rjpl+map73EYbgc7Zo
  2TSNrZHsAdIhUOuEgiY8LMT2crrIyuiPU1gmmbzcMRLO294IPrsFIfI4SkRzui09
  zKMH5YyzNqjlOuFt5llWzJKr
  -----END PRIVATE KEY-----
```
**vpnclient_tls_auth** # tls-auth in config.conf

Default:
```yaml
-----BEGIN PRIVATE KEY-----
  MIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQC6oovzo7RCIaad
  fZ8FY7m0++j4OR8wcOYnT9l7Jm4H2bvRy2FtNzptPZiSg+TpV8oPnqIo6ElCiLHS
  dGK/tUIvfFyWplYIzzgDb2yhjRcjYOE6blbbQ9pk1N7jmmf8SBpUrVOyS8bU7WZG
  HN1b///2pe/w/Rzzt0x4zVBJiksJQmYjijvFIiSMdktdQFN0mzPbf4ks8O2liAB1
  cKQ/OEHAanvgmSsZrcENOg3Omb7koQJrdfcUaYctgois/G8bMmH7ewiVDK4C3SNZ
  EJn8lr7A5OHTLaswn53HAfEcsTLjcSqf0HEZkvP1JJW3Gi0uzNihdH6giL3q/0U/
  quqtgLnvAgMBAAECggEBAI82RbAKMTsBuWlmSM0I7iqblvRKWM2CBImr8xVVst7h
  TAc7SiJVW8cRme7ruI75p3p+3q4HOJgObm0wk8nJm+T2R9HuB1yxLaktKi15J4Ul
  RQ7iNlIAaigvVG1QQXTMGzBY5D2Peh5PoMgyRAXhlhc807aXc0zsnYig+3fC37tU
  31ynYcOrFFFUVozPmmQJOOVknmlzW/EdObvQ7bB+VeTusLExDoVYLXILk6d2ac0a
  yWCLbV6NA16e47A0KQKPERJbI4hD1MAkC+XmLjUIlRDZGMb/XG+tqHsocvJnsgrA
  Cu+5iMyslhHGPN4RsaweKieKtaUSc5Z+ZujALMCqKskCgYEA9hKBSOpe0dvTjDk9
  E5N+PDp9pnSj58RYPf2T5LdA9H0d29WPurzNn9nxfceFG4EGghvt2AP53XM6hUUJ
  cvj27sqB8sO2G+dgbfRq4h2AzWZWn7rKa30H4kVq1lH1Bh3zJ3KBONH7mjw1rTmp
  77tPr7WQRaRAHsiP2FZjp5CRPwMCgYEAwioog2AxYFIKD31Ux3f8CrM/1sRTc0tI
  k7S6GWCtRIAqE8xfhvFK9N2IVsDdryKvfLmn7X4GL8jmbjNmYILZ2ahI69qjBVuw
  xlhVNISoZKCtdIRWdtUQEVl7YX7lwJ/+n1D7WEcoE63nzbT3+0jm566fO/G4YcH5
  VlgMg6wrX6UCgYAPf9rk3N5cGZyZmIFgWkn5QTXo5i/syVFFllNadLCCtd7LmggT
  mxDYoMG1Snv334ipaVjx4k46xKdK/a46r7PeFqNYxzsRRuGsC1kwJOuYBHowVXOq
  kZWNixHPrhng6MIIGg5JpfBTJre60YcCsqmyR51uxYnEZp2o4sgkJdcAQQKBgFmR
  SQ8RmLVuIuXyUuGRH9tvxMs11akh2WEJxa9fQY6P8NkhNg/xzzoV14btgVYBEiLf
  IfAUapYwftvnKhrrQcN+NeVW/kzCd1GH/gY0C9ofpORTB+/ZaYgXVysqdqHdLIAh
  w1B9wqcRWhUynhJ1Fs9ZZmsonn26FWMXSu6SxY9hAoGBAJmVHpsb4YpwhnCIaOSj
  85WwRudIgo13g2sM/vffvQ9y5HwpdZnZ89przI7KRoNgO2rjpl+map73EYbgc7Zo
  2TSNrZHsAdIhUOuEgiY8LMT2crrIyuiPU1gmmbzcMRLO294IPrsFIfI4SkRzui09
  zKMH5YyzNqjlOuFt5llWzJKr
  -----END PRIVATE KEY-----
```
