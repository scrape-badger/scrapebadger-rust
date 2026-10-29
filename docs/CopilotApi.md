# \CopilotApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**copilot_ask_copilot_a_question**](CopilotApi.md#copilot_ask_copilot_a_question) | **GET** /v1/copilot/ask | Ask Copilot a question
[**copilot_ask_copilot_a_question_post**](CopilotApi.md#copilot_ask_copilot_a_question_post) | **POST** /v1/copilot/ask | Ask Copilot a question (POST)
[**copilot_copilot_scraper_health_check**](CopilotApi.md#copilot_copilot_scraper_health_check) | **GET** /v1/copilot/health | Copilot scraper health check
[**copilot_copilot_scraper_health_check_head**](CopilotApi.md#copilot_copilot_scraper_health_check_head) | **HEAD** /v1/copilot/health | Copilot scraper health check
[**copilot_list_copilot_markets**](CopilotApi.md#copilot_list_copilot_markets) | **GET** /v1/copilot/markets | List Copilot markets
[**copilot_measure_a_brand_s_visibility_in_a_copilot_answer**](CopilotApi.md#copilot_measure_a_brand_s_visibility_in_a_copilot_answer) | **GET** /v1/copilot/brand-visibility | Measure a brand's visibility in a Copilot answer
[**copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post**](CopilotApi.md#copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post) | **POST** /v1/copilot/brand-visibility | Measure a brand's visibility in a Copilot answer (POST)



## copilot_ask_copilot_a_question

> serde_json::Value copilot_ask_copilot_a_question(prompt, country, market, strict_country)
Ask Copilot a question

Ask Microsoft Copilot (Copilot Search in Bing) and get the answer plus its cited sources.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to send to Copilot (max 2000 characters). | [required] |
**country** | Option<**String**> | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market. |  |
**market** | Option<**String**> | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's. |  |
**strict_country** | Option<**bool**> | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`. |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## copilot_ask_copilot_a_question_post

> serde_json::Value copilot_ask_copilot_a_question_post()
Ask Copilot a question (POST)

POST form of `/ask`, for prompts too long for a query string.

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## copilot_copilot_scraper_health_check

> serde_json::Value copilot_copilot_scraper_health_check()
Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## copilot_copilot_scraper_health_check_head

> serde_json::Value copilot_copilot_scraper_health_check_head()
Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## copilot_list_copilot_markets

> serde_json::Value copilot_list_copilot_markets()
List Copilot markets

The Bing markets Copilot can be asked in.

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## copilot_measure_a_brand_s_visibility_in_a_copilot_answer

> serde_json::Value copilot_measure_a_brand_s_visibility_in_a_copilot_answer(prompt, brand, domain, aliases, competitors, country, market, strict_country)
Measure a brand's visibility in a Copilot answer

Ask Copilot, then report whether the brand is mentioned, cited and how prominently.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to ask Copilot. | [required] |
**brand** | **String** | Brand name to look for in the answer. | [required] |
**domain** | Option<**String**> | Brand domain, for citation matching. |  |
**aliases** | Option<**String**> | Comma-separated alternative names. |  |
**competitors** | Option<**String**> | Comma-separated competitor names. |  |
**country** | Option<**String**> | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market. |  |
**market** | Option<**String**> | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's. |  |
**strict_country** | Option<**bool**> | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`. |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post

> serde_json::Value copilot_measure_a_brand_s_visibility_in_a_copilot_answer_post()
Measure a brand's visibility in a Copilot answer (POST)

POST form, for longer prompts and larger competitor sets.

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

