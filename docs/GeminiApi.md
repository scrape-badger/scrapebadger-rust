# \GeminiApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gemini_ask_gemini_a_question**](GeminiApi.md#gemini_ask_gemini_a_question) | **GET** /v1/gemini/ask | Ask Gemini a question
[**gemini_ask_gemini_a_question_post**](GeminiApi.md#gemini_ask_gemini_a_question_post) | **POST** /v1/gemini/ask | Ask Gemini a question (POST)
[**gemini_gemini_scraper_health_check**](GeminiApi.md#gemini_gemini_scraper_health_check) | **GET** /v1/gemini/health | Gemini scraper health check
[**gemini_gemini_scraper_health_check_head**](GeminiApi.md#gemini_gemini_scraper_health_check_head) | **HEAD** /v1/gemini/health | Gemini scraper health check
[**gemini_measure_a_brand_s_visibility_in_a_gemini_answer**](GeminiApi.md#gemini_measure_a_brand_s_visibility_in_a_gemini_answer) | **GET** /v1/gemini/brand-visibility | Measure a brand's visibility in a Gemini answer
[**gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post**](GeminiApi.md#gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post) | **POST** /v1/gemini/brand-visibility | Measure a brand's visibility in a Gemini answer (POST)



## gemini_ask_gemini_a_question

> serde_json::Value gemini_ask_gemini_a_question(prompt, country, web_search)
Ask Gemini a question

Send a prompt to Gemini and get the answer plus the web sources it cited.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to send to Gemini (max 4096 characters). | [required] |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. |  |
**web_search** | Option<**String**> | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened. |  |[default to auto]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gemini_ask_gemini_a_question_post

> serde_json::Value gemini_ask_gemini_a_question_post()
Ask Gemini a question (POST)

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


## gemini_gemini_scraper_health_check

> serde_json::Value gemini_gemini_scraper_health_check()
Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

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


## gemini_gemini_scraper_health_check_head

> serde_json::Value gemini_gemini_scraper_health_check_head()
Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

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


## gemini_measure_a_brand_s_visibility_in_a_gemini_answer

> serde_json::Value gemini_measure_a_brand_s_visibility_in_a_gemini_answer(prompt, brand, domain, aliases, competitors, country, web_search)
Measure a brand's visibility in a Gemini answer

Ask Gemini, then report whether the brand is mentioned, cited and how prominently.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to ask Gemini. | [required] |
**brand** | **String** | Brand name to look for in the answer. | [required] |
**domain** | Option<**String**> | Brand domain, for citation matching. |  |
**aliases** | Option<**String**> | Comma-separated alternative names. |  |
**competitors** | Option<**String**> | Comma-separated competitor names. |  |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country. |  |
**web_search** | Option<**String**> | auto | force | off |  |[default to force]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post

> serde_json::Value gemini_measure_a_brand_s_visibility_in_a_gemini_answer_post()
Measure a brand's visibility in a Gemini answer (POST)

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

