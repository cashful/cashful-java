

# JwkDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**kid** | **String** | Key ID uniquely identifying the key |  |
|**kty** | **String** | Key type (e.g., &#39;RSA&#39;, &#39;EC&#39;, &#39;OKP&#39;) |  |
|**alg** | **String** | Algorithm intended for use with the key |  |
|**use** | [**UseEnum**](#UseEnum) | Intended use of the public key |  [optional] |
|**n** | **String** | Modulus for RSA keys |  [optional] |
|**e** | **String** | Exponent for RSA keys |  [optional] |
|**crv** | **String** | Curve name for elliptic curve keys |  [optional] |
|**x** | **String** | X coordinate for elliptic curve keys |  [optional] |
|**y** | **String** | Y coordinate for elliptic curve keys |  [optional] |



## Enum: UseEnum

| Name | Value |
|---- | -----|
| SIG | &quot;sig&quot; |


## Implemented Interfaces

* Serializable


