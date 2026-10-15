

# BulkDomainAvailabilityRequest

Request body for POST /v2.0/domain/availability. Use domainNames OR tld.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**domainNames** | **List&lt;String&gt;** | Mode 1: list of full domain names. Cannot be used with tld. |  [optional] |
|**tld** | **List&lt;String&gt;** | Mode 2: TLDs to check against the domain query param. Cannot be used with domainNames. |  [optional] |



