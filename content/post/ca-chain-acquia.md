---
title: "Generate CA Chain for Acquia Environment"
date: 2020-07-10T00:20:25+08:00
tags: [sslcert, tlscert, ca, acquia]
draft: false
---

From Comodo Email after verifying domain ownership, got this hints:
```
Root CA Certificate - AAACertificateServices.crt
Intermediate CA Certificate - USERTrustRSAAAACA.crt
Intermediate CA Certificate - SectigoRSADomainValidationSecureServerCA.crt
Your PositiveSSL Multi-Domain Certificate - 378394251.crt
```

Generate the CA Chain as follows:
```
cat AAACertificateServices.crt USERTrustRSAAAACA.crt SectigoRSADomainValidationSecureServerCA.crt > ca-chain-acquia-prod.pem
```

And add to Acquia SSL section in corresponding environment.
