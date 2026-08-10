# \PerplexityApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**perplexity_ask_perplexity_a_question**](PerplexityApi.md#perplexity_ask_perplexity_a_question) | **GET** /v1/perplexity/ask | Ask Perplexity a question
[**perplexity_ask_perplexity_a_question_post**](PerplexityApi.md#perplexity_ask_perplexity_a_question_post) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST)
[**perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer**](PerplexityApi.md#perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer) | **GET** /v1/perplexity/brand-visibility | Measure a brand's visibility in a Perplexity answer
[**perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post**](PerplexityApi.md#perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post) | **POST** /v1/perplexity/brand-visibility | Measure a brand's visibility in a Perplexity answer (POST)
[**perplexity_perplexity_scraper_health_check**](PerplexityApi.md#perplexity_perplexity_scraper_health_check) | **GET** /v1/perplexity/health | Perplexity scraper health check
[**perplexity_perplexity_scraper_health_check_head**](PerplexityApi.md#perplexity_perplexity_scraper_health_check_head) | **HEAD** /v1/perplexity/health | Perplexity scraper health check



## perplexity_ask_perplexity_a_question

> serde_json::Value perplexity_ask_perplexity_a_question(prompt, country)
Ask Perplexity a question

Send a prompt to Perplexity and get the answer plus the web sources it cited.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to send to Perplexity (max 4096 characters). | [required] |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## perplexity_ask_perplexity_a_question_post

> serde_json::Value perplexity_ask_perplexity_a_question_post()
Ask Perplexity a question (POST)

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


## perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer

> serde_json::Value perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer(prompt, brand, domain, aliases, competitors, country)
Measure a brand's visibility in a Perplexity answer

Ask Perplexity, then report whether the brand is mentioned, cited and how prominently.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to ask Perplexity. | [required] |
**brand** | **String** | Brand name to look for in the answer. | [required] |
**domain** | Option<**String**> | Brand domain, for citation matching. |  |
**aliases** | Option<**String**> | Comma-separated alternative names. |  |
**competitors** | Option<**String**> | Comma-separated competitor names. |  |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post

> serde_json::Value perplexity_measure_a_brand_s_visibility_in_a_perplexity_answer_post()
Measure a brand's visibility in a Perplexity answer (POST)

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


## perplexity_perplexity_scraper_health_check

> serde_json::Value perplexity_perplexity_scraper_health_check()
Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

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


## perplexity_perplexity_scraper_health_check_head

> serde_json::Value perplexity_perplexity_scraper_health_check_head()
Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

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

